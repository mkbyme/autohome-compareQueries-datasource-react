# Grafana Compare Query Datasource

Migrate to React version support Grafana 10 and above

---

[中文文档](https://github.com/AutohomeCorp/autohome-compareQueries-datasource/blob/master/README_zh.md)

Webpack copy of [grafana-meta-queries](https://github.com/GoshPosh/grafana-meta-queries) implementing https://github.com/grafana/grafana/issues/2093

This plugin is built as a datasource plugin that combines and contrasts different time shifts data.

Time shift supports the following units: s (seconds), m (minutes), h (hours), d (days), w (weeks), M (months), y (years)

## Screenshots

![Screenshot1](https://raw.githubusercontent.com/AutohomeCorp/autohome-compareQueries-datasource/master/img/step-1.png)

![Screenshot2](https://raw.githubusercontent.com/AutohomeCorp/autohome-compareQueries-datasource/master/img/step-2.png)

## Installation

Clone this project into the grafana plugins directory (if you install grafana with the package, the default is /var / lib / grafana / plugins). Restart grafana and the datasource plugin should be detected and automatically used.

## Usage

- Create a datasource and select the Compare Query Datasource plugin.
- Create a basic query
- Create a query use compare query datasource and set base query as compare query
- Add time shift on the compare query

## Build

Important work on a machine that has Grafana installed.
```
$ sudo apt-get install npm
$ sudo apt-get remove cmdtest
$ sudo apt-get remove yarn
$ sudo npm install -g yarn
$ cd /var/lib/grafana/plugins
$ sudo git clone https://github.com/alimli/autohome-compareQueries-datasource.git
$ sudo chown -R ubuntu:ubuntu autohome-compareQueries-datasource
$ cd autohome-compareQueries-datasource/
$ yarn install
$ yarn build
```

## Credits

Based on

- [grafana](https://github.com/grafana/grafana)
- [simple-json-datasource](https://github.com/grafana/simple-json-datasource)
- [grafana-meta-queries](https://github.com/GoshPosh/grafana-meta-queries)

Made by [AutoHome Team](https://github.com/AutohomeCorp)
