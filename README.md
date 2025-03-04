### About This Project

Complete environment configuration for Maven builds in Github workflows. Default maven version is 3.9.9 (Java 8).

### How To Use

Copy to your Github workflow .yml file

Maven Release History: https://maven.apache.org/docs/history.html

```
    - name: Set up Maven
      uses: Contrast-Security-OSS/setup-maven
      with:
        maven-version: {desired.maven.version}
```
