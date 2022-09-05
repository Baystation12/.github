# Baystation

[Website](https://bay.ss13.me) - [Discord](https://bay.ss13.me/discord)

Hi there. Welcome to Baystation. We're a Space Station 13 server and community, and one of the oldest around. You can [check out our archives](https://github.com/orgs/Baystation12/repositories) if you're looking for something old but, otherwise, here's our current active project list.

---

### [Baystation](https://github.com/Baystation12/Baystation12)

[Wiki](https://github.com/baystation12/arrivals/wiki) - [Issues](https://github.com/baystation12/arrivals/issues)

[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3.0-orange.svg)](https://opensource.org/licenses/AGPL-3.0) [![CodeQL](https://github.com/Baystation12/Baystation12/workflows/CodeQL/badge.svg)](https://github.com/baystation12/Baystation12/actions) [![CI Status](https://github.com/Baystation12/Baystation12/workflows/Run%20Tests/badge.svg)](https://github.com/baystation12/baystation12/actions) [![codebeat badge](https://codebeat.co/badges/8ecb9a34-1bab-4d80-b34d-b16e8b216a03)](https://codebeat.co/projects/github-com-baystation12-baystation12-dev)

The actual space station 13 game server.

---

### [Atlas](https://github.com/Baystation12/Atlas) -- **[View Here](http://atlas.baystation.xyz)**

[Wiki](https://github.com/baystation12/atlas/wiki) - [Issues](https://github.com/baystation12/atlas/issues) - [Projects](https://github.com/baystation12/atlas/projects)

[![License: ISC v3](https://img.shields.io/badge/License-ISC-informational.svg)](https://opensource.org/licenses/ISC) [![CodeQL](https://github.com/Baystation12/atlas/workflows/CodeQL/badge.svg)](https://github.com/baystation12/atlas/actions) [![codebeat badge](https://codebeat.co/badges/daa1d78c-f7f8-4ff8-9ac8-88b13c797eec)](https://codebeat.co/projects/github-com-baystation12-atlas-main)

A map for baystation's narrative world.

In progress.

---

### [Arrivals](https://github.com/Baystation12/Arrivals)

[Wiki](https://github.com/baystation12/arrivals/wiki) - [Issues](https://github.com/baystation12/arrivals/issues) - [Projects](https://github.com/baystation12/arrivals/projects)

[![License: ISC v3](https://img.shields.io/badge/License-ISC-informational.svg)](https://opensource.org/licenses/ISC) [![CodeQL](https://github.com/Baystation12/arrivals/workflows/CodeQL/badge.svg)](https://github.com/baystation12/arrivals/actions) [![codebeat badge](https://codebeat.co/badges/965914c1-fb74-4360-8a18-9fbbd08ae0de)](https://codebeat.co/projects/github-com-baystation12-arrivals-main)

A new joinee greeting and IP trust gateway.

In progress.

---

### [Warden](https://github.com/baystation12/warden)

[Wiki](https://github.com/baystation12/warden/wiki) - [Issues](https://github.com/baystation12/warden/issues) - [Projects](https://github.com/baystation12/warden/projects)

[![License: ISC v3](https://img.shields.io/badge/License-ISC-informational.svg)](https://opensource.org/licenses/ISC) [![CodeQL](https://github.com/Baystation12/warden/workflows/CodeQL/badge.svg)](https://github.com/baystation12/warden/actions) [![codebeat badge](https://codebeat.co/badges/aff3ecf7-e0a9-42c8-864b-ed8c4106f9de)](https://codebeat.co/projects/github-com-baystation12-warden-main)

A packet inspection reverse proxy for the byond protocol.

In progress.

---

### [ExCom](https://github.com/baystation12/excom)

[Wiki](https://github.com/baystation12/excom/wiki) - [Issues](https://github.com/baystation12/excom/issues) - [Projects](https://github.com/baystation12/excom/projects)

[![License: ISC v3](https://img.shields.io/badge/License-ISC-informational.svg)](https://opensource.org/licenses/ISC) [![CodeQL](https://github.com/Baystation12/ExCom/workflows/CodeQL/badge.svg)](https://github.com/baystation12/excom/actions) [![codebeat badge](https://codebeat.co/badges/018ab379-a43e-4f45-a8e8-b1482d5de5d9)](https://codebeat.co/projects/github-com-baystation12-excom-main)

A discord bot for game server integration, with user and administrative commands.

In progress.

---

Right now we're still in testing and sandboxing and, besides the game server, are probably not running exactly what we publish here. When we're in a stable state we'll recommend a setup like this to people who want a stack of security and user integration, although every part will be optional. We include HAProxy in front of everything for its ability to mitigate some kinds of attack. We also recommend making use of your service provider's firewall or mitigation services where available - a protected server is a playable server.

```mermaid
graph TD;
    Internet-->HAProxy;
    HAProxy-->ExCom;
    HAProxy-->Arrivals;
    Warden-->Baystation;
    Arrivals-.->Warden;
    ExCom---Baystation;
    ExCom---Warden;
```
