# Docker Portfolio Website

A containerized personal portfolio website with automated deployment to Azure and AWS using GitHub Actions.
Forked from VCard https://github.com/codewithsadee/vcard-personal-portfolio

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white)
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=flat&logo=microsoftazure&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=flat&logo=amazon-aws&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=flat&logo=githubactions&logoColor=white)

## 🚀 Features

- Responsive portfolio website
- Docker containerization
- SSL/TLS encryption
- CI/CD with GitHub Actions
- Multi-cloud deployment (Azure & AWS)
- Nginx web server
- Security best practices
- Performance optimization

## 📋 Prerequisites

- Docker Desktop
- Git
- Node.js (for local development)
- Azure CLI
- AWS CLI
- GitHub account

## 🛠️ Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/portfolio-docker.git
cd portfolio-docker
```

2. **Build the Docker image**
```bash
docker build -t portfolio .
```

3. **Run locally**
```bash
docker run -d -p 80:80 portfolio
```

## 🌐 Deployment

### Azure Deployment

1. **Set up Azure resources**
```bash
# Login to Azure
az login

# Create resource group
az group create --name portfolio-rg --location eastus

# Create container registry
az acr create --resource-group portfolio-rg --name <registry-name> --sku Basic
```

2. **Deploy using GitHub Actions**
- Add required secrets to your GitHub repository
- Push to main branch to trigger deployment

### AWS Deployment

1. **Set up AWS resources**
```bash
# Configure AWS CLI
aws configure

# Create ECR repository
aws ecr create-repository --repository-name portfolio
```

2. **Deploy using GitHub Actions**
- Add AWS credentials to GitHub secrets
- Push to main branch to trigger deployment

## 🔧 Configuration

### Environment Variables

```env
# Azure
AZURE_CREDENTIALS=<your-azure-credentials>
REGISTRY_USERNAME=<acr-username>
REGISTRY_PASSWORD=<acr-password>

# AWS
AWS_ACCESS_KEY_ID=<your-access-key>
AWS_SECRET_ACCESS_KEY=<your-secret-key>
```

### Nginx Configuration

The default Nginx configuration is located in `nginx.conf`. Modify this file to adjust:
- SSL settings
- Cache control
- Security headers
- Performance optimizations

## 📁 Project Structure

```
portfolio-docker/
├── .github/
│   └── workflows/
│       ├── azure-deploy.yml
│       └── aws-deploy.yml
├── portfolio/
│   ├── index.html
│   ├── css/
│   └── js/
├── Dockerfile
├── nginx.conf
├── .dockerignore
└── README.md
```

## 🔒 Security

- HTTPS enabled by default
- Security headers configured
- Regular security updates
- Docker best practices implemented
- WAF protection available

## 💻 Development

1. **Local Development**
```bash
# Start development server
npm install
npm start

# Build for production
npm run build
```

2. **Docker Development**
```bash
# Build with development configuration
docker build -t portfolio:dev -f Dockerfile.dev .

# Run with volume mount for live updates
docker run -v ${PWD}/portfolio:/usr/share/nginx/html -p 80:80 portfolio:dev
```

## 📈 Performance Optimization

- Nginx caching enabled
- Gzip compression
- Image optimization
- CSS/JS minification
- Browser caching headers

## 🔍 Monitoring

### Azure
- Application Insights enabled
- Performance metrics
- Log analytics
- Availability monitoring

### AWS
- CloudWatch metrics
- Health checks
- Log monitoring
- Performance tracking

## 🚧 Troubleshooting

### Common Issues

1. **Docker Build Fails**
```bash
# Clean Docker cache
docker system prune -a
```

2. **Deployment Issues**
```bash
# Check Azure logs
az webapp log tail

# Check AWS logs
aws elasticbeanstalk retrieve-environment-info
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support, email your-email@example.com or create an issue in the repository.

## 🙏 Acknowledgments

- [Docker Documentation](https://docs.docker.com/)
- [Azure Documentation](https://docs.microsoft.com/azure/)
- [AWS Documentation](https://docs.aws.amazon.com/)
- [GitHub Actions Documentation](https://docs.github.com/actions)
