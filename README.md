# Personal Portfolio Website

A modern, responsive personal portfolio website containerized with Docker and deployable to both Azure and AWS through GitHub Actions.
Sample code: https://github.com/codewithsadee/vcard-personal-portfolio

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white)
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=flat&logo=microsoftazure&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=flat&logo=amazon-aws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=flat&logo=githubactions&logoColor=white)

## 📌 Table of Contents
- [Features](#-features)
- [Demo](#-demo)
- [Technologies Used](#-technologies-used)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Deployment](#-deployment)
- [Performance](#-performance)
- [Contributing](#-contributing)
- [License](#-license)

## ✨ Features

- 🎨 Modern and responsive design
- 🐳 Docker containerization
- 🚀 CI/CD with GitHub Actions
- 🌐 Multi-cloud deployment support (Azure & AWS)
- 🔒 SSL/TLS encryption
- 📱 Mobile-first approach
- 🎯 SEO optimized
- 🛡️ Security best practices
- 📊 Performance optimized

## 🎮 Demo

- Live Demo: [Your Portfolio URL](https://your-portfolio-url.com)
- [Screenshots](#) (Coming soon)

## 🛠 Technologies Used

- **Frontend**
  - HTML5
  - CSS3
  - JavaScript (ES6+)
  - Responsive Design
  - Custom Animations

- **DevOps & Deployment**
  - Docker
  - GitHub Actions
  - Azure Web Apps
  - AWS Elastic Beanstalk
  - Nginx

- **Performance & SEO**
  - Image Optimization
  - Lazy Loading
  - Caching Strategies
  - Meta Tags Optimization

## 📁 Project Structure

```bash
portfolio-website/
├── portfolio/
│   └── assets/
│       ├── css/
│       │   └── style.css
│       ├── images/
│       │   ├── avatars/
│       │   ├── blog/
│       │   ├── projects/
│       │   ├── logos/
│       │   └── icons/
│       ├── js/
│       │   └── script.js
│       └── index.html
├── .github/
│   └── workflows/
│       ├── azure-deploy.yml
│       └── aws-deploy.yml
├── nginx/
│   └── nginx.conf
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- Docker Desktop
- Node.js (for development)
- Git
- VS Code (recommended)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/portfolio-website.git
cd portfolio-website
```

2. **Local Development**
```bash
# Start local development server
npm install
npm start
```

3. **Docker Development**
```bash
# Build Docker image
docker build -t portfolio .

# Run container
docker run -d -p 80:80 portfolio
```

### Environment Variables

Create a `.env` file in the root directory:
```env
NODE_ENV=development
AZURE_WEBAPP_NAME=your-webapp-name
AWS_REGION=your-region
```

## 📦 Deployment

### Azure Deployment

1. **Configure Azure CLI**
```bash
az login
az account set --subscription <subscription-id>
```

2. **Deploy using GitHub Actions**
- Add Azure credentials to GitHub secrets
- Push to main branch

### AWS Deployment

1. **Configure AWS CLI**
```bash
aws configure
```

2. **Deploy using GitHub Actions**
- Add AWS credentials to GitHub secrets
- Push to main branch

## 📈 Performance

### Optimizations

- Image compression and optimization
- CSS minification
- JavaScript bundling
- Browser caching
- Gzip compression

### Benchmarks

- Lighthouse Score: [Your Score]/100
- PageSpeed Insights: [Your Score]/100
- GTmetrix Grade: [Your Grade]

## 🔒 Security Features

- HTTPS enforcement
- Security headers
- Content Security Policy
- XSS protection
- CORS policies

## 🛠 Development

### Code Style

```bash
# Run linter
npm run lint

# Format code
npm run format

# Optimize images
npm run optimize:images
```

### Building for Production

```bash
# Build production Docker image
docker build -f Dockerfile.prod -t portfolio:prod .

# Run production build
docker-compose -f docker-compose.prod.yml up -d
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch
```bash
git checkout -b feature/AmazingFeature
```
3. Commit your changes
```bash
git commit -m 'Add some AmazingFeature'
```
4. Push to the branch
```bash
git push origin feature/AmazingFeature
```
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Docker Documentation](https://docs.docker.com/)
- [Azure Documentation](https://docs.microsoft.com/azure/)
- [AWS Documentation](https://docs.aws.amazon.com/)
- [GitHub Actions Documentation](https://docs.github.com/actions)
