# Set up Jenkins
### Using docker-compose
```yaml
version: '2'
services:
  jenkins:
    image: 'jenkins/jenkins'
    container_name: jenkins4dev
    restart: always
    ports:
      - '8080:8080'
      - '50000:50000'
    environment:
      JAVA_OPTS: "-Djava.awt.headless=true"
    volumes:
      - '/data/jenkins/data:/var/jenkins_home'

```

### Quickly
```bash
$ docker-compose up -d
```

### Demo
![alt text](doc/setup_jenkins_dashboard.png)