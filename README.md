# PokeFightII_Dockerized
Docker composed version of pokefight 2 to run in your Docker host and play on a web browser.

🔴 Poke Fight II

Poke_Fight_II is a simple game where you can do two player Pok-e-mon battles, via a web app with gifs for the Pok-e-mon!

It is a docker-compose file that combines a MongoDB instance to host the required data as well as store current match data, a script to seed the DB with data, and a Flask app to run the game.

🚀 Features
Flask API served on port 5000

MongoDB seeded with pre-defined data in three collections

Single-command deployment with Docker Compose

Designed for cloud deployment (e.g., AWS EC2)

🧰 Requirements
Docker installed on your machine

📦 Usage
1. Clone the Repo
git clone https://github.com/your-username/pokefight2-docker.git
cd pokefight2-docker

2. CD into the folder

3. Start the App
docker-compose up

This will:
- Pull the official MongoDB image
- Pull the custom pf2 app image from Docker Hub
- Seed the MongoDB instance with required data
- Launch the Flask app on port 5000

🌐 Access the App
Once running, navigate to:
http://your-docker-host-public-ip:5000

⚠️ Make sure your firewall or cloud security group allows traffic on port 5000.

🔐 Networking & Security
The Flask app listens on 0.0.0.0:5000, making it reachable from outside the container.

The MongoDB container is only accessible within the Docker network and not exposed to the public.

For cloud deployments (e.g., EC2):
- Open only port 5000 in your EC2 Security Group
- Restrict access to your own IP address for added security
- Never expose MongoDB directly to the internet

