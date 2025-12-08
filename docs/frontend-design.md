# Yamdut Frontend (MVC Architecture)

Yamdut(frontend) is built using a clean **MVC (Model-View-Controller)** architecture.
It follows a desktop-first UI approach, focusing on clarity, modularity and maintainability.
It is built using a clean **MVC (Model-View-Controller)** pattern to ensure:
- Easy Feature development
- Zero clutter/ no "B/S" while adding screens
- Strong seperation of concerns
- Predictable folder structure
- Testability + Scalability

---

## Architecture Overview (MVC)

The Yamdut follows the structured MVC pattern, ensuring clear seperation of responsibilities and easy future scalability.

**Model**
- Contain only data structures & business logic(User, Ride, Location).

**View**
- Pure UI elements (screens, components)
- No business logic, no API calls inside views.

**Controllers**
- (Handled implicitly by ScreenManager + API client)
- Controls screen transitions & handles user actions.

---

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
│       │   │           ├── App.java                                 --> App Launcher
│       │   │           ├── core
│       │   │           │   ├── AppState.java                        --> Global state (logged user,session..)
│       │   │           │   └── ScreenManager.java                   --> Navigation Controller
│       │   │           ├── MainWindow.java                          --> Primary JFrame(root window)
│       │   │           ├── models                                   --> Data Models (M in mvc)
│       │   │           │   ├── Location.java
│       │   │           │   ├── Ride.java
│       │   │           │   └── User.java
│       │   │           ├── network                                  --> Network Layer(API)
│       │   │           │   ├── ApiClient.java
│       │   │           │   └── EndPoints.java
│       │   │           ├── ui                                       --> Views (V in MVC)
│       │   │           │   ├── components                           --> Buttons, input, custom UI elements
│       │   │           │   │   ├── InputField.java
│       │   │           │   │   ├── PrimaryButton.java
│       │   │           │   │   └── RoundPanel.java
│       │   │           │   ├── home
│       │   │           │   │   └── HomeScreen.java
│       │   │           │   ├── login                                --> LoginScreen.java
│       │   │           │   │   └── LoginScreen.java
│       │   │           │   ├── profile
│       │   │           │   │   └── ProfileScreen.java
│       │   │           │   ├── rides
│       │   │           │   │   ├── RideRequestScreen.java
│       │   │           │   │   └── RideStatusScreen.java
│       │   │           │   └── signup                                --> SignUpScreen.java
│       │   │           │       └── SignUpScreen.java
│       │   │           └── utils                                     --> Helper, Theme, Validation
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
