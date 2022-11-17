# PERN Stack Boilerplate
Boilerplate for a React/Express/PostgreSQL app.

## Quick Start
### Development - Backend
The backend can be launched by running in ``/``:
```bash
$ docker-compose up
```
This runs the backend server on http://localhost:5000.

### Development - Frontend
The frontend can be launched by running in ``/frontend``:
```bash
$ npm run start
```
This runs the frontend server on http://localhost:3000. All requests will be proxied to the backend.

### Deployment
Both the frontend and backend can be deployed by running in ``/``:
```bash
$ docker-compose -f docker-compose-prod.yml up
```
This runs the deployed website on http://localhost:8000.


*Boilerplate inspired in https://github.com/V-Wong/pern-stack-template*
