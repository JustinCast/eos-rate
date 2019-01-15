<p align="center">
	<a href="https://travis-ci.org/eoscostarica/rate.eoscostarica.io">
		<img src="https://travis-ci.org/eoscostarica/rate.eoscostarica.io.svg?branch=master" alt="TravisCI">
	</a>
	<a href="http://standardjs.com">
		<img src="https://img.shields.io/badge/code%20style-standard-brightgreen.svg" alt="StandardJS">
	</a>
	<a href="https://git.io/col">
		<img src="https://img.shields.io/badge/%E2%9C%93-collaborative_etiquette-brightgreen.svg" alt="Collaborative Etiquette">
	</a>
	<a href="https://discord.gg/bBpQHym">
		<img src="https://img.shields.io/discord/447118387118735380.svg?logo=discord" alt="chat on Discord">
	</a>
	<a href="https://twitter.com/intent/follow?screen_name=eoscostarica">
		<img src="https://img.shields.io/twitter/follow/eoscostarica.svg?style=social&logo=twitter" alt="follow on Twitter">
	</a>
	<a href="#">
		<img src="https://img.shields.io/dub/l/vibe-d.svg" alt="MIT">
	</a>
</p>

<p align="center">
	<img src="docs/eosrate-logo-black.png" width="600">
</p>

# A Rating System and Voting Portal for the EOS Community

EOS Rate is a community-driven visual rating tool that allows EOS token holders to easily rate Block Producers in distinct categories.

The rating system is based on a radial graph representing the most important qualitative aspects (let’s call them categories) of a block producer, populated with ratings provided by the input if the EOS community, and stored on the blockchain.

It will also provide basic quantitative information, a compare tool, dynamic filtering and links related to each BP (block producer), in order to fully inform the potential voter, but also let them share their ratings.

Each EOS account can submit their rating for each BP as many times as they like facilitating a "liquid democracy", however, the weighting is independent from the amount the EOS account holds. One account = one submission of equal weight.

