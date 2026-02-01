# AccuSky: Intelligent Weather Dashboard

AccuSky is a custom ServiceNow Service Portal application designed to provide real-time weather tracking, 5-day forecasting, and data visualization for cities globally. Beyond basic weather reporting, it features an **Intelligent Advice System** that interprets environmental data to provide actionable lifestyle recommendations, such as "Wear a jacket" or "Carry an umbrella".

---

## 🚀 Project Overview
The Intelligent Weather Dashboard is built on the ServiceNow platform as a custom Service Portal widget. It serves as a comprehensive tool for monitoring global weather conditions while offering smart, data-driven insights.

* **Platform**: ServiceNow Service Portal.
* **Core Logic**: Features a "Smart Advice" algorithm that prioritizes safety (such as rain or snow conditions) over temperature and general sky conditions.
* **User Interface**: A modern Dark Mode interface utilizing vibrant, color-coded icons and responsive cards.

---

## 🏗️ System Architecture
The application is structured using a **Model-View-Controller (MVC)** pattern within the ServiceNow framework to ensure a secure separation of concerns.

* **View (HTML/CSS)**: The user interface that displays data, icons, and Chart.js graphs.
* **Controller (Client Script)**: Handles user input, logic for the "Smart Advice" system, and data binding using AngularJS.
* **Model (Server Script)**: A Script Include (`WeatherHelper`) that acts as a secure bridge between the client and the external API.
* **External Integration**: Connects to the **AccuWeather API database** via REST message configuration.

---

## 🛠️ Technical Implementation
AccuSky manages a complex data flow to ensure security and performance.

1. **User Trigger**: The user enters a city name, which triggers a `c.checkEnter()` event in the widget.
2. **Asynchronous Request**: The client script initiates an asynchronous `GlideAjax` call to the `WeatherHelper` Script Include.
3. **Outbound REST**: The server-side script executes an HTTP GET request to the AccuWeather API, keeping the API key hidden from the client.
4. **Data Processing**: The system returns a JSON string, which is parsed by the client to run the advice logic and render trend graphs.
5. **UI Rendering**: The dashboard updates the DOM and charts (using Chart.js) to display the final weather results.

---

## 💻 Key Technologies Used
* **ServiceNow Platform**: Service Portal, Widget Editor, and Script Includes.
* **Frontend**: AngularJS, JavaScript, and SCSS/CSS with Glassmorphism effects.
* **Data Visualization**: Chart.js for line graphs.
* **Integration**: Outbound REST Messages and AccuWeather API.
* **Icons**: Font Awesome for dynamic, weather-specific icons.

---

## 🔮 Future Scope
* **Geolocation**: Implement the browser HTML5 Geolocation API to detect user location automatically on load.
* **Historical Data**: Integrate paid API plans to enable a "History" tab for viewing past weather trends.
* **User Customization**: Allow users to toggle preferences between Celsius and Fahrenheit.

---

**Author**: Sachin Kumar  
**Department**: Department of Computer Science, IIIT Guwahati  
**Date**: January 12, 2026
