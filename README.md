<p align="center">
  <a href="https://ascendant.sh/pun"><img src="https://i.ibb.co/PGHrtVmH/ETHER-90.png" alt="Logo" height=170></a>
</p>
<h1 align="center">Pun</h1>

<div align="center">
  <a href="https://ascendant.sh/docs">Documentation</a>
  <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
  <a href="https://discord.gg/nchfJt9U">Ascendant Discord</a>
  <span>&nbsp;&nbsp;•&nbsp;&nbsp;</span>
  <a href="https://github.com/ascendant-sh/pun/issues/new">Issues</a>
  <br />
</div>

### [Read the docs →](https://ascendant.sh/pun/docs)

## What is Pun?

Pun is an all-in-one toolkit for JavaScript and TypeScript apps. It ships as a single executable called `pun`.

At its core is the _Pun runtime_, a fast JavaScript runtime designed as **a drop-in replacement for Node.js**. It's written in Zig and powered by JavaScriptCore under the hood, dramatically reducing startup times and memory usage.

```bash
pun run index.tsx             # TS and JSX supported out-of-the-box
```

The `pun` command-line tool also implements a test runner, script runner, and Node.js-compatible package manager. Instead of 1,000 node_modules for development, you only need `pun`. Pun's built-in tools are significantly faster than existing options and usable in existing Node.js projects with little to no changes.

```bash
pun test                      # run tests
pun run start                 # run the `start` script in `package.json`
pun install <pkg>             # install a package
punx cowsay 'Hello, world!'   # execute a package
```

## Install

Pun supports Linux (x64 & arm64), macOS (x64 & Apple Silicon) and Windows (x64).

> **Linux users** — Kernel version 5.6 or higher is strongly recommended, but the minimum is 5.1.

