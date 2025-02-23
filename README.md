# 🌦️ Weather Application

A responsive weather application built using **HTML**, **CSS**, and **JavaScript** that displays real-time weather information for any city using the **OpenWeatherMap API**. The app shows temperature, humidity, wind speed, and weather conditions with dynamic icons based on the forecast.

---

## 🚀 Features

- 🔎 Search weather details by city name.  
- 🌡️ Real-time temperature display in Celsius.  
- 🌬️ Displays humidity levels and wind speed.  
- 🌤️ Dynamic weather icons based on current conditions (Rain, Clouds, Clear, etc.).  
- ⚡ Error handling for invalid city names.  
- 💻 Responsive design with a modern, clean UI.

---

## 🔧 Technologies Used

- **HTML5** - For structuring the web page.  
- **CSS3** - For styling the application with gradients and responsive layouts.  
- **JavaScript (Vanilla JS)** - For fetching and displaying weather data dynamically.  
- **OpenWeatherMap API** - To retrieve real-time weather data.

---

## 💡 How It Works

1. The user enters a city name in the input field.
2. On clicking the search button, the app makes an API call to **OpenWeatherMap**.
3. The response data is processed and displayed, including:
   - City name
   - Temperature (°C)
   - Humidity (%)
   - Wind speed (km/h)
   - Weather icon (rain, clear, clouds, etc.)
4. If an invalid city is entered, an error message is displayed.

---

## 🖼️ UI Preview

> Add screenshots of your app here (e.g., images of the weather display for different cities and weather conditions).

---

## ⚙️ Setup and Installation

### 1. **Clone the Repository**
```bash
git clone <your-repo-link>
cd weather-app
```

### 2. **Add Your OpenWeatherMap API Key**
Replace the value of `apiKey` in the `<script>` section of the HTML file:
```javascript
const apiKey = "YOUR_API_KEY_HERE";
```
> You can get a free API key by signing up at [OpenWeatherMap](https://openweathermap.org/).

### 3. **Run the Application**
- Open `app.html` in any web browser.
- Enter the name of a city and view real-time weather details.

---

## ⚡ Code Highlights

- **API Fetching Logic:**
```javascript
const apiUrl = "https://api.openweathermap.org/data/2.5/weather?units=metric&q=";
async function checkWeather(city) {
    const response = await fetch(apiUrl + city + `&appid=${apiKey}`);
    const data = await response.json();
    // Update UI with weather data
}
```

- **Dynamic Weather Icon Update:**
```javascript
if (data.weather[0].main == "Clouds") {
    weatherIcon.src = "cloud.png";
} else if (data.weather[0].main == "Clear") {
    weatherIcon.src = "clear.jpg";
}
```

- **Error Handling for Invalid City:**
```javascript
if (response.status == 404) {
    document.querySelector(".error").style.display = "block";
    document.querySelector(".weather").style.display = "none";
}
```

---

## 🌐 Live Demo

> [🔗 Live Demo Link (if hosted on GitHub Pages, Netlify, etc.)](#)

---

## 💬 Future Enhancements

- 🌎 Add support for selecting temperature units (°C/°F).  
- 📍 Fetch user’s current location weather using Geolocation API.  
- 🌙 Add dark mode toggle for better UI experience.  
- ⏳ Include a loading spinner while fetching data.  
- 📈 Display additional details like sunrise/sunset time, pressure, and forecast.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to open a [pull request](#) or [issue](#).

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## ✨ Acknowledgments

- [OpenWeatherMap API](https://openweathermap.org/) for providing free weather data.
- [Unsplash](https://unsplash.com/) for free weather-related icons (if applicable).

---

📩 **Contact:** [Your Email/Portfolio Link]  
⭐ *If you liked this project, give it a star!*
