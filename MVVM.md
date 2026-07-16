### MVC (Model-View-Controller)

#### Flow

```text
User
  ↓
View
  ↓
ViewController
 ↙          ↘
Model      View
```

- User interacts with the **View (UI)**.
- The **ViewController** receives those interactions.
- If needed, the ViewController interacts with the **Model** (API, Database, Business Logic, etc.).
- The ViewController updates the **View** if the UI needs to change.
- As the project grows, the ViewController starts handling too many responsibilities (API calls, validation, business logic, JSON parsing, navigation, UI updates, etc.), leading to a **Massive View Controller**.

> **Note:** The Model is **not just the Database**. It represents the application's data and business logic. It may use a database, an API, local storage, or in-memory objects.

---

### MVVM (Model-View-ViewModel)

- User interacts with the **View (UI)**.
- The **ViewController** receives those interactions.
- Instead of directly interacting with the **Model**, it forwards the request to the **ViewModel**.
- The **ViewModel** communicates with the **Model**, performs the required logic, and returns the result to the ViewController.
- The **ViewController** updates the View if needed.

The ViewController mainly acts as a bridge between the View and the ViewModel, making it much smaller and easier to maintain.

---

#### MVC
The ViewController talks directly to both the View and the Model, which can make it large as the project grows.

#### MVVM
The ViewController (or SwiftUI View) forwards work to the ViewModel, which interacts with the Model. This keeps the UI layer cleaner and separates presentation logic from the View.
