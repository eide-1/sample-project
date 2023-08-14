# sample-project
A sample project that demonstrates the "ChunkLoadError" when using the app router in a dockerized Next.js SPA with Nginx.

**To run the project in a development environment:**
1. `cd` into the root directory of the project
2. Run the following command (replace <container-name> with your chosen container name):
```
 docker-compose -p <container-name> up --build
```

**To run the project in a production environment:**
1. `cd` into the root directory of the project
2. Run the following command (replace <container-name> with your chosen container name):
```
 docker-compose -p <container-name> --file docker-compose.production.yaml up --build
```

The app router bug can only be observed in a **production** container.

**Steps to Reproduce:**
1. Run the the project in a production environment
2. Click on the "Go to Dynamic Route" button. You will be presented with an application error
3. Right-click anywhere on the webpage and click "Inspect". The browser console will display the "ChunkLoadError"
