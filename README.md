# Swagger Static Docs Template

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-brightgreen?logo=github)](https://YOUR_USERNAME.github.io/YOUR_REPO_NAME)
[![OpenAPI 3.0](https://img.shields.io/badge/OpenAPI-3.0-green.svg)](swagger.json)
[![Static Documentation](https://img.shields.io/badge/Docs-Static%20Only-orange)](https://YOUR_USERNAME.github.io/YOUR_REPO_NAME)

A simple template for **hosting static Swagger/OpenAPI documentation** using GitHub Pages.

No backend server required — just replace the `swagger.json` file and push to GitHub. Your interactive API documentation will be automatically deployed and publicly accessible.

> Perfect for projects that want to share API documentation without exposing a live Swagger UI on production servers (for security or cost reasons).

## Demo

After forking and enabling GitHub Pages, your documentation will be available at:

https://YOUR_USERNAME.github.io/YOUR_REPO_NAME

*(Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your actual GitHub username and repository name)*

## How to Use

1. **Fork** this repository to your GitHub account.
2. Replace the `swagger.json` file in the root directory with your own OpenAPI specification.
3. Commit and push the changes to the `main` branch:

```bash
git add swagger.json
git commit -m "Update API documentation"
git push origin main
```
→ GitHub Pages will automatically rebuild and deploy the site within 1–2 minutes.

(First time only) Go to Settings → Pages in your repository:
Select branch main and folder / (root)
Save to enable GitHub Pages.


How to Get swagger.json
1. From a Running API (if Swagger endpoint is exposed)
Open your browser and visit the Swagger JSON endpoint, for example:
texthttp://localhost:5000/swagger/v1/swagger.json
https://api.yourdomain.com/swagger/v1/swagger.json

Press Ctrl + S (Save As) and save the file as swagger.json.
Copy this file into the root of the repository.

2. From an ASP.NET Core Project (using Swashbuckle CLI)
Bash# Install the tool globally (only once)
dotnet tool install -g Swashbuckle.AspNetCore.Cli

# Build your project first
```bash
dotnet build
```

# Export swagger.json (replace DLL path and version as needed)
dotnet swagger tofile --output swagger.json ./bin/Debug/net8.0/YourProject.dll v1
3. From Other Frameworks

NestJS: Access /api/json or use an export tool.
Spring Boot: Access /v3/api-docs and save the JSON.
FastAPI: Access /openapi.json.
Express + swagger-ui-express: Use a custom route or separate tool to export JSON.

Local Preview (Optional)
You can preview the documentation locally without pushing to GitHub:

Simplest way: Double-click and open index.html directly in your browser.
Or use a local server (recommended to avoid CORS issues with Swagger UI):

```bash
Bashnpx serve .
```
# or
```bash
npx http-server .
```
# or
python -m http.server 8000
Then visit: http://localhost:3000 (or the displayed port)
Important Notes

This is static documentation only — the Swagger UI looks fully interactive, but "Try it out" requests will not work (no backend to handle them).
No build or deploy commands are needed beyond a regular git push.
Fully supports OpenAPI 3.0.x with the latest Swagger UI.
For multiple API versions: create files like swagger-v1.json, swagger-v2.json, and modify index.html to add a version selector.
