# PokeFightII_Dockerized
Docker composed version of pokefight 2 to run in your Docker host and play on a web browser.

🔴 Pokefight2 – Dockerized Flask + MongoDB App
Pokefight2 is a Flask web app that allows users to simulate Pokémon battles using a custom dataset. This repo contains a docker-compose.yml setup for easily deploying the app alongside a MongoDB instance.

🚀 Features
Flask API served on port 5000

MongoDB seeded with pre-defined data

Single-command deployment with Docker Compose

Designed for cloud deployment (e.g., AWS EC2)

🧰 Requirements
Docker installed on your machine

Docker Compose installed (usually included with Docker Desktop)

📦 Usage
1. Clone the Repo
bash
Copy
Edit
git clone https://github.com/your-username/pokefight2-docker.git
cd pokefight2-docker
2. Start the App
bash
Copy
Edit
docker-compose up
This will:

Pull the official MongoDB image

Pull your custom app image from Docker Hub (if set in the compose file)

Seed the MongoDB instance with required data

Launch the Flask app on port 5000

🌐 Access the App
Once running, navigate to:

cpp
Copy
Edit
http://<your-docker-host-public-ip>:5000
⚠️ Make sure your firewall or cloud security group allows traffic on port 5000.

🔐 Networking & Security
The Flask app listens on 0.0.0.0:5000, making it reachable from outside the container.

The MongoDB container is only accessible within the Docker network and not exposed to the public.

For cloud deployments (e.g., EC2):

Open only port 5000 in your EC2 Security Group

Restrict access to your own IP address for added security

Never expose MongoDB directly to the internet

