## GitHub Pages Test Setup

This workspace now includes a `docs` folder ready for GitHub Pages.

Files prepared:

- `docs/gravimon_radar.json`
- `docs/index.html`

### Publish steps

1. Create a new public GitHub repository.
2. Upload the contents of this workspace, including the `docs` folder.
3. In the repository settings, open **Pages**.
4. Set the source to **Deploy from a branch**.
5. Choose the `main` branch and the `/docs` folder.
6. Save and wait for the site to publish.

### Expected URL pattern

The direct JSON URL for ArcGIS Velocity will be:

`https://<github-username>.github.io/<repo-name>/gravimon_radar.json`

### ArcGIS Velocity feed settings

- Feed type: HTTP Poller
- HTTP method: GET
- Authentication: None
- URL: the published JSON URL above
- Data format: JSON or GeoJSON, depending on how Velocity detects the payload during configuration

### Notes

- The hosted file is a static test artifact.
- Repeated polling will request the same dataset until the file is replaced.
- Keep the response size under Velocity's recommended limits.