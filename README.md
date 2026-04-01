# VRMS Microservices

Spring Boot microservices workspace for the VRMS (Vehicle Registration Management System) assignment.

## Current Workspace Layout

This repository contains five generated Spring Boot services:

- `api-gateway`
- `cars-service`
- `owners-service`
- `agents-service`
- `registration-service`

A project generation script is included at `create-projects.bash`.

## What Has Been Completed

Based on the current repository files:

- Service skeletons were generated using Spring Initializr via `create-projects.bash`.
- Each service is a Gradle project with its own wrapper and standard Spring structure.
- Core folders exist in each service:
  - `src/main/java`
  - `src/main/resources`
  - `src/test/java`
- Each service has its own `application.properties` and `settings.gradle`.

## Tech Stack (From Generation Script)

- Java 17
- Spring Boot 4.0.2
- Gradle
- Dependencies used during generation: `web`, `validation`

## Prerequisites

- JDK 17
- Bash-compatible shell (WSL recommended on Windows for script-based workflow)
- Git

## Generate Services (If Needed)

From repository root:

```bash
bash create-projects.bash
```

The script skips services that already exist.

## Build Commands

### Build One Service

```bash
cd api-gateway
bash gradlew build
```

Repeat for each service directory.

### Build From Root (After Root Multi-Project Setup)

If you add a root-level `settings.gradle` and copy a root Gradle wrapper, you can build from root:

```bash
bash gradlew build
```

## Windows + WSL Note

If your project is under `/mnt/c/...`, some Gradle tasks may fail with file permission errors when setting file modes.

Recommended options:

- Work from Linux filesystem (for example `~/projects/vrms-microservices`), or
- Enable WSL metadata mounts if you must stay under `/mnt/c`.

## Suggested Next Steps

1. Add root `settings.gradle` to register all five services as one multi-project build.
2. Add/copy root Gradle wrapper (`gradlew`, `gradlew.bat`, `gradle/`) from one service.
3. Assign distinct ports in each service `application.properties`.
4. Start implementing controllers, service layers, persistence, and integration logic.

## Author

Aarush Patel

