# Yamdut Frontend (MVC Architecture)

Yamdut(frontend) is built using a clean **MVC (Model-View-Controller)** architecture.
It follows a desktop-first UI approach, focusing on clarity, modularity and maintainability.
What I believe and want is to make easy and no B/S when i'm adding new features.

---

## Architecture Overview (MVC)

The Yamdut follows the structured MVC pattern, ensuring clear seperation of responsibilities and easy future scalability.

### Project Structure
```
.
├── app
│   ├── build.gradle.kts
│   └── src
│       ├── main
│       │   ├── java
│       │   │   └── org
│       │   │       └── yamdut
│       │   │           ├── App.java
│       │   │           ├── core
│       │   │           │   ├── AppState.java
│       │   │           │   └── ScreenManager.java
│       │   │           ├── MainWindow.java
│       │   │           ├── models
│       │   │           │   ├── Location.java
│       │   │           │   ├── Ride.java
│       │   │           │   └── User.java
│       │   │           ├── network
│       │   │           │   ├── ApiClient.java
│       │   │           │   └── EndPoints.java
│       │   │           ├── ui
│       │   │           │   ├── components
│       │   │           │   │   ├── InputField.java
│       │   │           │   │   ├── PrimaryButton.java
│       │   │           │   │   └── RoundPanel.java
│       │   │           │   ├── home
│       │   │           │   │   └── HomeScreen.java
│       │   │           │   ├── login
│       │   │           │   │   └── LoginScreen.java
│       │   │           │   ├── profile
│       │   │           │   │   └── ProfileScreen.java
│       │   │           │   ├── rides
│       │   │           │   │   ├── RideRequestScreen.java
│       │   │           │   │   └── RideStatusScreen.java
│       │   │           │   └── signup
│       │   │           │       └── SignUpScreen.java
│       │   │           └── utils
│       │   │               ├── Theme.java
│       │   │               ├── UIUtils.java
│       │   │               └── Validators.java
│       │   └── resources
│       │       └── icons
│       │           └── logo.png
│       └── test
│           ├── java
│           │   └── org
│           │       └── example
│           │           └── AppTest.java
│           └── resources
├── gradle
│   ├── libs.versions.toml
│   └── wrapper
│       ├── gradle-wrapper.jar
│       └── gradle-wrapper.properties
├── gradle.properties
├── gradlew
├── gradlew.bat
├── settings.gradle.kts
└── yamdut-mascot.png
```
