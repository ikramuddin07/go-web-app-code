# Go Web Application - DevOps Best Practices Showcase

A comprehensive DevOps demonstration project showcasing industry-standard practices for building, testing, and deploying applications using modern DevOps tools and methodologies.

## Project Overview

This project demonstrates end-to-end DevOps practices including containerization, orchestration, infrastructure as code, and automated deployment strategies. The application serves as a simple web platform while the focus remains on implementing DevOps best practices.

## DevOps Features Demonstrated

- **Containerization**: Multi-stage Docker builds with security optimization
- **Orchestration**: Complete Kubernetes deployment manifests
- **Package Management**: Helm charts for standardized deployments
- **Infrastructure as Code**: Declarative configuration management
- **Testing**: Automated testing pipeline integration
- **Security**: Production-ready security practices
- **CI/CD Ready**: Structured for continuous integration/deployment

## Technology Stack

- **Runtime**: Go 1.22.5
- **Containerization**: Docker with multi-stage builds
- **Orchestration**: Kubernetes
- **Package Management**: Helm 3.x
- **Base Image**: Google Distroless (production)
- **Testing**: Go testing framework

## Project Structure

```
go-web-app-code/
├── main.go                 # Application entry point
├── main_test.go           # Unit tests
├── go.mod                 # Go module definition
├── Dockerfile             # Multi-stage Docker build
├── static/                # Static web assets
├── k8s/                   # Kubernetes manifests
│   └── manifests/
│       ├── deployment.yml
│       ├── service.yml
│       └── ingress.yml
└── helm/                  # Helm chart
    └── go-web-app-chart/
        ├── Chart.yaml
        ├── values.yaml
        └── templates/
            ├── deployment.yml
            ├── service.yml
            └── ingress.yml
```

## Quick Start

### Prerequisites

- Go 1.22.5 or later
- Docker
- Kubernetes cluster (for deployment)
- Helm 3.x (for Helm deployment)

### Local Development

```bash
git clone <repository-url>
cd go-web-app-code
go run main.go
```

Access: http://localhost:8080/home

### Running Tests

```bash
go test -v
```

## DevOps Deployment Strategies

### Docker Deployment

**Build optimized container:**
```bash
docker build -t go-web-app:latest .
docker run -p 8080:8080 go-web-app:latest
```

**Key DevOps practices demonstrated:**
- Multi-stage builds for optimized image size
- Distroless base image for security
- Layer caching optimization
- Minimal attack surface

### Kubernetes Deployment

**Using K8s manifests:**
```bash
kubectl apply -f k8s/manifests/
kubectl get pods,services,ingress
```

**Using Helm chart:**
```bash
helm install go-web-app ./helm/go-web-app-chart
helm upgrade go-web-app ./helm/go-web-app-chart
```

## DevOps Best Practices Implemented

### Security
- **Distroless base image**: Minimal attack surface
- **Non-root execution**: Enhanced container security
- **Static compilation**: No runtime dependencies
- **Port exposure**: Only necessary ports exposed

### Performance
- **Optimized container layers**: Efficient caching
- **Minimal image footprint**: Reduced resource usage
- **Efficient resource allocation**: K8s resource limits

### Scalability
- **Stateless design**: Horizontal scaling ready
- **Load balancing**: Kubernetes service integration
- **Rolling updates**: Zero-downtime deployments

### Monitoring & Observability
- **Health check endpoints**: Ready for monitoring
- **Structured logging**: Integration friendly
- **Metrics collection**: Prometheus compatible
- **Standard HTTP responses**: Easy debugging

## Infrastructure as Code

### Kubernetes Manifests
- **Deployment**: Application lifecycle management
- **Service**: Network abstraction and load balancing
- **Ingress**: External access and routing

### Helm Charts
- **Templating**: Environment-specific configurations
- **Versioning**: Release management
- **Dependencies**: Chart composition
- **Values management**: Configuration flexibility

## CI/CD Pipeline Ready

This project structure supports:
- **Automated testing**: Unit test integration
- **Container builds**: Docker image automation
- **Kubernetes deployment**: Manifest application
- **Helm releases**: Chart deployment automation
- **Environment promotion**: Dev/Staging/Production

## Production Deployment Considerations

- **Resource management**: CPU/memory limits configured
- **High availability**: Multi-replica deployments
- **Security policies**: RBAC and network policies ready
- **Backup strategies**: Persistent volume configurations
- **Monitoring integration**: Prometheus/Grafana ready

## DevOps Tools Integration

**Compatible with:**
- **Jenkins**: Pipeline automation
- **GitLab CI**: GitOps workflows
- **GitHub Actions**: Automated testing and deployment
- **ArgoCD**: GitOps deployment
- **Prometheus**: Metrics collection
- **Grafana**: Visualization and alerting

## Contributing

1. Fork the repository
2. Create a feature branch
3. Implement DevOps improvements
4. Add/update tests
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

**Ikramuddin** - DevOps Engineer

---

*This project demonstrates modern DevOps practices including containerization, orchestration, infrastructure as code, and automated deployment strategies.*
