### CI/CD Workflow

### SCM:
- Set up a Git repository in GitLab to manage the source code. Developers push code to feature branches during development and Create PR stable ba\rances like dev, stage, and prod(main) deployment.

### Build Stage:
- Here source code will compile and build and generate `.jar or .war file`
- For Angular, Node.js and Angular CLI are used to build the application

### Automatic versioning:
- We can automate the versioning either in `pacakge.json` angular,  or `pom.xml` for Java application or else we can also use custom functions in the pipeline.

### Unit Testing:
-  After the build stage, the pipeline runs unit tests for both frontend and backend services and provides fast feedback on the correctness of small units of code.
  
### Static Code Analysis:
-  Static analysis tools scan the codebase for potential bugs, security vulnerabilities, coding style violations, and other issues and generate reports to help developers review and fix to pass `Quality gates`

### Artifact:  
- The build outputs, dependencies, and other necessary files are bundled and organized into a deployable artefact package into JFROG.

### Containerization:
- We write `Dockerfile` to containerise the application based on docker images. Containers can run applications across different environments, ensuring reproducibility and scalability.

### Security Scanning: 
- `Trivy scan` is used to analyze the images for security vulnerabilities, potential threats, and compliance issues. This stage helps identify and address security risks before deploying the application.

### Deployment/Delivery: 
- Here, the package application will deploy to the target environment, such as `dev`, `stage` or `prod` and this can be done manually (click) or automatically.

### User Acceptance: 
-  User Acceptance, involves a group of end users or stakeholders testing the application to verify its functionality, usability, and overall suitability for their needs. UAT typically follows predefined test scenarios, use cases, or business workflows to ensure that the application meets the desired objectives.

### Release Management:
- Release management involves coordinating the release of the application to users or customers. It includes activities like versioning, change management, and ensuring a smooth transition to the new release.

### Environment Management: 
- By using configuration management tools like Ansible we can deploy to dev, stage and prod environments.

### Monitoring & Logging: 
- Once the application is deployed, monitoring and logging tools are used to collect and analyze real-time data on the application's performance, usage, and errors to resolve quickly and optimise the application performance.
