⏺ ReplayWeb.page - Web Archive Viewer

  ReplayWeb.page is a browser-based web archive viewer that loads and replays archived web content directly in your
  browser without requiring any server infrastructure.

  Project Overview

  Current Version: 2.3.16License: AGPL-3.0-or-laterRepository: https://github.com/webrecorder/replayweb.pageLive Site:
  https://replayweb.page/

  What It Does

  ReplayWeb.page allows users to view and interact with archived web content from various archive formats including:
  - WARC (.warc, .warc.gz) files
  - WACZ (Web Archive Collection Zipped) files
  - HAR (HTTP Archive) files

  The application runs entirely client-side using a service worker architecture, meaning no data is uploaded to any
  servers and all content stays within your browser.

  Architecture

  Frontend (UI)

  - Built with Lit web components and TypeScript
  - Uses Bulma CSS framework for styling
  - Main entry point: src/index.ts exports all components
  - Core application: src/appmain.ts contains the main ReplayWebApp component

  Backend (Service Worker)

  - Powered by @webrecorder/wabac library (loaded as sw.js)
  - Handles archive loading, parsing, and URL rewriting
  - Enables offline replay of archived content

  Key Components

  - ReplayWebApp (appmain.ts): Main application shell
  - Chooser (chooser.ts): File selection and loading interface
  - Item/Coll (item.ts): Archive collection management
  - Replay (replay.ts): Content replay functionality
  - Pages (pages.ts): Page listing and navigation
  - Embed (embed.ts): Embeddable viewer component

  Deployment Options

  1. Static Website

  - Core files: index.html, sw.js, ui.js
  - Can run on any HTTP server
  - Hosted version available at https://replayweb.page/

  2. Electron Desktop App

  - Cross-platform app for Mac, Windows, Linux
  - Supports file associations for archive formats
  - Built with Electron and available on GitHub releases

  3. NPM Package/Library

  - Available as replaywebpage on npm
  - Can be embedded in other websites
  - Supports various embedding configurations

  4. Documentation Site

  - Built with MkDocs Material
  - Available at https://replayweb.page/docs/
  - Includes user guides and embedding documentation

  Development Setup

  yarn install                # Install dependencies
  yarn start-dev            # Dev server with hot reload (port 9990)
  yarn start-docs           # Build assets + docs dev server
  yarn build                # Production build
  yarn build-docs           # Build full site with docs
  yarn dist                 # Build + Electron app

  Key Technologies

  - Lit - Web components framework
  - TypeScript - Type-safe JavaScript
  - Webpack - Module bundler with multiple build configs
  - @webrecorder/wabac - Web archive replay engine
  - Electron - Desktop app framework
  - Bulma - CSS framework
  - MkDocs - Documentation generator

  Special Features

  - Google Drive Integration: Can load archives directly from Google Drive
  - Embedding Support: Can be embedded in other websites with various configurations
  - Ruffle Integration: Flash content support via Ruffle emulator
  - No Server Required: Fully client-side operation
  - Privacy-First: No data upload, all processing happens locally

  This is a well-architected web archive replay system that successfully bridges the gap between complex archive formats
  and user-friendly web browsing, making archived web content accessible without technical barriers.