It will support proxy profile pages and voting.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Feature Roadmap](#feature-roadmap)
- [Prototypes and Assets](#prototypes-and-assets)
- [User Flow](#user-flow)
- [Architecture](#architecture)
- [Development Setup](#development-setup)
  - [Global Dependencies](#global-dependencies)
  - [Run EOS Rate on your Computer](#run-eos-rate-on-your-computer)
- [Contributing](#contributing)
- [About EOS Costa Rica](#about-eos-costa-rica)
- [License](#license)
- [Contributors](#contributors)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Feature Roadmap

**Version 1.0**

- List and Search Block Producers.
- Scatter and Lynx Integration.
- Autogenerated Block Producer profile pages based on information from [eosio.system](https://github.com/EOSIO/eos/tree/master/contracts/eosio.system) containing:
  - Information from the [producerjson](https://github.com/greymass/producerjson) contract.
  - Community ratings results.
  - Rating UI for token holders to rate that block producer.
- Compare Block Producers page:
  - Ability to superpose different BPs ratings flake charts.
- Home page with explanation and instructions.
- Languages: English & Spanish.

**Version 1.2**

- Ability to Vote for a block producer directly on their profile page.
- Add comments when rating. ( review, like Yelp )
- Languages: Chinese and Korean.
- Filtering Block Producer List
  - by Strengths: transparency, community, infrastructure, testnets, tooling.
  - by Region.

**Version 1.3**

- List and search proxies.
- Proxies landing page with:
  - Proxy list from the [eosio.system](https://github.com/EOSIO/eos/tree/master/contracts/eosio.system) voters tables.
  - Proxy Info from the [eos-proxyinfo](https://github.com/AlohaEOS/eos-proxyinfo) contract.
  - Ability to vote for the proxy.

**Version 1.4**

- Filtering proxies list. ( tbd which attributes will be used for filtering )
- Ability to vote for multiple producers at the same from the BP Comparison tool.

**Version 1.5**

- Earn tokens by rating. ( maybe something like Karma )
- Server Side Rendering

## Prototypes and Assets

https://scene.zeplin.io/project/5a58ea3341f76658994e000c

![](docs/eosrate-scenes.png)

## User Flow

![](docs/EOSRate-UserFlow.png)

## Architecture

This project is based on [EOS DApp Boilerplate](https://github.com/eoscostarica/eos-dapp-boilerplate).  
Please reads it's documentation. There's no need to install anything as this repo already contains everything.

<p align="center">
	<img src="docs/architecture.png" width="600">
</p>

## Development Setup

Basic knowledge about Docker, Docker Compose, EOSIO and NodeJS is required.

- Video tutorial [Docker Containers | Learn Docker Basics in 30 Mins](https://www.youtube.com/watch?v=0kwXLcwUw0Q)

### Global Dependencies

- EOS Local https://github.com/eoscostarica/eos-local.
- Docker https://docs.docker.com/install/.  
  At least 10GB RAM (Docker -> Preferences -> Advanced -> Memory -> 10GB or above)
- Hasura CLI https://docs.hasura.io/1.0/graphql/manual/hasura-cli/install-hasura-cli.html
- EOSIO Binaries https://github.com/eosio/eos.  
  This will allow you to `cleos` and `koesd` directly on host machine.
- EOSIO.CDT https://github.com/eosio/eosio.cdt.  
  This will allow you to compile the contracts directly on host machine.

### Run EOS Rate on your Computer

```
git clone git@github.com:eoscostarica/eos-rate.git
cd eos-rate
make start
```

## Contributing

We use a Kanban-style board. That's were we prioritize the work. [Go to Project Board](https://github.com/eoscostarica/eos-rate/projects/1).

The main communication channels are [github issues](https://github.com/eoscostarica/eos-rate/issues) and [EOS Costa Rica's Discord server](https://eoscostarica.io/discord).

Our weekly sync call is every Monday 1:00 AM UTC. [meet.eoscostarica.io](https:/meet.eoscostarica.io).

Contributing Guidelines https://developers.eoscostarica.io/docs/open-source-guidelines.

Please report bugs big and small by [opening an issue](https://github.com/eoscostarica/eos-rate/issues)

## About EOS Costa Rica

<p align="center">
	<a href="https://eoscostarica.io">
		<img src="https://cdn.rawgit.com/eoscostarica/assets/574d20a6/logos/eoscolors-transparent.png" width="300">
	</a>
</p>
<br/>
EOS Costa Rica is an independently-owned, self-funded, bare-metal Genesis block producer that provides stable and secure infrastructure for EOSIO blockchains.  We support open source software for our community while offering enterprise solutions and custom smart contract development for our clients.

[eoscostarica.io](https://eoscostarica.io)

## License

MIT © [EOS Costa Rica](https://eoscostarica.io)

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars0.githubusercontent.com/u/391270?v=4" width="100px;"/><br /><sub><b>Gabo Esquivel</b></sub>](https://gaboesquivel.com)<br />[🤔](#ideas-gaboesquivel "Ideas, Planning, & Feedback") [📖](https://github.com/eoscostarica/eosrate/commits?author=gaboesquivel "Documentation") [💻](https://github.com/eoscostarica/eosrate/commits?author=gaboesquivel "Code") [👀](#review-gaboesquivel "Reviewed Pull Requests") | [<img src="https://avatars1.githubusercontent.com/u/1179619?v=4" width="100px;"/><br /><sub><b>Jorge Murillo</b></sub>](https://github.com/murillojorge)<br />[🤔](#ideas-murillojorge "Ideas, Planning, & Feedback") [📖](https://github.com/eoscostarica/eosrate/commits?author=murillojorge "Documentation") [🎨](#design-murillojorge "Design") [💻](https://github.com/eoscostarica/eosrate/commits?author=murillojorge "Code") [👀](#review-murillojorge "Reviewed Pull Requests") | [<img src="https://avatars2.githubusercontent.com/u/349542?v=4" width="100px;"/><br /><sub><b>Daniel Prado</b></sub>](https://github.com/danazkari)<br />[💻](https://github.com/eoscostarica/eosrate/commits?author=danazkari "Code") [📖](https://github.com/eoscostarica/eosrate/commits?author=danazkari "Documentation") [🤔](#ideas-danazkari "Ideas, Planning, & Feedback") [👀](#review-danazkari "Reviewed Pull Requests") | [<img src="https://avatars0.githubusercontent.com/u/5632966?v=4" width="100px;"/><br /><sub><b>Xavier Fernandez</b></sub>](https://github.com/xavier506)<br />[🤔](#ideas-xavier506 "Ideas, Planning, & Feedback") [📝](#blog-xavier506 "Blogposts") [📢](#talk-xavier506 "Talks") [🚇](#infra-xavier506 "Infrastructure (Hosting, Build-Tools, etc)") | [<img src="https://avatars2.githubusercontent.com/u/40245170?v=4" width="100px;"/><br /><sub><b>Edgar Fernandez</b></sub>](http://www.eoscostarica.io)<br />[🤔](#ideas-edgar-eoscostarica "Ideas, Planning, & Feedback") [📝](#blog-edgar-eoscostarica "Blogposts") [📢](#talk-edgar-eoscostarica "Talks") | [<img src="https://avatars2.githubusercontent.com/u/13205620?v=4" width="100px;"/><br /><sub><b>Rubén Abarca Navarro</b></sub>](https://github.com/rubenabix)<br />[🤔](#ideas-rubenabix "Ideas, Planning, & Feedback") [💻](https://github.com/eoscostarica/eosrate/commits?author=rubenabix "Code") [👀](#review-rubenabix "Reviewed Pull Requests") | [<img src="https://avatars1.githubusercontent.com/u/40480825?v=4" width="100px;"/><br /><sub><b>roafroaf</b></sub>](https://github.com/roafroaf)<br />[🤔](#ideas-roafroaf "Ideas, Planning, & Feedback") [🎨](#design-roafroaf "Design") |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [<img src="https://avatars1.githubusercontent.com/u/8497609?v=4" width="100px;"/><br /><sub><b>Cristian Ramírez</b></sub>](https://github.com/cristian-ramirez)<br />[💻](https://github.com/eoscostarica/eosrate/commits?author=cristian-ramirez "Code") |

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!
