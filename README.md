# backstage-example
Consider whether Backstage can be used for development.

### Create My Backstage App.
```bash
node ➜ /workspaces/backstage-example (main) $ npx @backstage/create-app@latest
Need to install the following packages:
  @backstage/create-app@0.5.2
Ok to proceed? (y) y
? Enter a name for the app [required] backstage

Creating the app...

 Checking if the directory is available:
  checking      backstage ✔ 

 Creating a temporary app directory:
  creating      temporary directory ✔ 

 Preparing files:
  copying       .dockerignore ✔ 
  templating    .gitignore.hbs ✔ 
  copying       .prettierignore ✔ 
  templating    .eslintrc.js.hbs ✔ 
  copying       README.md ✔ 
  copying       app-config.local.yaml ✔ 
  copying       app-config.production.yaml ✔ 
  templating    app-config.yaml.hbs ✔ 
  templating    backstage.json.hbs ✔ 
  templating    catalog-info.yaml.hbs ✔ 
  copying       lerna.json ✔ 
  templating    package.json.hbs ✔ 
  copying       tsconfig.json ✔ 
  copying       yarn.lock ✔ 
  copying       README.md ✔ 
  copying       entities.yaml ✔ 
  copying       org.yaml ✔ 
  copying       template.yaml ✔ 
  copying       catalog-info.yaml ✔ 
  copying       index.js ✔ 
  copying       package.json ✔ 
  copying       README.md ✔ 
  templating    .eslintrc.js.hbs ✔ 
  copying       Dockerfile ✔ 
  copying       README.md ✔ 
  templating    package.json.hbs ✔ 
  copying       index.test.ts ✔ 
  copying       index.ts ✔ 
  copying       types.ts ✔ 
  copying       auth.ts ✔ 
  copying       catalog.ts ✔ 
  copying       proxy.ts ✔ 
  copying       scaffolder.ts ✔ 
  templating    search.ts.hbs ✔ 
  copying       techdocs.ts ✔ 
  copying       app.ts ✔ 
  copying       .eslintignore ✔ 
  templating    .eslintrc.js.hbs ✔ 
  templating    package.json.hbs ✔ 
  copying       cypress.json ✔ 
  copying       android-chrome-192x192.png ✔ 
  copying       apple-touch-icon.png ✔ 
  copying       favicon-16x16.png ✔ 
  copying       favicon.ico ✔ 
  copying       index.html ✔ 
  copying       favicon-32x32.png ✔ 
  copying       manifest.json ✔ 
  copying       robots.txt ✔ 
  copying       safari-pinned-tab.svg ✔ 
  copying       .eslintrc.json ✔ 
  copying       app.js ✔ 
  copying       App.tsx ✔ 
  copying       App.test.tsx ✔ 
  copying       apis.ts ✔ 
  copying       index.tsx ✔ 
  copying       setupTests.ts ✔ 
  copying       SearchPage.tsx ✔ 
  copying       LogoFull.tsx ✔ 
  copying       LogoIcon.tsx ✔ 
  copying       Root.tsx ✔ 
  copying       index.ts ✔ 
  copying       EntityPage.tsx ✔ 

 Moving to final location:
  moving        backstage ✔ 

 Installing dependencies:
  determining   yarn version ✔ 
  executing     yarn install ✔ 
  executing     yarn tsc ✔ 

🥇  Successfully created backstage


 All set! Now you might want to:
  Run the app: cd backstage && yarn dev
  Set up the software catalog: https://backstage.io/docs/features/software-catalog/configuration
  Add authentication: https://backstage.io/docs/auth/

npm notice 
npm notice New minor version of npm available! 9.5.1 -> 9.8.0
npm notice Changelog: https://github.com/npm/cli/releases/tag/v9.8.0
npm notice Run npm install -g npm@9.8.0 to update!
npm notice 
node ➜ /workspaces/backstage-example (main) $ 
```

### Run the Backstage app.
```bash
node ➜ /workspaces/backstage-example (main) $ cd backstage/
node ➜ /workspaces/backstage-example/backstage (main) $ yarn dev
yarn run v1.22.19
$ concurrently "yarn start" "yarn start-backend"
$ yarn workspace app start
$ yarn workspace backend start
$ backstage-cli package start
$ backstage-cli package start
[1] Build succeeded
```

### Add PostgreSQL.
```bash
yarn add --cwd packages/backend pg
```

### Add Authentication.
```bash
node ➜ /workspaces/backstage-example/backstage (main) $ export AUTH_GITHUB_CLIENT_ID=01234567890123456789
node ➜ /workspaces/backstage-example/backstage (main) $ export AUTH_GITHUB_CLIENT_SECRET=0123456789012345678901234567890123456789
node ➜ /workspaces/backstage-example/backstage (main) $ echo $AUTH_GITHUB_CLIENT_ID
node ➜ /workspaces/backstage-example/backstage (main) $ echo $AUTH_GITHUB_CLIENT_SECRET
```