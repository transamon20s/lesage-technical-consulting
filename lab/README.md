# LeSageTech Cyber Command Center

A static browser-based IT operations playground. Metrics, hosts, and commands are simulated. No real hosts are contacted and no commands are executed on the server.

## Add to existing website without replacing it

1. Download and extract this ZIP.
2. Open the existing GitHub repository `transamon20s/lesage-technical-consulting`.
3. Create a `lab` folder in the repository's deployed site root.
4. Upload `index.html`, `command-center.css`, and `command-center.js` from this package's `lab/` folder into that new folder.
5. Commit to `main` and wait for the existing Azure Static Web Apps GitHub Actions workflow to succeed.
6. Visit `https://www.lesagetech.com/lab/`.

For a standard root-level static site, put `lab/` at the repository root. If the Azure workflow uses a custom `app_location`, put the folder beneath that configured app directory.

## Optional navigation link

Add this to your existing site's navigation without replacing the home page:

```html
<a href="/lab/">Labs</a>
```

## Try it

- Select nodes on the network map.
- Trigger simulated DNS, web-server, access-switch, or CPU incidents.
- Reset the lab to restore the normal state.
- Terminal commands: `help`, `status`, `show servers`, `show network`, `ping gateway`, `nslookup example.com`, `tracert web-srv-01`, `incidents`, `reset dns`, `ipconfig`, and `whoami`.

## Safety

The app is front-end only. It does not ping, scan, or execute commands on real infrastructure. Addresses are reserved documentation examples such as `192.0.2.0/24`, `198.51.100.0/24`, and `203.0.113.0/24`. No credentials or API keys are required. Google Fonts is optional; system fonts are used if it is unavailable.
