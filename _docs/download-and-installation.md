---
layout: docs
title: Download and Installation
meta_title: "How to Download and Install WireMock"
toc_rank: 13
description: >
    WireMock is available as a standalone service (for Docker of Java), Java library
    and integrations for modern languages and technology stacks.
---


## Download options

WireMock Java is distributed in two flavours - a standard JAR containing just WireMock, and a standalone uber JAR containing
WireMock plus all its dependencies.

Most of the standalone JAR's dependencies are shaded i.e. they are hidden in alternative packages. This allows WireMock to be used in projects with
conflicting versions of its dependencies. The standalone JAR is also runnable (see [Running as a Standalone Process](../running-standalone/)).

## Test dependencies

<div class="downloads-wrapper">
    {% include downloads.html %}
</div>

## Standalone Service

### WireMock 3.x Beta (recommended)

#### Maven

```xml
<dependency>
    <groupId>org.wiremock</groupId>
    <artifactId>wiremock-standalone</artifactId>
    <version>{{ site.wiremock_beta_version }}</version>
    <scope>test</scope>
</dependency>
```

#### Gradle

```groovy
testImplementation "org.wiremock:wiremock-standalone:{{ site.wiremock_beta_version }}"
```

### WireMock 2.x Stable

#### Docker

Run the following in a terminal:

```bash
docker run -it --rm \
  -p 8080:8080 \
  --name wiremock \
  wiremock/wiremock:{{ site.wiremock_version }}
```

Learn more in the [Docker guide](../docker).

#### Maven - stable

```xml
<dependency>
    <groupId>com.github.tomakehurst</groupId>
    <artifactId>wiremock-jre8-standalone</artifactId>
    <version>{{ site.wiremock_version }}</version>
    <scope>test</scope>
</dependency>
```

#### Gradle - stable

```groovy
testImplementation "com.github.tomakehurst:wiremock-jre8-standalone:{{ site.wiremock_version }}"
```

## Direct download

If you want to run WireMock as a standalone process you can
<a id="wiremock-standalone-download" href="https://repo1.maven.org/maven2/org/wiremock/wiremock-standalone/{{ site.wiremock_beta_version }}/wiremock-standalone-{{ site.wiremock_beta_version }}.jar">download the standalone JAR from
here</a>
