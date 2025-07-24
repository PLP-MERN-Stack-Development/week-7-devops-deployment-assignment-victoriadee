[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19976937&assignment_repo_type=AssignmentRepo)

# MERN Stack Application Deployment

This is a full-stack MERN application deployed with CI/CD, monitoring, and best practices.

---

## 🔗 Deployed URLs

- **Frontend**: [https://your-frontend.vercel.app](https://your-frontend.vercel.app)
- **Backend API**: [https://your-backend.onrender.com/api](https://your-backend.onrender.com/api)

---
frontend-ci.yml → Deploys to Netlify

backend-ci.yml → Triggers deploy to Render
## 🚀 Tech Stack

- React (Frontend)
- Express.js (Backend)
- MongoDB Atlas (Database)
- Vercel (Frontend Hosting)
- Render / Railway / Heroku (Backend Hosting)
- GitHub Actions (CI/CD)

---

## 📦 Environment Variables

### Frontend `.env.example`
```env
REACT_APP_API_URL=https://your-backend-api-url.com/api
REACT_APP_ENV=production


Task 1: Preparing the Application for Deployment
React Frontend
✅ Run npm run build to create optimized static assets

✅ Enable code splitting via React.lazy and Suspense for dynamic imports

✅ Use .env.production and .env.development for environment-specific configs

Express.js Backend
✅ Add centralized error handling middleware

✅ Use helmet to secure HTTP headers (app.use(helmet()))

✅ Configure .env and use dotenv for environment configs

✅ Add winston or morgan for structured logging

✅ Use mongoose with poolSize option for connection pooling

MongoDB Setup
✅ Create a MongoDB Atlas cluster

✅ Create dedicated users with scoped permissions (readWrite, etc.)

✅ Enable connection pooling in your mongoose.connect options

🚀 Task 2: Deploying the Backend
✅ Choose Render, Railway, or Heroku and deploy your Express.js backend

✅ Add .env variables in platform dashboard (e.g., MONGODB_URI, PORT)

✅ Connect GitHub repo and enable auto-deploy

✅ (Optional) Configure a custom domain

✅ Enable HTTPS via platform settings or automatic SSL cert

✅ Add platform or 3rd-party monitoring/logging (e.g., LogRocket, New Relic)

🌐 Task 3: Deploying the Frontend
✅ Choose Vercel, Netlify, or GitHub Pages

✅ Set build command: npm run build, and publish directory: build/

✅ Add .env variables like REACT_APP_API_URL

✅ Connect GitHub and enable auto-deploy

✅ Set custom domain (optional)

✅ Ensure HTTPS is enabled

✅ Add caching headers or use a service-worker.js for asset caching

🔄 Task 4: CI/CD Pipeline Setup
✅ Create .github/workflows/ci.yml

✅ Use actions/setup-node, npm install, npm run test, and eslint

✅ Automate build and test with each push/PR

✅ Add deploy steps using CLI tools or platform GitHub integrations

✅ Use separate branches/environments for staging and production

✅ Add rollback mechanism (manual re-deploy, tagged releases, etc.)

🔍 Task 5: Monitoring and Maintenance
✅ Add health check endpoint (e.g., GET /health)

✅ Use uptime monitoring tools (e.g., UptimeRobot)

✅ Add error tracking (e.g., Sentry for frontend + backend)

✅ Monitor performance (Lighthouse, Web Vitals, or New Relic)

✅ Add server metrics monitoring (e.g., PM2, Datadog)

✅ Backup strategy for MongoDB Atlas (daily backups enabled)

✅ Maintain update log and patch routine

✅ Document rollback procedures in the README

Backend .env.example

PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
NODE_ENV=production
🔄 CI/CD Pipeline
CI/CD is implemented using GitHub Actions to run:

Lint checks

Automated tests (if present)

Build checks

📸 Screenshots:

🧪 Monitoring Setup
Health Check: GET /api/health

Uptime Monitoring: UptimeRobot

Error Tracking: Sentry.io

Performance Monitoring: Lighthouse, Web Vitals

🔁 Maintenance Plan
Weekly dependency updates

Daily MongoDB backups via Atlas

Logging using Winston / Render Logs

Documented rollback strategy using previous deploy snapshots

📚 Rollback Strategy
Restore previous working deployment snapshot (Render/Vercel).

Revert GitHub commit that caused the issue.

Redeploy from stable branch.

frontend-ci.yml → Deploys to Netlify

backend-ci.yml → Triggers deploy to Render


