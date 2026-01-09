# Nextflix 
A simple Netflix Clone made using [Next.js](https://nextjs.org/) ⚡

Currently, I have implemented the basic UI with media details fetch functionality.


Deployed it using vercel [here](https://nextflix-azure.vercel.app/).

Please leave a ⭐ as motivation if you liked the implementation 😄


## Demo
![Demo](/public/assets/demo.gif)
<br />
<br />

## Built With

- Next.js
- TypeScript
- Sass
- TMDB API

---

## Running the Project Locally

This is a Next.js project bootstrapped with create-next-app.

In the project directory, you can run:

yarn install  
yarn start  

The app runs in development mode.  
Open http://localhost:3000 to view it in the browser.

---

## AWS Deployment (DevOps Implementation)

This repository was used as part of a **cost-optimised AWS deployment project**, where the application was containerised and deployed on AWS EC2 using Docker.
The goal was to demonstrate a **simple, secure, and low-cost deployment strategy**, avoiding unnecessary managed services.

### Live Demo (Time-Bound)
http://nnamdidevops.uk:3000  
(Demo was intentionally deployed for a short duration to minimise cost)

---

## Deployment Architecture

User  
→ GoDaddy DNS  
→ AWS EC2  
→ Docker Container (Next.js app)

### Key Characteristics

- Single EC2 instance
- Dockerised application
- No CI/CD pipeline (intentional)
- No Load Balancer
- No Elastic IP
- No ECS or EKS

This architecture was chosen to minimise operational overhead and cloud costs while remaining production-viable for demos and MVPs.

---

## Technologies Used (Deployment)

- AWS EC2 (Linux)
- Docker
- Git (Private Repository)
- Shell scripting
- GoDaddy DNS
- Linux server administration

---

## Security Configuration

- Security Groups configured to allow only required inbound ports
- SSH access restricted to key-based authentication
- No secrets committed to the repository
- Application isolated using Docker containers
- Minimal AWS footprint to reduce attack surface

---

## Cost Breakdown (5 Days)

- EC2 (t2/t3.micro): ~£0.96 – £1.20
- EBS storage: ~£0.10 – £0.15
- Data transfer: ~£0.00 – £0.30

Total cost: approximately £1–£2 for 5 days

Cost optimisations applied:
- No Load Balancer
- No Elastic IP
- No Route 53 hosted zone
- No NAT Gateway
- No CI/CD compute costs

---

## Key Learnings

- Docker provides a lightweight and portable runtime for frontend applications
- Not all workloads require managed container services
- Cloud cost optimisation starts with architecture decisions
- Simple infrastructure can be effective when scoped correctly

---

## Future Improvements

- Add HTTPS using ALB + ACM or Nginx with Let’s Encrypt
- Introduce basic monitoring and logging
- Implement blue-green deployment
- Add CI/CD if deployment frequency increases
- Scale horizontally if traffic demands it

---

## Notes

This project focuses on **infrastructure and deployment strategy** rather than application development.  
The application code itself was not modified beyond containerisation and runtime configuration.



