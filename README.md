# SolarThing Grafana
A Grafana Panel that can communicate with SolarThing REST

### Goals
* Communicate with SolarThing REST
* 

### Development Setup
* See below
* Install `nvm` on your machine
  * If you're having trouble installing or using, make sure to use `bash` or a common shell
  * Run `nvm install 14.0 && nvm use 14.0 && nvm alias default 14.0`
    * I don't recommend versions other than 14. I tested 16, and couldn't get it to work
  * WebStorm or your IDE may default to using `/usr/bin/node`, so make sure to change it if you need to
    * "Language & Frameworks" -> "Node.js and NPM"
* Running Grafana in docker: With your current working directory as this folder,
  * `docker run -d -p 3000:3000 -v "$(pwd)":/var/lib/grafana/plugins/solarthing-grafana --name=grafana-solarthing-grafana grafana/grafana:7.0.0`
  * `yarn dev`
  * `docker restart grafana-solarthing-grafana`
  * Password admin/admin
  * Note that data is completely purged if you recreate the container

---

# Grafana Panel Plugin Template

[![Build](https://github.com/wildmountainfarms/solarthing-grafana/workflows/CI/badge.svg)](https://github.com/wildmountainfarms/solarthing-grafana/actions?query=workflow%3A%22CI%22)

This template is a starting point for building Grafana Panel Plugins in Grafana 7.0+

## What is Grafana Panel Plugin?

Panels are the building blocks of Grafana. They allow you to visualize data in different ways. While Grafana has several types of panels already built-in, you can also build your own panel, to add support for other visualizations.

For more information about panels, refer to the documentation on [Panels](https://grafana.com/docs/grafana/latest/features/panels/panels/)

## Getting started

1. Install dependencies

   ```bash
   yarn install
   ```

2. Build plugin in development mode or run in watch mode

   ```bash
   yarn dev
   ```

   or

   ```bash
   yarn watch
   ```

3. Build plugin in production mode

   ```bash
   yarn build
   ```

## Learn more

- [Build a panel plugin tutorial](https://grafana.com/tutorials/build-a-panel-plugin)
- [Grafana documentation](https://grafana.com/docs/)
- [Grafana Tutorials](https://grafana.com/tutorials/) - Grafana Tutorials are step-by-step guides that help you make the most of Grafana
- [Grafana UI Library](https://developers.grafana.com/ui) - UI components to help you build interfaces using Grafana Design System
