1. Start Nacos using Docker: docker-compose up -d
2. Access Nacos console at http://localhost:8848/nacos (default credentials: nacos/nacos)
  In Nacos console, create a configuration:
  Data ID: nacos-config-demo.yaml
  Group: DEFAULT_GROUP
  Format: YAML
  Content:
  user:
    name: "test user"
3. Run your Spring Boot application and test it:
mvn spring-boot:run
4. Test the configuration by accessing:
http://localhost:8080/config
The application will fetch the configuration from Nacos and display the value. Any changes you make to the configuration in Nacos will be automatically reflected in your application without requiring a restart (thanks to @RefreshScope).
