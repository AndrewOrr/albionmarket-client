[![CircleCI](https://circleci.com/gh/Regner/albionmarket-client.svg?style=svg)](https://circleci.com/gh/Regner/albionmarket-client) [![Go Report Card](https://goreportcard.com/badge/github.com/Regner/albionmarket-client)](https://goreportcard.com/report/github.com/Regner/albionmarket-client)

# Albion Market - Client
Distributed client for the [Albion Market](https://albion-market.com/)
website.

> A quick note on the legality of this application and if it
ciolates the Terms and Conditions for Albion Online: The Technical
Lead for Sanbox Interactive confirmed that looking at network
packets, but not touching is fine. He confirmed this publicly on
the forums. You can find the post here: https://forum.albiononline.com/index.php/Thread/51604-Is-it-allowed-to-scan-your-internet-trafic-and-pick-up-logs/?postID=512670#post512670

This client monitors local network traffic, identifies UDP packets
that contain market data for Albion Online, and ships the raw JSON
from the market packets off to an ingest server.

The client is not meant to parse the packets any more than what is
required to pull the JSON out of them. Processing the JSON is done
on the ingest server so that if an update is required to parse the
JSON it does not require updating the distributed client.

# Related Projects
- [Albion Market - Backend](https://github.com/Regner/albionmarket-backend/)
- [Albion Market - Frontend](https://github.com/Regner/albionmarket-frontend/)

# Dev Setup

### Mac/Linux Setup
- Install [Glide](https://github.com/Masterminds/glide)
  - Linux or Mac: `curl https://glide.sh/get | sh`
  - Mac with Homebrew: `brew install glide`
- Install dependencies using `glide install`

### Windows Setup
[Windows Setup Guide](building_in_windows.md)

# License
This project, and all contributed code, are licensed under the MIT
License. A copy of the MIT License may be found in the repository.
