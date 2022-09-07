---
title: 🗞️ easypubsub
summary: A simple wrapper around PyZMQ that provides an easy interface to the PubSub (Publish-Subscribe) functionality of ZeroMQ.

date: '2022-07-29T00:00:00Z'

url_pdf: ''
url_slides: ''
url_video: ''
links:
  - name: GitHub
    icon: github
    icon_pack: fab
    url: 'https://github.com/matpompili/easypubsub'
  - name: Documentation
    icon: book
    url: 'https://easypubsub.readthedocs.io/en/latest/'

slides: ""
---

`easypubsub` is a simple wrapper around [PyZMQ](https://pyzmq.readthedocs.io/en/latest/) that provides an easy interface to the *PubSub* (Publish-Subscribe) functionality of [ZeroMQ](https://zeromq.org/). 

In PubSub, a *publisher* publishes a message to a *topic* and a *subscriber* subscribes to that topic and receives the message. In `easypubsub`, publishers and subscribers connect to each other via a *proxy*, which acts as intermediary between them.
For more information regarding *PubSub*, see [Wikipedia](https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern).

## Get started

`easypubsub` can be installed via `pip`:

```bash
pip install easypubsub
```

### Proxy

Now let's start a proxy (code from `examples/example_proxy.py`):

```python
import time

from easypubsub.proxy import Proxy

PUBLISHERS_ADDRESS = "tcp://127.0.0.1:5555"
SUBSCRIBERS_ADDRESS = "tcp://127.0.0.1:5556"

proxy = Proxy(PUBLISHERS_ADDRESS, SUBSCRIBERS_ADDRESS)
proxy.launch()

try:
    while True:
        time.sleep(0.1)
except KeyboardInterrupt:
    proxy.stop()
```

This starts a proxy (stoppable with `CTRL-C`) that allows publishers to publish messages to `PUBLISHERS_ADDRESS` and subscribers to subscribe to topics on `SUBSCRIBERS_ADDRESS`. By using a proxy, publishers and subscribers can connect to each other without having to know each other's addresses.

### Publisher

Let's create a publisher that every ten seconds announces one random number (code from `examples/example_publisher.py`):

```python
import random
import time

from easypubsub.publisher import Publisher

PUBLISHERS_ADDRESS = "tcp://127.0.0.1:5555"
PUBLISH_INTERVAL = 10  # seconds.

publisher = Publisher("lottery", PUBLISHERS_ADDRESS, default_topic="winning_number")
try:
    while True:
        publisher.publish(message=random.randint(1, 100))
        time.sleep(PUBLISH_INTERVAL)
except KeyboardInterrupt:
    pass
```

### Subscriber

Now we can create a subscriber that prints the winning number every time it receives one (code from `examples/example_subscriber.py`):

```python
import time

from easypubsub.subscriber import Subscriber

SUBSCRIBERS_ADDRESS = "tcp://127.0.0.1:5556"
subscriber = Subscriber("lottery_player", SUBSCRIBERS_ADDRESS)

try:
    while True:
        result = subscriber.receive()
        if len(result) > 0:
            print("Received:")
            for topic, message in result:
                print(f"{topic}: {message}")
        else:
            # No message received.
            time.sleep(1.0)
except KeyboardInterrupt:
    pass
```

There can be many publishers and subscribers connected to the same proxy, try starting a few of them with different names!

For more detailed information, please visit the [documentation](https://easypubsub.readthedocs.io/en/latest/).
