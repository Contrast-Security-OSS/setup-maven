# Setup Maven GitHub Action

This GitHub Action simplifies the setup of Apache Maven within your workflows. It downloads and installs the specified Maven version and adds it to the `PATH` environment variable, making `mvn` commands readily available.

## Usage

```yaml
name: Maven Build

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v3

      - name: Setup Maven
        uses: Contrast-Security-OSS/setup-maven@v1.0.1 
        with:
          maven-version: '3.8.6' # Specify the desired Maven version

      - name: Build with Maven
        run: mvn clean install
