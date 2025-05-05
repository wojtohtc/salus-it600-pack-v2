# salus-it600-pack-v2

**Improved and maintained JavaScript library for communicating with Salus iT600 Smart Home thermostats (UG600 gateway).**

This is a community-maintained fork of the original `salus-it600-pack` package, with improved error handling and active development.

---

## ✨ Improvements in v2

- Fixes crash when `access_token` is missing in login response
- Improved stability when Salus API returns null or unexpected data
- Designed for integration with [Homebridge Salus iT600 Gateway v2](https://github.com/wojtohtc/homebridge-salus-it600-gateway-v2)

---

## 📦 Installation

Install from GitHub:

```bash
npm install git+https://github.com/wojtohtc/salus-it600-pack-v2.git
```

Or add to your `package.json`:

```json
"dependencies": {
  "salus-it600-pack-v2": "git+https://github.com/wojtohtc/salus-it600-pack-v2.git"
}
```

---

## 🚀 Usage Example

```javascript
const Salus = require("salus-it600-pack-v2");

const salus = new Salus({
  username: "example@email.com",
  password: "password"
});

salus.getDevices().then(devices => {
  console.log("Thermostats:", devices);
});

salus.updateTemperature("thermostatId123", 21.5);
```

---

## 🤝 Contributing

Pull requests are welcome!  
Please open an issue first if you plan any major changes.  
Make sure to include tests or examples where appropriate.

---

## 📄 License

MIT
