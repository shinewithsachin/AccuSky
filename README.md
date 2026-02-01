# AccuSky: Intelligent Weather Dashboard

[cite_start]AccuSky is a custom ServiceNow Service Portal application designed to provide real-time weather tracking, 5-day forecasting, and data visualization for cities globally[cite: 14, 15]. [cite_start]Beyond basic weather reporting, it features an **Intelligent Advice System** that interprets environmental data to provide actionable lifestyle recommendations, such as "Wear a jacket" or "Carry an umbrella"[cite: 16].

---

## 🚀 Project Overview
[cite_start]The Intelligent Weather Dashboard is built on the ServiceNow platform as a custom Service Portal widget[cite: 14]. [cite_start]It serves as a comprehensive tool for monitoring global weather conditions while offering smart, data-driven insights[cite: 15, 16].

* [cite_start]**Platform**: ServiceNow Service Portal[cite: 14].
* [cite_start]**Core Logic**: Features a "Smart Advice" algorithm that prioritizes safety (such as rain or snow conditions) over temperature and general sky conditions[cite: 61].
* [cite_start]**User Interface**: A modern Dark Mode interface utilizing vibrant, color-coded icons and responsive cards[cite: 101].

---

## 🏗️ System Architecture
[cite_start]The application is structured using a **Model-View-Controller (MVC)** pattern within the ServiceNow framework to ensure a secure separation of concerns[cite: 22].

* [cite_start]**View (HTML/CSS)**: The user interface that displays data, icons, and Chart.js graphs[cite: 47].
* [cite_start]**Controller (Client Script)**: Handles user input, logic for the "Smart Advice" system, and data binding using AngularJS[cite: 48].
* [cite_start]**Model (Server Script)**: A Script Include (`WeatherHelper`) that acts as a secure bridge between the client and the external API[cite: 49].
* [cite_start]**External Integration**: Connects to the **AccuWeather API database** via REST message configuration[cite: 50, 94].

---

## 🛠️ Technical Implementation
[cite_start]AccuSky manages a complex data flow to ensure security and performance[cite: 23].

1. [cite_start]**User Trigger**: The user enters a city name, which triggers a `c.checkEnter()` event in the widget[cite: 72, 73].
2. [cite_start]**Asynchronous Request**: The client script initiates an asynchronous `GlideAjax` call to the `WeatherHelper` Script Include[cite: 77].
3. [cite_start]**Outbound REST**: The server-side script executes an HTTP GET request to the AccuWeather API, keeping the API key hidden from the client[cite: 23, 84].
4. [cite_start]**Data Processing**: The system returns a JSON string, which is parsed by the client to run the advice logic and render trend graphs[cite: 78, 79, 80].
5. [cite_start]**UI Rendering**: The dashboard updates the DOM and charts (using Chart.js) to display the final weather results[cite: 81, 82].

---

## 💻 Key Technologies Used
* [cite_start]**ServiceNow Platform**: Service Portal, Widget Editor, and Script Includes[cite: 92, 93].
* [cite_start]**Frontend**: AngularJS, JavaScript, and SCSS/CSS with Glassmorphism effects[cite: 93, 96].
* [cite_start]**Data Visualization**: Chart.js for line graphs[cite: 95].
* [cite_start]**Integration**: Outbound REST Messages and AccuWeather API[cite: 17, 94].
* [cite_start]**Icons**: Font Awesome for dynamic, weather-specific icons[cite: 95].

---

## 🔮 Future Scope
* [cite_start]**Geolocation**: Implement the browser HTML5 Geolocation API to detect user location automatically on load[cite: 118].
* [cite_start]**Historical Data**: Integrate paid API plans to enable a "History" tab for viewing past weather trends[cite: 119].
* [cite_start]**User Customization**: Allow users to toggle preferences between Celsius and Fahrenheit[cite: 120].

---

[cite_start]**Author**: Sachin Kumar [cite: 3]  
[cite_start]**Department**: Department of Computer Science, IIIT Guwahati [cite: 3, 4]  
[cite_start]**Date**: January 12, 2026 [cite: 5]
