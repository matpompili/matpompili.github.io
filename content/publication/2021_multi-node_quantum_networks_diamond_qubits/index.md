---
title: 'Multi-Node Quantum Networks with Diamond Qubits'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  
# Author notes (optional)
# author_notes:
#   - 'These authors contributed equally'
#   - 'These authors contributed equally'

date: '2021-12-15T00:00:00Z'
doi: 'https://doi.org/10.4233/uuid:b125ec2d-e2af-4708-bccc-0a2357a533b1'

# Schedule page publish date (NOT publication's date).
publishDate: '2021-12-15T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['7']

# Publication name and optional abbreviated publication name.
publication: PhD Thesis, TUDelft
# publication_short:  PhD Thesis, TUDelft

abstract: >-
  The Internet has revolutionized the way we live. It has enabled applications far beyond what it was originally built for, and it will continue to exceed our expectations for the future. Quantum computers, and the network that will connect them—the Quantum Internet— are likely going to follow the same path. Differently from normal computers, quantum computers can share a property called entanglement, which allows the qubits (quantum bits) to be connected at a much more fundamental level. This property enables a range of new applications that span secure communication to enhanced metrology. Over the past fifteen years, significant progress has been made in connecting rudimentary quantum network nodes via long-distance entanglement. Several quantum platforms have demonstrated entanglement generation between two physically separated qubits. In this thesis we take a significant step forward, both in terms of experimental complexity achieved, and in the abstraction of said complexity for future developments. Moving past two-node experiments required a fundamental redesign of our experimental apparatus, as well as developing the capabilities to control simultaneously the additional node. The first result of this thesis is building a three-node entanglement-based quantum network. We demonstrated distribution of Greenberger-Horne-Zeilinger states over the network, as well as a building block for larger networks: entanglement swapping. Differently from previous multi-node demonstrations, which relied on post-selection, our network is able to perform the entanglement distribution in a heralded fashion: a signal will notify the users that the protocol was successful, and that the state is ready to be used. The second result builds on the first, by adding control over a fifth qubit, improving the quality of the entanglement, and introducing a novel repetitive readout technique, to achieve quantum teleportation of a qubit from the third node to the first—nodes that do not share a direct entanglement channel. The third and final result is the demonstration of entanglement delivery using a quantum network stack. The Internet is built using a plethora of physical platforms: optical fibers, Ethernet cables, Wi-Fi, satellite signals etc. To abstract their functionality, and make applications work regardless of the underlying platform, a layered approach was developed in the 1970s (the Internet protocol). Taking inspiration from classical network stacks, we demonstrate the first two layers of a quantum network stack, the physical layer (where the qubits, lasers and signal generators live), and the link layer, which abstracts the concepts of qubit and entanglement generation such that they can be used by applications at the higher-layers, hiding the complexity of the quantum platform being used.

# Summary. An optional shortened abstract.
#summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags: []

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://research.tudelft.nl/files/102158552/PhD_Thesis_Matteo_Pompili.pdf'
# url_code: 'https://doi.org/10.4121/16912522.v1'
# url_dataset: 'https://doi.org/10.4121/16912522.v1'
# url_poster: ''
# url_project: ''
# url_slides: ''
# url_source: ''
# url_video: 'https://www.youtube.com/watch?v=DRGT5ZgGrEc'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: "Cover of Matteo Pompili's PhD Thesis."
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects:
#   - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---