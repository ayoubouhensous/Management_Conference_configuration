# Conference Management System - Configuration Repository

This repository contains the centralized configuration files for the [Conference Management System](https://github.com/ayoubouhensous/Conference_Management_System) microservices application.

## Overview

This configuration repository is used by the **Config Service** (Spring Cloud Config Server) to provide centralized, externalized configuration for all microservices in the Conference Management System.

## Purpose

- Centralized configuration management for all microservices
- Environment-specific configurations (dev, test, production)
- Dynamic configuration updates without service restarts
- Version-controlled configuration tracking

## Main Application Repository

🔗 **[Conference_Management_System](https://github.com/ayoubouhensous/Conference_Management_System)**

This is the configuration repository for the main application. Please refer to the main repository for complete documentation, setup instructions, and application details.

## Configuration Files

This repository contains configuration files for the following services:

- `discovery-service.yml` - Eureka Service Registry configuration
- `gateway-service.yml` - API Gateway configuration  
- `conference-service.yml` - Conference management service configuration
- `keynote-service.yml` - Keynote speaker service configuration
- `application.yml` - Shared configuration across all services

## Usage

The Config Service in the main application is configured to pull configurations from this repository. When each microservice starts, it connects to the Config Service to retrieve its configuration.

### Configuration Format

```yaml
spring:
  application:
    name: service-name
  # Service-specific configurations
```

## Environment Profiles

Configurations can be organized by environment using Spring profiles:

- `application-dev.yml` - Development environment
- `application-test.yml` - Testing environment  
- `application-prod.yml` - Production environment

## Security Note

⚠️ **Important**: This repository should not contain sensitive information like passwords, API keys, or tokens in plain text. Use encrypted properties or environment variables for sensitive data.

## Related Repositories

- **Main Application**: [Conference_Management_System](https://github.com/ayoubouhensous/Conference_Management_System)

