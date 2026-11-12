# Budget Tracker PWA

A budget tracking application built with Express, MongoDB, and vanilla JavaScript.

## Requirements

- Node.js >=20.19.0
- npm
- MongoDB

## Installation

```bash
npm ci
```

## Running locally

Start MongoDB, then run:

```bash
npm start
```

The application runs at [http://localhost:3001](http://localhost:3001) by default.

Set `MONGODB_URI` to override the default `mongodb://localhost/budget` connection. Set `PORT` to change the HTTP port.

## Verification

Verified in a clean source copy without preinstalled dependencies or environment files, using Node.js 26.7.0, npm 11.19.0, and a disposable local MongoDB 8.0.12 instance:

- `npm ci` completed successfully without changing the lockfile.
- JavaScript syntax checks passed for the server, routes, model, and browser transaction script.
- `npm start` connected to the isolated database on port 27028 before listening on HTTP port 3002.
- The homepage and transaction-list endpoint returned HTTP 200.
- Creating a synthetic transaction returned HTTP 200, and a subsequent GET retrieved the saved transaction.
- Both verification processes were stopped afterward; the existing local database was not used.

There is currently no automated test suite. The existing `npm test` command is a starter placeholder and was confirmed to exit with status 1, not passing test coverage.