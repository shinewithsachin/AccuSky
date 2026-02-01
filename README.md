# AccuSky: Intelligent Weather Dashboard

![ServiceNow](https://img.shields.io/badge/ServiceNow-293E40?style=for-the-badge&logo=servicenow&logoColor=white)
![AngularJS](https://img.shields.io/badge/AngularJS-E23237?style=for-the-badge&logo=angularjs&logoColor=white) 
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) 
![Sass](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white) 
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) 
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white) 
![Font Awesome](https://img.shields.io/badge/Font_Awesome-339AF0?style=for-the-badge&logo=font-awesome&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-005571?style=for-the-badge&logo=google-cloud&logoColor=white)

AccuSky is a custom ServiceNow Service Portal application designed to provide real-time weather tracking, 5-day forecasting, and data visualization for cities globally. Beyond basic weather reporting, it features an **Intelligent Advice System** that interprets environmental data to provide actionable lifestyle recommendations, such as "Wear a jacket" or "Carry an umbrella".

---
## 📺 Project Demo
Experience the Intelligent Weather Dashboard in action: **[Watch the Live Demo here](https://drive.google.com/file/d/1z3Jjfo-6Kez_eiroql_kUI8V8OJTDEEx/view?usp=sharing)**

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
## 📸 Screenshots
![](Screenshot%202026-01-13%20030043.png)
![](Screenshot%202026-01-13%20030056.png)
![](Screenshot%202026-01-13%20030108.png)


---

## 📬 Contact
Created by **Sachin Kumar** 
* [LinkedIn Profile](https://www.linkedin.com/in/sachin-iiitg/)
* [GitHub Profile](https://github.com/shinewithsachin)
* [My Portfolio](https://build-your-portfolio-ceetocb.gamma.site/untitled-lsuym)
