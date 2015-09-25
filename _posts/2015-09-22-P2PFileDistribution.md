---
layout: post
title:  "P2P File Distribution"
date:   2015-04-18 08:43:59
author: Adam Casey
categories: university
---

Created for a third-year Computer Science module. We were given the specification to create either a P2P or a Multicast reliable file distribution system. I opted for P2P so it could be used on the open internet without issues.

I followed the original BitTorrent architecture for this practical, one central machine acts as the "swam manager" - directing new peers at existing peers. The rest of the peers connect to each other to download files. A file is split into standard sized chunks (Specified by the metadata file - the ".torrent" file equivalent, 256KB by default)

File transfer is made reliable by checking downloaded chunks against the hashes stored in the metadata file. By using a cryptographic hash, SHA-256 (configurable for future-proofing), this system should also allow for the file to be retrieved from untrusted sources through hash-based chunk/file-verification.

[Check it out on GitHub](https://github.com/adamncasey/CS3102-P2PFileDistribution)