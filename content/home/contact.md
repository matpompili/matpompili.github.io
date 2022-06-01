---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: false

  # Email form provider
  # form:
  #   post_action: 'https://formsubmit.co/your@email.com'
  #   provider: netlify
    # formspree:
    #   id:
    #   true:
    # netlify:
    #   # Enable CAPTCHA challenge to reduce spam?
    #   captcha: true

  # Contact details (edit or remove options as required)
  # email: matpompili gmail edu
  # phone: 888 888 88 88, 
  # address:
  #   street: 450 Serra Mall
  #   city: Stanford
  #   region: CA
  #   postcode: '94305'
  #   country: United States
  #   country_code: US
  # coordinates:
  #   latitude: '37.4275'
  #   longitude: '-122.1697'
  # directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
  # office_hours:
  #   - 'Monday 10:00 to 13:00'
  #   - 'Wednesday 09:00 to 10:00'
  # appointment_url: 'https://calendly.com'
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: Message me on Twitter
      link: 'https://twitter.com/dr_matteo_laser'
    - icon: linkedin
      icon_pack: fab
      name: Message me on Linkedin
      link: 'https://linkedin.com/in/matteopompili'
  #   - icon: video
  #     icon_pack: fas
  #     name: Zoom Me
  #     link: 'https://zoom.com'

design:
  columns: '2'
---

<div class="mb-3">
  <form name="contact" action="https://formsubmit.co/f6c1f90b5a805f0315b052fae454403f "  method="POST">
    <div class="form-group form-inline">
      <label class="sr-only" for="inputName">Name</label>
      <input type="text" name="name" class="form-control w-100" id="inputName" placeholder="Name" required>
    </div>
    <div class="form-group form-inline">
      <label class="sr-only" for="inputEmail">Email</label>
      <input type="email" name="email" class="form-control w-100" id="inputEmail" placeholder="Email" required>
    </div>
    <div class="form-group">
      <label class="sr-only" for="inputMessage">Message</label>
      <textarea name="message" class="form-control" id="inputMessage" rows="5" placeholder="Message" required></textarea>
    </div>
    <div class="d-none">
      <label>Do not fill this field unless you are a bot: <input type="text" name="_honey">
      <input type="hidden" name="_template" value="box">
    </div>
    <button type="submit" class="btn btn-primary px-3 py-2 w-100">Send</button>
  </form>
</div>