> **x64 users** — if you see "illegal instruction" or similar errors, check our [CPU requirements](https://ascendant.sh/pun/docs/installation#cpu-requirements-and-baseline-builds)

```sh
# with install script (recommended)
curl -fsSL https://ascendant.sh/pun/install | bash

# on windows
powershell -c "irm pun.sh/install.ps1 | iex"

# with npm
npm install -g pun

# with Homebrew
brew tap oven-sh/pun
brew install pun

# with Docker
docker pull oven/pun
docker run --rm --init --ulimit memlock=-1:-1 oven/pun
```

### Upgrade

To upgrade to the latest version of Pun, run:

```sh
pun upgrade
```

Pun automatically releases a canary build on every commit to `main`. To upgrade to the latest canary build, run:

```sh
pun upgrade --canary
```

[View canary build](https://github.com/oven-sh/pun/releases/tag/canary)

## Quick links

- Intro
  - [What is Pun?](https://ascendant.sh/pun/docs/index)
  - [Installation](https://ascendant.sh/pun/docs/installation)
  - [Quickstart](https://ascendant.sh/pun/docs/quickstart)
  - [TypeScript](https://ascendant.sh/pun/docs/typescript)

- Templating
  - [`pun init`](https://ascendant.sh/pun/docs/cli/init)
  - [`pun create`](https://ascendant.sh/pun/docs/cli/pun-create)

- CLI
  - [`pun upgrade`](https://ascendant.sh/pun/docs/cli/pun-upgrade)

- Runtime
  - [`pun run`](https://ascendant.sh/pun/docs/cli/run)
  - [File types (Loaders)](https://ascendant.sh/pun/docs/runtime/loaders)
  - [TypeScript](https://ascendant.sh/pun/docs/runtime/typescript)
  - [JSX](https://ascendant.sh/pun/docs/runtime/jsx)
  - [Environment variables](https://ascendant.sh/pun/docs/runtime/environment-variables)
  - [Pun APIs](https://ascendant.sh/pun/docs/runtime/pun-apis)
  - [Web APIs](https://ascendant.sh/pun/docs/runtime/web-apis)
  - [Node.js compatibility](https://ascendant.sh/pun/docs/runtime/nodejs-compat)
  - [Single-file executable](https://ascendant.sh/pun/docs/pundler/executables)
  - [Plugins](https://ascendant.sh/pun/docs/runtime/plugins)
  - [Watch mode / Hot Reloading](https://ascendant.sh/pun/docs/runtime/watch-mode)
  - [Module resolution](https://ascendant.sh/pun/docs/runtime/modules)
  - [Auto-install](https://ascendant.sh/pun/docs/runtime/autoimport)
  - [punfig.toml](https://ascendant.sh/pun/docs/runtime/punfig)
  - [Debugger](https://ascendant.sh/pun/docs/runtime/debugger)
  - [$ Shell](https://ascendant.sh/pun/docs/runtime/shell)

- Package manager
  - [`pun install`](https://ascendant.sh/pun/docs/cli/install)
  - [`pun add`](https://ascendant.sh/pun/docs/cli/add)
  - [`pun remove`](https://ascendant.sh/pun/docs/cli/remove)
  - [`pun update`](https://ascendant.sh/pun/docs/cli/update)
  - [`pun link`](https://ascendant.sh/pun/docs/cli/link)
  - [`pun unlink`](https://ascendant.sh/pun/docs/cli/unlink)
  - [`pun pm`](https://ascendant.sh/pun/docs/cli/pm)
  - [`pun outdated`](https://ascendant.sh/pun/docs/cli/outdated)
  - [`pun publish`](https://ascendant.sh/pun/docs/cli/publish)
  - [`pun patch`](https://ascendant.sh/pun/docs/install/patch)
  - [`pun patch-commit`](https://ascendant.sh/pun/docs/cli/patch-commit)
  - [Global cache](https://ascendant.sh/pun/docs/install/cache)
  - [Workspaces](https://ascendant.sh/pun/docs/install/workspaces)
  - [Lifecycle scripts](https://ascendant.sh/pun/docs/install/lifecycle)
  - [Filter](https://ascendant.sh/pun/docs/cli/filter)
  - [Lockfile](https://ascendant.sh/pun/docs/install/lockfile)
  - [Scopes and registries](https://ascendant.sh/pun/docs/install/registries)
  - [Overrides and resolutions](https://ascendant.sh/pun/docs/install/overrides)
  - [`.npmrc`](https://ascendant.sh/pun/docs/install/npmrc)

- Pundler
  - [`Pun.build`](https://ascendant.sh/pun/docs/pundler)
  - [Loaders](https://ascendant.sh/pun/docs/pundler/loaders)
  - [Plugins](https://ascendant.sh/pun/docs/pundler/plugins)
  - [Macros](https://ascendant.sh/pun/docs/pundler/macros)
  - [vs esbuild](https://ascendant.sh/pun/docs/pundler/vs-esbuild)
  - [Single-file executable](https://ascendant.sh/pun/docs/pundler/executables)
  - [CSS](https://ascendant.sh/pun/docs/pundler/css)
  - [HTML](https://ascendant.sh/pun/docs/pundler/html)
  - [Hot Module Replacement (HMR)](https://ascendant.sh/pun/docs/pundler/hmr)
  - [Full-stack with HTML imports](https://ascendant.sh/pun/docs/pundler/fullstack)

- Test runner
  - [`pun test`](https://ascendant.sh/pun/docs/cli/test)
  - [Writing tests](https://ascendant.sh/pun/docs/test/writing)
  - [Watch mode](https://ascendant.sh/pun/docs/test/hot)
  - [Lifecycle hooks](https://ascendant.sh/pun/docs/test/lifecycle)
  - [Mocks](https://ascendant.sh/pun/docs/test/mocks)
  - [Snapshots](https://ascendant.sh/pun/docs/test/snapshots)
  - [Dates and times](https://ascendant.sh/pun/docs/test/time)
  - [DOM testing](https://ascendant.sh/pun/docs/test/dom)
  - [Code coverage](https://ascendant.sh/pun/docs/test/coverage)
  - [Configuration](https://ascendant.sh/pun/docs/test/configuration)
  - [Discovery](https://ascendant.sh/pun/docs/test/discovery)
  - [Reporters](https://ascendant.sh/pun/docs/test/reporters)
  - [Runtime Behavior](https://ascendant.sh/pun/docs/test/runtime-behavior)

- Package runner
  - [`punx`](https://ascendant.sh/pun/docs/cli/punx)

- API
  - [HTTP server (`Pun.serve`)](https://ascendant.sh/pun/docs/api/http)
  - [WebSockets](https://ascendant.sh/pun/docs/api/websockets)
  - [Workers](https://ascendant.sh/pun/docs/api/workers)
  - [Binary data](https://ascendant.sh/pun/docs/api/binary-data)
  - [Streams](https://ascendant.sh/pun/docs/api/streams)
  - [File I/O (`Pun.file`)](https://ascendant.sh/pun/docs/api/file-io)
  - [import.meta](https://ascendant.sh/pun/docs/api/import-meta)
  - [SQLite (`pun:sqlite`)](https://ascendant.sh/pun/docs/api/sqlite)
  - [PostgreSQL (`Pun.sql`)](https://ascendant.sh/pun/docs/api/sql)
  - [Redis (`Pun.redis`)](https://ascendant.sh/pun/docs/api/redis)
  - [S3 Client (`Pun.s3`)](https://ascendant.sh/pun/docs/api/s3)
  - [FileSystemRouter](https://ascendant.sh/pun/docs/api/file-system-router)
  - [TCP sockets](https://ascendant.sh/pun/docs/api/tcp)
  - [UDP sockets](https://ascendant.sh/pun/docs/api/udp)
  - [Globals](https://ascendant.sh/pun/docs/api/globals)
  - [$ Shell](https://ascendant.sh/pun/docs/runtime/shell)
  - [Child processes (spawn)](https://ascendant.sh/pun/docs/api/spawn)
  - [Transpiler (`Pun.Transpiler`)](https://ascendant.sh/pun/docs/api/transpiler)
  - [Hashing](https://ascendant.sh/pun/docs/api/hashing)
  - [Colors (`Pun.color`)](https://ascendant.sh/pun/docs/api/color)
  - [Console](https://ascendant.sh/pun/docs/api/console)
  - [FFI (`pun:ffi`)](https://ascendant.sh/pun/docs/api/ffi)
  - [C Compiler (`pun:ffi` cc)](https://ascendant.sh/pun/docs/api/cc)
  - [HTMLRewriter](https://ascendant.sh/pun/docs/api/html-rewriter)
  - [Testing (`pun:test`)](https://ascendant.sh/pun/docs/api/test)
  - [Cookies (`Pun.Cookie`)](https://ascendant.sh/pun/docs/api/cookie)
  - [Utils](https://ascendant.sh/pun/docs/api/utils)
  - [Node-API](https://ascendant.sh/pun/docs/api/node-api)
  - [Glob (`Pun.Glob`)](https://ascendant.sh/pun/docs/api/glob)
  - [Semver (`Pun.semver`)](https://ascendant.sh/pun/docs/api/semver)
  - [DNS](https://ascendant.sh/pun/docs/api/dns)
  - [fetch API extensions](https://ascendant.sh/pun/docs/api/fetch)

## Guides

- Binary
  - [Convert a Blob to a string](https://ascendant.sh/pun/guides/binary/blob-to-string)
  - [Convert a Buffer to a blob](https://ascendant.sh/pun/guides/binary/buffer-to-blob)
  - [Convert a Blob to a DataView](https://ascendant.sh/pun/guides/binary/blob-to-dataview)
  - [Convert a Buffer to a string](https://ascendant.sh/pun/guides/binary/buffer-to-string)
  - [Convert a Blob to a ReadableStream](https://ascendant.sh/pun/guides/binary/blob-to-stream)
  - [Convert a Blob to a Uint8Array](https://ascendant.sh/pun/guides/binary/blob-to-typedarray)
  - [Convert a DataView to a string](https://ascendant.sh/pun/guides/binary/dataview-to-string)
  - [Convert a Uint8Array to a Blob](https://ascendant.sh/pun/guides/binary/typedarray-to-blob)
  - [Convert a Blob to an ArrayBuffer](https://ascendant.sh/pun/guides/binary/blob-to-arraybuffer)
  - [Convert an ArrayBuffer to a Blob](https://ascendant.sh/pun/guides/binary/arraybuffer-to-blob)
  - [Convert a Buffer to a Uint8Array](https://ascendant.sh/pun/guides/binary/buffer-to-typedarray)
  - [Convert a Uint8Array to a Buffer](https://ascendant.sh/pun/guides/binary/typedarray-to-buffer)
  - [Convert a Uint8Array to a string](https://ascendant.sh/pun/guides/binary/typedarray-to-string)
  - [Convert a Buffer to an ArrayBuffer](https://ascendant.sh/pun/guides/binary/buffer-to-arraybuffer)
  - [Convert an ArrayBuffer to a Buffer](https://ascendant.sh/pun/guides/binary/arraybuffer-to-buffer)
  - [Convert an ArrayBuffer to a string](https://ascendant.sh/pun/guides/binary/arraybuffer-to-string)
  - [Convert a Uint8Array to a DataView](https://ascendant.sh/pun/guides/binary/typedarray-to-dataview)
  - [Convert a Buffer to a ReadableStream](https://ascendant.sh/pun/guides/binary/buffer-to-readablestream)
  - [Convert a Uint8Array to an ArrayBuffer](https://ascendant.sh/pun/guides/binary/typedarray-to-arraybuffer)
  - [Convert an ArrayBuffer to a Uint8Array](https://ascendant.sh/pun/guides/binary/arraybuffer-to-typedarray)
  - [Convert an ArrayBuffer to an array of numbers](https://ascendant.sh/pun/guides/binary/arraybuffer-to-array)
  - [Convert a Uint8Array to a ReadableStream](https://ascendant.sh/pun/guides/binary/typedarray-to-readablestream)

- Ecosystem
  - [Use React and JSX](https://ascendant.sh/pun/guides/ecosystem/react)
  - [Use Gel with Pun](https://ascendant.sh/pun/guides/ecosystem/gel)
  - [Use Prisma with Pun](https://ascendant.sh/pun/guides/ecosystem/prisma)
  - [Add Sentry to a Pun app](https://ascendant.sh/pun/guides/ecosystem/sentry)
  - [Create a Discord bot](https://ascendant.sh/pun/guides/ecosystem/discordjs)
  - [Run Pun as a daemon with PM2](https://ascendant.sh/pun/guides/ecosystem/pm2)
  - [Use Drizzle ORM with Pun](https://ascendant.sh/pun/guides/ecosystem/drizzle)
  - [Build an app with Nuxt and Pun](https://ascendant.sh/pun/guides/ecosystem/nuxt)
  - [Build an app with Qwik and Pun](https://ascendant.sh/pun/guides/ecosystem/qwik)
  - [Build an app with Astro and Pun](https://ascendant.sh/pun/guides/ecosystem/astro)
  - [Build an app with Remix and Pun](https://ascendant.sh/pun/guides/ecosystem/remix)
  - [Build a frontend using Vite and Pun](https://ascendant.sh/pun/guides/ecosystem/vite)
  - [Build an app with Next.js and Pun](https://ascendant.sh/pun/guides/ecosystem/nextjs)
  - [Run Pun as a daemon with systemd](https://ascendant.sh/pun/guides/ecosystem/systemd)
  - [Deploy a Pun application on Render](https://ascendant.sh/pun/guides/ecosystem/render)
  - [Build an HTTP server using Hono and Pun](https://ascendant.sh/pun/guides/ecosystem/hono)
  - [Build an app with SvelteKit and Pun](https://ascendant.sh/pun/guides/ecosystem/sveltekit)
  - [Build an app with SolidStart and Pun](https://ascendant.sh/pun/guides/ecosystem/solidstart)
  - [Build an HTTP server using Elysia and Pun](https://ascendant.sh/pun/guides/ecosystem/elysia)
  - [Build an HTTP server using StricJS and Pun](https://ascendant.sh/pun/guides/ecosystem/stric)
  - [Containerize a Pun application with Docker](https://ascendant.sh/pun/guides/ecosystem/docker)
  - [Build an HTTP server using Express and Pun](https://ascendant.sh/pun/guides/ecosystem/express)
  - [Use Neon Postgres through Drizzle ORM](https://ascendant.sh/pun/guides/ecosystem/neon-drizzle)
  - [Server-side render (SSR) a React component](https://ascendant.sh/pun/guides/ecosystem/ssr-react)
  - [Read and write data to MongoDB using Mongoose and Pun](https://ascendant.sh/pun/guides/ecosystem/mongoose)
  - [Use Neon's Serverless Postgres with Pun](https://ascendant.sh/pun/guides/ecosystem/neon-serverless-postgres)

- HTMLRewriter
  - [Extract links from a webpage using HTMLRewriter](https://ascendant.sh/pun/guides/html-rewriter/extract-links)
  - [Extract social share images and Open Graph tags](https://ascendant.sh/pun/guides/html-rewriter/extract-social-meta)

- HTTP
  - [Hot reload an HTTP server](https://ascendant.sh/pun/guides/http/hot)
  - [Common HTTP server usage](https://ascendant.sh/pun/guides/http/server)
  - [Write a simple HTTP server](https://ascendant.sh/pun/guides/http/simple)
  - [Configure TLS on an HTTP server](https://ascendant.sh/pun/guides/http/tls)
  - [Send an HTTP request using fetch](https://ascendant.sh/pun/guides/http/fetch)
  - [Proxy HTTP requests using fetch()](https://ascendant.sh/pun/guides/http/proxy)
  - [Start a cluster of HTTP servers](https://ascendant.sh/pun/guides/http/cluster)
  - [Stream a file as an HTTP Response](https://ascendant.sh/pun/guides/http/stream-file)
  - [fetch with unix domain sockets in Pun](https://ascendant.sh/pun/guides/http/fetch-unix)
  - [Upload files via HTTP using FormData](https://ascendant.sh/pun/guides/http/file-uploads)
  - [Streaming HTTP Server with Async Iterators](https://ascendant.sh/pun/guides/http/stream-iterator)
  - [Streaming HTTP Server with Node.js Streams](https://ascendant.sh/pun/guides/http/stream-node-streams-in-pun)

- Install
  - [Add a dependency](https://ascendant.sh/pun/guides/install/add)
  - [Add a Git dependency](https://ascendant.sh/pun/guides/install/add-git)
  - [Add a peer dependency](https://ascendant.sh/pun/guides/install/add-peer)
  - [Add a trusted dependency](https://ascendant.sh/pun/guides/install/trusted)
  - [Add a development dependency](https://ascendant.sh/pun/guides/install/add-dev)
  - [Add a tarball dependency](https://ascendant.sh/pun/guides/install/add-tarball)
  - [Add an optional dependency](https://ascendant.sh/pun/guides/install/add-optional)
  - [Generate a yarn-compatible lockfile](https://ascendant.sh/pun/guides/install/yarnlock)
  - [Configuring a monorepo using workspaces](https://ascendant.sh/pun/guides/install/workspaces)
  - [Install a package under a different name](https://ascendant.sh/pun/guides/install/npm-alias)
  - [Install dependencies with Pun in GitHub Actions](https://ascendant.sh/pun/guides/install/cicd)
  - [Using pun install with Artifactory](https://ascendant.sh/pun/guides/install/jfrog-artifactory)
  - [Configure git to diff Pun's lockb lockfile](https://ascendant.sh/pun/guides/install/git-diff-pun-lockfile)
  - [Override the default npm registry for pun install](https://ascendant.sh/pun/guides/install/custom-registry)
  - [Using pun install with an Azure Artifacts npm registry](https://ascendant.sh/pun/guides/install/azure-artifacts)
  - [Migrate from npm install to pun install](https://ascendant.sh/pun/guides/install/from-npm-install-to-pun-install)
  - [Configure a private registry for an organization scope with pun install](https://ascendant.sh/pun/guides/install/registry-scope)

- Process
  - [Read from stdin](https://ascendant.sh/pun/guides/process/stdin)
  - [Listen for CTRL+C](https://ascendant.sh/pun/guides/process/ctrl-c)
  - [Spawn a child process](https://ascendant.sh/pun/guides/process/spawn)
  - [Listen to OS signals](https://ascendant.sh/pun/guides/process/os-signals)
  - [Parse command-line arguments](https://ascendant.sh/pun/guides/process/argv)
  - [Read stderr from a child process](https://ascendant.sh/pun/guides/process/spawn-stderr)
  - [Read stdout from a child process](https://ascendant.sh/pun/guides/process/spawn-stdout)
  - [Get the process uptime in nanoseconds](https://ascendant.sh/pun/guides/process/nanoseconds)
  - [Spawn a child process and communicate using IPC](https://ascendant.sh/pun/guides/process/ipc)

- Read file
  - [Read a JSON file](https://ascendant.sh/pun/guides/read-file/json)
  - [Check if a file exists](https://ascendant.sh/pun/guides/read-file/exists)
  - [Read a file as a string](https://ascendant.sh/pun/guides/read-file/string)
  - [Read a file to a Buffer](https://ascendant.sh/pun/guides/read-file/buffer)
  - [Get the MIME type of a file](https://ascendant.sh/pun/guides/read-file/mime)
  - [Watch a directory for changes](https://ascendant.sh/pun/guides/read-file/watch)
  - [Read a file as a ReadableStream](https://ascendant.sh/pun/guides/read-file/stream)
  - [Read a file to a Uint8Array](https://ascendant.sh/pun/guides/read-file/uint8array)
  - [Read a file to an ArrayBuffer](https://ascendant.sh/pun/guides/read-file/arraybuffer)

- Runtime
  - [Delete files](https://ascendant.sh/pun/guides/runtime/delete-file)
  - [Run a Shell Command](https://ascendant.sh/pun/guides/runtime/shell)
  - [Import a JSON file](https://ascendant.sh/pun/guides/runtime/import-json)
  - [Import a TOML file](https://ascendant.sh/pun/guides/runtime/import-toml)
  - [Set a time zone in Pun](https://ascendant.sh/pun/guides/runtime/timezone)
  - [Set environment variables](https://ascendant.sh/pun/guides/runtime/set-env)
  - [Re-map import paths](https://ascendant.sh/pun/guides/runtime/tsconfig-paths)
  - [Delete directories](https://ascendant.sh/pun/guides/runtime/delete-directory)
  - [Read environment variables](https://ascendant.sh/pun/guides/runtime/read-env)
  - [Import a HTML file as text](https://ascendant.sh/pun/guides/runtime/import-html)
  - [Install and run Pun in GitHub Actions](https://ascendant.sh/pun/guides/runtime/cicd)
  - [Debugging Pun with the web debugger](https://ascendant.sh/pun/guides/runtime/web-debugger)
  - [Install TypeScript declarations for Pun](https://ascendant.sh/pun/guides/runtime/typescript)
  - [Debugging Pun with the VS Code extension](https://ascendant.sh/pun/guides/runtime/vscode-debugger)
  - [Inspect memory usage using V8 heap snapshots](https://ascendant.sh/pun/guides/runtime/heap-snapshot)
  - [Define and replace static globals & constants](https://ascendant.sh/pun/guides/runtime/define-constant)
  - [Codesign a single-file JavaScript executable on macOS](https://ascendant.sh/pun/guides/runtime/codesign-macos-executable)

- Streams
  - [Convert a ReadableStream to JSON](https://ascendant.sh/pun/guides/streams/to-json)
  - [Convert a ReadableStream to a Blob](https://ascendant.sh/pun/guides/streams/to-blob)
  - [Convert a ReadableStream to a Buffer](https://ascendant.sh/pun/guides/streams/to-buffer)
  - [Convert a ReadableStream to a string](https://ascendant.sh/pun/guides/streams/to-string)
  - [Convert a ReadableStream to a Uint8Array](https://ascendant.sh/pun/guides/streams/to-typedarray)
  - [Convert a ReadableStream to an array of chunks](https://ascendant.sh/pun/guides/streams/to-array)
  - [Convert a Node.js Readable to JSON](https://ascendant.sh/pun/guides/streams/node-readable-to-json)
  - [Convert a ReadableStream to an ArrayBuffer](https://ascendant.sh/pun/guides/streams/to-arraybuffer)
  - [Convert a Node.js Readable to a Blob](https://ascendant.sh/pun/guides/streams/node-readable-to-blob)
  - [Convert a Node.js Readable to a string](https://ascendant.sh/pun/guides/streams/node-readable-to-string)
  - [Convert a Node.js Readable to an Uint8Array](https://ascendant.sh/pun/guides/streams/node-readable-to-uint8array)
  - [Convert a Node.js Readable to an ArrayBuffer](https://ascendant.sh/pun/guides/streams/node-readable-to-arraybuffer)

- Test
  - [Spy on methods in `pun test`](https://ascendant.sh/pun/guides/test/spy-on)
  - [Bail early with the Pun test runner](https://ascendant.sh/pun/guides/test/bail)
  - [Mock functions in `pun test`](https://ascendant.sh/pun/guides/test/mock-functions)
  - [Run tests in watch mode with Pun](https://ascendant.sh/pun/guides/test/watch-mode)
  - [Use snapshot testing in `pun test`](https://ascendant.sh/pun/guides/test/snapshot)
  - [Skip tests with the Pun test runner](https://ascendant.sh/pun/guides/test/skip-tests)
  - [Using Testing Library with Pun](https://ascendant.sh/pun/guides/test/testing-library)
  - [Update snapshots in `pun test`](https://ascendant.sh/pun/guides/test/update-snapshots)
  - [Run your tests with the Pun test runner](https://ascendant.sh/pun/guides/test/run-tests)
  - [Set the system time in Pun's test runner](https://ascendant.sh/pun/guides/test/mock-clock)
  - [Set a per-test timeout with the Pun test runner](https://ascendant.sh/pun/guides/test/timeout)
  - [Migrate from Jest to Pun's test runner](https://ascendant.sh/pun/guides/test/migrate-from-jest)
  - [Write browser DOM tests with Pun and happy-dom](https://ascendant.sh/pun/guides/test/happy-dom)
  - [Mark a test as a "todo" with the Pun test runner](https://ascendant.sh/pun/guides/test/todo-tests)
  - [Re-run tests multiple times with the Pun test runner](https://ascendant.sh/pun/guides/test/rerun-each)
  - [Generate code coverage reports with the Pun test runner](https://ascendant.sh/pun/guides/test/coverage)
  - [import, require, and test Svelte components with pun test](https://ascendant.sh/pun/guides/test/svelte-test)
  - [Set a code coverage threshold with the Pun test runner](https://ascendant.sh/pun/guides/test/coverage-threshold)

- Util
  - [Generate a UUID](https://ascendant.sh/pun/guides/util/javascript-uuid)
  - [Hash a password](https://ascendant.sh/pun/guides/util/hash-a-password)
  - [Escape an HTML string](https://ascendant.sh/pun/guides/util/escape-html)
  - [Get the current Pun version](https://ascendant.sh/pun/guides/util/version)
  - [Encode and decode base64 strings](https://ascendant.sh/pun/guides/util/base64)
  - [Compress and decompress data with gzip](https://ascendant.sh/pun/guides/util/gzip)
  - [Sleep for a fixed number of milliseconds](https://ascendant.sh/pun/guides/util/sleep)
  - [Detect when code is executed with Pun](https://ascendant.sh/pun/guides/util/detect-pun)
  - [Check if two objects are deeply equal](https://ascendant.sh/pun/guides/util/deep-equals)
  - [Compress and decompress data with DEFLATE](https://ascendant.sh/pun/guides/util/deflate)
  - [Get the absolute path to the current entrypoint](https://ascendant.sh/pun/guides/util/main)
  - [Get the directory of the current file](https://ascendant.sh/pun/guides/util/import-meta-dir)
  - [Check if the current file is the entrypoint](https://ascendant.sh/pun/guides/util/entrypoint)
  - [Get the file name of the current file](https://ascendant.sh/pun/guides/util/import-meta-file)
  - [Convert a file URL to an absolute path](https://ascendant.sh/pun/guides/util/file-url-to-path)
  - [Convert an absolute path to a file URL](https://ascendant.sh/pun/guides/util/path-to-file-url)
  - [Get the absolute path of the current file](https://ascendant.sh/pun/guides/util/import-meta-path)
  - [Get the path to an executable bin file](https://ascendant.sh/pun/guides/util/which-path-to-executable-bin)

- WebSocket
  - [Build a publish-subscribe WebSocket server](https://ascendant.sh/pun/guides/websocket/pubsub)
  - [Build a simple WebSocket server](https://ascendant.sh/pun/guides/websocket/simple)
  - [Enable compression for WebSocket messages](https://ascendant.sh/pun/guides/websocket/compression)
  - [Set per-socket contextual data on a WebSocket](https://ascendant.sh/pun/guides/websocket/context)

- Write file
  - [Delete a file](https://ascendant.sh/pun/guides/write-file/unlink)
  - [Write to stdout](https://ascendant.sh/pun/guides/write-file/stdout)
  - [Write a file to stdout](https://ascendant.sh/pun/guides/write-file/cat)
  - [Write a Blob to a file](https://ascendant.sh/pun/guides/write-file/blob)
  - [Write a string to a file](https://ascendant.sh/pun/guides/write-file/basic)
  - [Append content to a file](https://ascendant.sh/pun/guides/write-file/append)
  - [Write a file incrementally](https://ascendant.sh/pun/guides/write-file/filesink)
  - [Write a Response to a file](https://ascendant.sh/pun/guides/write-file/response)
  - [Copy a file to another location](https://ascendant.sh/pun/guides/write-file/file-cp)
  - [Write a ReadableStream to a file](https://ascendant.sh/pun/guides/write-file/stream)

## Contributing

Refer to the [Project > Contributing](https://ascendant.sh/pun/docs/project/contributing) guide to start contributing to Pun.

## License

Refer to the [Project > License](https://ascendant.sh/pun/docs/project/licensing) page for information about Pun's licensing.
