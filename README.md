# LangManus Web UI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> Come From Open Source, Back to Open Source

**The default Web UI for [LangManus](https://github.com/langmanus/langmanus).**

LangManus is a community-driven AI automation framework that builds upon the incredible work of the open source community. Our goal is to combine language models with specialized tools for tasks like web search, crawling, and Python code execution, while giving back to the community that made this possible.

## Demo

![demo](https://github.com/langmanus/langmanus/blob/main/assets/demo.gif?raw=true)

- [View on YouTube](https://youtu.be/sZCHqrQBUGk)

## Table of Contents

- [Quick Start](#quick-start)
- [Docker](#docker)
- [Project Statement](#project-statement)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Quick Start

### Prerequisites

- [LangManus](https://github.com/langmanus/langmanus)
- Node.js (v22.14.0+)
- pnpm (v10.6.2+) as package manager

### Configuration

Create a `.env` file in the project root and configure the following environment variables:

- `NEXT_PUBLIC_API_URL`: The URL of the LangManus API.

It's always a good idea to start with the given example file, and edit the `.env` file with your own values:

```bash
cp .env.example .env
```

### Installation

**IMPORTANT: First, **start the Python server**, see [LangManus](https://github.com/langmanus/langmanus) for more details.**

```bash
# Clone the repository
git clone https://github.com/joerandazzo76/langmanus-web
cd langmanus-web

# Install dependencies
pnpm install

# Run the project in development mode
pnpm dev
```

Then open your browser and navigate to http://localhost:3000

Have fun!

## Docker

You can also run this project with Docker.

First, you need read the [configuration](#configuration) below. Make sure `.env` file is ready.

Second, to build a Docker image of your own web server:

```bash
docker build --build-arg NEXT_PUBLIC_API_URL=YOUR_LANGMANUS_API -t langmanus-web .
```

Final, start up a docker container running the web server:

```bash
# Replace langmanus-web-app with your preferred container name
docker run -d -t -p 3000:3000 --env-file .env --name langmanus-web-app langmanus-web

# stop the server
docker stop langmanus-web-app
```

### Docker Compose

You can also setup this project with the docker compose:

```bash
# building docker image
docker compose build

# start the server
docker compose up
```

## Project Statement

This is an academically driven open-source project, developed by a group of former colleagues in our spare time. It aims to explore and exchange ideas in the fields of Multi-Agent and DeepResearch.

- **Purpose**: The primary purpose of this project is academic research, participation in the GAIA leaderboard, and the future publication of related papers.
- **Independence Statement**: This project is entirely independent and unrelated to our primary job responsibilities. It does not represent the views or positions of our employers or any organizations.
- **No Association**: This project has no association with Manus (whether it refers to a company, organization, or any other entity).
- **Clarification Statement**: We have not promoted this project on any social media platforms. Any inaccurate reports related to this project are not aligned with its academic spirit.
- **Contribution Management**: Issues and PRs will be addressed during our free time and may experience delays. We appreciate your understanding.
- **Disclaimer**: This project is open-sourced under the MIT License. Users assume all risks associated with its use. We disclaim any responsibility for any direct or indirect consequences arising from the use of this project.

## Contributing

We welcome contributions of all kinds! Whether you're fixing a typo, improving documentation, or adding a new feature, your help is appreciated. Please see our [Contributing Guide](CONTRIBUTING.md) for details on how to get started.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

Special thanks to all the open source projects and contributors that make LangManus possible. We stand on the shoulders of giants.
