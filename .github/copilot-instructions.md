# GitHub Copilot Instructions

This repository contains the documentation website for [DataV](https://github.com/DataV-Team/Datav), a Vue data visualization component library for large-screen displays.

## Project Overview

- **Framework**: VuePress 1.x
- **Language**: Chinese (Simplified) documentation
- **Purpose**: Documentation and demo site for the DataV Vue component library
- **Components documented**: BorderBox, Decoration, Charts, ScrollBoard, DigitalFlop, FlylineChart, WaterLevelPond, etc.

## Repository Structure

- `docs/` - VuePress documentation source
  - `.vuepress/` - VuePress configuration and theme
  - `guide/` - Component usage guides
  - `DataV/` - Component API documentation
  - `demo/` - Demo pages
  - `support/` - Support information
- `demo/` - Standalone demo projects
- `deploy/` - Deployment scripts

## Development

- Run `yarn dev` to start the development server (port 5000)
- Run `yarn build` to build the static site
- Run `yarn deploy` to deploy via FTP
