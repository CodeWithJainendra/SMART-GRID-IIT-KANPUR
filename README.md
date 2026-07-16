# Breaker Guard

An Android application for IoT-based smart-grid and circuit-breaker monitoring, developed as part of engineering work at IIT Kanpur.

> **Project status — early stage.** As of the latest commit (May 2025), this repository contains project configuration only; the application source has not yet been published here. The sections below describe the project's purpose and intended scope and state exactly what the repository currently contains. Nothing below claims functionality that is not yet in the code.

## What it is

Breaker Guard is an Android companion app for monitoring circuit breakers in electrical distribution and smart-grid settings. Circuit breakers protect a network by interrupting faulty or overloaded circuits, and their state — closed, tripped, or faulted — is important to track operationally. The project's aim is to give an operator a mobile view of connected breaker units and to surface status and fault information from the field. It was created in the context of smart-grid engineering work at IIT Kanpur.

## Intended scope

These are the goals of the project, listed as intended scope rather than delivered features. They are not yet implemented in this repository:

- An Android interface for monitoring one or more circuit-breaker units
- Visibility into breaker status and trip / fault events
- Remote observation of smart-grid distribution points from a mobile device

The specific IoT transport, sensor hardware, and any backend service are not defined in the repository and are deliberately not specified here.

## What the repository currently contains

- A `.gitignore` configured for an Android / Gradle project: it ignores Android Studio files (`.idea/`), the Gradle cache (`.gradle/`), and build output (`build/`, `app/build/`).

No application source, Gradle build script (`build.gradle`), or `AndroidManifest.xml` has been committed yet.

## Tech stack

- **Platform:** Android — indicated by the repository description and the Android-oriented `.gitignore`.
- **Build system:** Gradle — indicated by the `.gradle/` and `app/build/` ignore entries.
- **Language, libraries, and IoT protocol:** not yet determinable, since no source has been committed. These will be documented once the implementation lands.

## Architecture

The intended system follows a standard device to transport to app shape:

```
Circuit-breaker unit  (field sensing / control)
        |
     network transport
        |
Breaker Guard  (Android monitoring client)
```

The concrete transport (for example Wi-Fi, BLE, MQTT, or HTTP) and any intermediate service are not specified in this repository and will be added with the implementation.

## Status & links

- **Status:** Initial scaffold / work in progress; latest push May 2025.
- **Context:** Developed as part of engineering work at IIT Kanpur.
- **Repository:** https://github.com/CodeWithJainendra/SMART-GRID-IIT-KANPUR

## Running locally

The repository does not yet contain a buildable app. Once the Android source and a Gradle wrapper are added, the usual Android build applies:

```bash
git clone https://github.com/CodeWithJainendra/SMART-GRID-IIT-KANPUR
cd SMART-GRID-IIT-KANPUR
# Open the project in Android Studio, or build from the command line:
./gradlew assembleDebug
```

Requirements: Android Studio and an Android SDK. These steps apply after the application source is committed.
