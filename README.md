
# AspNetCoreMvcCustomLoginAndRegistration (.NET 8)

A custom login and registration system built using **ASP.NET Core MVC (.NET 8)** without ASP.NET Identity. This project provides a simple and educational example of how to implement authentication from scratch using Entity Framework Core and modern security practices.

---

## 🚀 Features

- ✅ Custom user registration & login (no ASP.NET Identity)
- 🔐 Password hashing with SHA256 + Salt
- 🧠 Session-based authentication
- 📋 Input validation (client & server)
- 🧾 Dashboard after login
- 🚪 Logout functionality

---

## 🛠️ Tech Stack

- ASP.NET Core MVC (.NET 8)
- Entity Framework Core 8
- SQL Server / SQLite
- C#
- Bootstrap 5 (UI)
- Visual Studio 2022+ or VS Code

---

## 📦 Getting Started

### 🔧 Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- Visual Studio 2022 (v17.8+) or VS Code
- SQL Server / SQLite

### 📥 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/AspNetCoreMvcCustomLoginAndRegistration.git
   cd AspNetCoreMvcCustomLoginAndRegistration
   ```

2. **Configure the database**
   Open `appsettings.json` and update the connection string:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Your_Connection_String_Here"
   }
   ```

3. **Apply Migrations**
   ```bash
   dotnet ef migrations add InitialCreate
   dotnet ef database update
   ```

4. **Run the application**
   ```bash
   dotnet run
   ```

   Open your browser at: `https://localhost:5001` (or specified port).

---

## 🧪 How It Works

1. Go to `/Account/Register` to register a new user.
2. Then log in at `/Account/Login`.
3. After successful login, you’ll be redirected to the dashboard.
4. Session cookie is created and used for authorization.
5. You can log out via `/Account/Logout`.

---

## 📁 Project Structure

```
AspNetCoreMvcCustomLoginAndRegistration/
├── Controllers/
│   └── AccountController.cs
├── Models/
│   └── User.cs
├── Data/
│   └── AppDbContext.cs
├── Views/
│   └── Account/
│       ├── Login.cshtml
│       ├── Register.cshtml
│   └── Shared/
│       └── _Layout.cshtml
├── wwwroot/
├── appsettings.json
├── Program.cs
└── AspNetCoreMvcCustomLoginAndRegistration.csproj
```

---

## 🔒 Security Notes

- Passwords are hashed using SHA256 and a generated salt.
- Sessions are used for storing user info securely.
- CSRF protection is enabled by default in ASP.NET MVC.
- Consider using `BCrypt` or `PBKDF2` for stronger hashing in production.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributions

Pull requests and suggestions are welcome. Fork the repo, make changes, and submit a PR!

---

## 💬 Questions?

If you have any questions or need support, feel free to open an issue or contact the maintainer.
