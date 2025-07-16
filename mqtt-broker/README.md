# AI Data Gateway: MQTT Broker for Advanced Analytics

This project implements an MQTT broker using Eclipse Mosquitto, containerized with Docker. It is designed for managing multiple sensor devices and actuators in a private network environment.

---

## Features

- MQTT broker running in a Docker container
- Supports retained messages for late subscribers
- Logging of all messages to an external SQL database (setup not included)
- MQTT clients (publish/subscribe) examples
- Configurable via mounted config files
- Supports multiple sensors and actuators in a private Wi-Fi network

---

## Getting Started

### Prerequisites

- Docker installed ([Install Docker Desktop](https://docs.docker.com/get-docker/))
- (Optional) WSL2 for Windows users
- Basic knowledge of MQTT and Docker

### Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/mqtt-broker.git
   cd mqtt-broker
2. Review and customize the config/mosquitto.conf file as needed.
3. Start the Mosquitto broker using Docker Compose:
    ```bash
    docker-compose up -d

## Usage

### Publishing a message

```bash
mosquitto_pub -h localhost -t test/topic -m "Hello MQTT"
```
### Subscribing to a topic

```bash
mosquitto_pub -h localhost -t test/topic -m "Hello MQTT"
```

This setup currently does not use username/password authentication.

Make sure your network is secure since authentication is disabled.

For production or public-facing brokers, consider enabling authentication and encryption.
