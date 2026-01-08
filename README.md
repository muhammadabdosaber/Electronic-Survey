# 📋 Electronic Survey

A multi-part project for building and running an electronic survey platform. The workspace contains a legacy AngularJS front-end, a static/back-end site, and an ASP.NET server/API solution.

**What’s inside**
- 🧭 `FrontEnd/src/` — Front-end app (HTML, JS, CSS, assets). Uses an AngularJS-style structure in `app/` and a `gulp` build.
- 🏗️ `BackEnd/src/` — Static/back-end site and build assets (also has `gulp` tasks).
- ⚙️ `Operation Survey/` — Visual Studio solution with the ASP.NET API and server-side projects (`.csproj`, `Startup.cs`, etc.).

**Quick Start (high level)**

- Front-end (dev):

  ```bash
  cd FrontEnd/src
  # If you want to build with gulp (may require Node 10-14 for gulp v3 compatibility):
  npm install
  gulp
  # or serve quickly without a build:
  python3 -m http.server 9090
  # then open http://localhost:9090/ in your browser (or point to built `dist/`)
  ```

- Back-end (static/build):

  ```bash
  cd BackEnd/src
  npm install
  gulp
  ```

- OperationSurvey API (server):

  - Open `Operation Survey/OperationSurvey.sln` in Visual Studio (recommended on Windows) and run the `OperationSurvey.API` project.
  - If the API targets .NET Core/.NET, you may be able to use `dotnet build` / `dotnet run` from a terminal.

**Important files / entry points**
- `FrontEnd/src/index.html` — main front-end entry.
- `FrontEnd/src/app/core/app.module.js`, `app/core/app.routes.js` — app bootstrap and routes.
- `BackEnd/src/index.html`, `BackEnd/src/gulpFile.js` — static site entry and build.
- `Operation Survey/OperationSurvey.API/Startup.cs` — API startup configuration.

💡 Notes & tips
- The front-end uses an older toolchain (Gulp v3). Newer Node versions can cause compatibility issues with `gulp` — consider using Node v10–14 for running the original `gulp` tasks, or use a simple static server to preview files.
- If you change API hosts/ports, update the front-end API URLs in `FrontEnd/src/app/core/app.config.js`.
- I can help add modern scripts (npm `serve`, `build`), Dockerfiles, or CI config if you want to modernize the repo.

If you’d like, I can also:
- add more developer notes (env vars, typical ports),
- create per-folder READMEs, or
- add a small `Makefile` / `npm` scripts to unify local start commands.

✅ Ready to help next — tell me which part you want to run or modernize.
