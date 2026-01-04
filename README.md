# Swagger Static Docs Template

This repository is a template for hosting static Swagger (OpenAPI) documentation using GitHub Pages.

It allows you to publish API documentation without running a backend server.

---

## How to Use

1. Fork this repository.
2. Replace `swagger.json` with your own OpenAPI specification.
3. Commit and push the changes.

```bash
git add swagger.json
git commit -m "Update API docs"
git push
```
GitHub Pages will automatically redeploy the site.

---

## Local Preview (Optional)

Open `index.html` directly in a browser  
or run:
```bash
npx serve . 
```
---

## Notes

- This is a documentation-only site.
- API requests cannot be executed from Swagger UI.
- No build or deploy command is required.

--
