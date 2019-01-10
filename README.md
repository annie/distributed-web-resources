# Distributed Web Resources
A collection of links and notes about the distributed web

## Links
#### Reading
- [The end of the cloud: A truly serverless web](https://blog.red-badger.com/2017/10/13/the-end-of-the-cloud-a-truly-serverless-web), Red Badger (a digital consultancy)
- [The Decentralized Web (a report)](https://dci.mit.edu/decentralizedweb/), MIT Media Lab
- [Why Decentralization Matters](https://medium.com/s/story/why-decentralization-matters-5e3f79f7638e), Chris Dixon on Medium

#### Technologies
- [Dat protocol](https://datproject.org/): A p2p hypermedia protocol
- [Beaker Browser](https://beakerbrowser.com/): A browser for the distributed
web, with a built-in editor for building web pages. Uses the Dat protocol
- [IPFS](https://ipfs.io): A p2p hypermedia protocol built by Protocol Labs
- [Solid](https://solid.inrupt.com/): A framework for building applications
decoupled from the data layer

#### Organizing
- [Decentralized Web Summit](https://www.decentralizedweb.net/): Conference run
by the Internet Archive
- [NYC Mesh](https://www.nycmesh.net/): DIY community Internet
- [Distributed Web of Care](https://taeyoonchoi.com/soft-care/distributed-web-of-care/):
 An artist-founded research initiative to explore the social potential of the distributed web

## Notes
#### What is the distributed web?
A peer-to-peer model of the Web where data is stored in a distributed way across computers in a network, instead of aggregated in a few huge computers (data centers).

#### Open Questions/Thoughts
- What are the biggest technical problems that have to be solved before a distributed web is viable?
- Could this ever realistically replace the current Web?

#### Notes on [The end of the cloud: A truly serverless web](https://blog.red-badger.com/2017/10/13/the-end-of-the-cloud-a-truly-serverless-web):
- The current state of the Internet
  - A handful of tech giants have essentially monopolized the Web
  - In 2018, Netflix and Youtube accounted for [26% of all Internet traffic in the world](http://fortune.com/2018/10/02/netflix-consumes-15-percent-of-global-internet-bandwidth/)
- Problems with the current state of the Internet
  - *Monopolization of data*
    - Big tech companies store & control huge amounts of user data
    - There is no real transparency into how companies use this data
    - While users ostensibly have control over their own data (i.e. they can deny permissions or delete information), they have no way of verifying that what they requested was done (see all of the 2018 Facebook data scandals)
  - *Storage and bandwidth constraints*
    - As media like HD videos and VR experiences become more and more popular, the volume of data being transmitted across the Internet is increasing
    - Network bandwidth is not growing at a fast enough rate to accommodate this [todo: get source]
- Benefits of a distributed web
  - **People would have direct control over their own data**
  - Less vulnerable to hacks, since there would be no centralized location for a hacker to obtain mass amounts of user data
  - Possibly more efficient usage of Internet bandwidth [todo: investigate further]
- Eliminating the flow of data from user > product
  - > the design of the internet where customers send data to programs owned by businesses is backwards and what we should do instead is send programs to customers to execute on their privately held data that is never directly shared
- Technical implementation
  - One solution is a **content-addressable** system
  - Example: BitTorrent
    - Uses the [Kademlia protocol](https://pdos.csail.mit.edu/~petar/papers/maymounkov-kademlia-lncs.pdf)
    - Files are split up into blocks of data, each with a unique "fingerprint" - a cryptographic hash of the block's content
    - Each computer on the network is given a unique ID that's the same length as the block fingerprints
    - Blocks are stored on the computer with the closest ID
  - > The other interesting property of using a content hash for addressing is that by embedding the id of one block in the content of another, you link the two together in a way that can't be tampered with
