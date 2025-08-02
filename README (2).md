# 💰 Rails Budget App (Dockerized)

This is a simple Ruby on Rails app to manage personal budgets with categories and records, containerized using Docker.

---

## 🚀 What I Did

- Launched an EC2 instance on AWS (Ubuntu).
- SSH-ed into the instance:
  ```bash
  ssh -i <your-key.pem> ubuntu@<your-ec2-public-ip>


## Cloned this repo and checked out the app branch:


git clone https://github.com/Harshitha-2003-4/Rails-budget-app.git

cd Rails-budget-app

git checkout app

## Installed Docker and Docker Compose.

## 🐳 Running the App


docker-compose build

docker-compose run web rails db:create db:migrate

docker-compose up

Visit the app at: http://<your-ec2-public-ip>:3000


## 📝 Notes


PostgreSQL is used as the database.

Entry point handled via entrypoint.sh.

Dockerized setup includes:

Dockerfile

docker-compose.yml

config/database.yml


## ✅ Add Sample Category in Rails Console

docker-compose run web rails console


user = User.first
Category.create!(name: "Groceries", user_id: user.id)
