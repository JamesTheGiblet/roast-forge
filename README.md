## RoastForge: Coffee Roasting Emergence Simulator

RoastForge is a high-fidelity, browser-based simulation designed to bridge the gap between coffee roasting science and interactive software. By modeling the thermal mass, chemical degradation, and physical expansion of coffee beans, RoastForge provides a "sandbox" for understanding how variables like altitude (density) and airflow affect the final cup profile.

---

## 🛠 Features

* **Kinetic Thermal Engine:** Simulates bean temperature (BT) based on drum speed, airflow, and batch size.
* **Chemical Evolution Tracking:** Real-time monitoring of Caffeine, Chlorogenic Acids (acidity), Sugars (caramelization), and Volatile compounds (aroma).
* **Physical Feedback:** * **Visuals:** Procedural bean browning and physical expansion.
* **Audio:** Procedurally generated "cracking" sounds using the Web Audio API.


* **Dynamic Graphing:** Real-time canvas-based plotting of the roasting curve and Rate of Rise (RoR).
* **CaffeineForge Export:** Generates a JSON-based brewing profile including grind size, water temperature, and extraction efficiency recommendations based on the roast's specific chemistry.

---

## 🧪 The Science Behind the Simulation

### 1. Thermal Dynamics

The simulator uses a simplified heat transfer model. The Heating Rate (HR) is determined by:



Where:

* \epsilon is the efficiency derived from **Airflow** and **Drum Speed**.
* M_{thermal} is the mass calculated from **Batch Size** and **Bean Density**.

### 2. The Roasting Phases

RoastForge accurately tracks the four primary stages of a roast:

1. **Drying Phase (<160°C):** Moisture is evaporated; the bean remains greenish-yellow.
2. **Maillard Reaction (160°C - 180°C):** Amino acids and reducing sugars react to create complex flavors and brown pigments (melanoidins).
3. **First Crack (~196°C):** Water vapor pressure breaks the bean structure. In RoastForge, this is modeled as an exothermic spike where the bean releases heat.
4. **Development/Second Crack (>200°C):** The "roaster's window." The simulator tracks sugar carbonization and the eventual cellular breakdown at the second crack.

---

## 🚀 Getting Started

### Prerequisites

* A modern web browser (Chrome, Firefox, Edge, or Safari).
* Audio enabled (to hear the First and Second cracks).

### How to Use

1. **Configure Bean Props:** Set the density (based on altitude) and moisture content. High-density beans (SHB) require more energy to heat.
2. **Adjust Roaster Settings:** Set your target drop temperature and manage airflow.
3. **Monitor the Curve:** Watch the **RoR (Rate of Rise)**. A crashing RoR can lead to "baked" flavors, while a rising RoR post-first crack can lead to "scorched" notes.
4. **Export:** Once stopped, click **"Generate Brew Profile"** to see how your roast should be brewed.

---

## 📂 File Structure

```text
RoastForge/
├── index.html      # Core logic, UI structure, and CSS styles
└── README.md       # Project documentation

```

---

## ⚖️ Technical Limitations

* **Simplified Airflow:** The current version treats airflow as a static heat transfer multiplier rather than a complex convective cooling/heating variable.
* **Linear Moisture Loss:** Moisture loss is modeled as a function of temperature rather than a complex partial pressure calculation.

---

## 📜 License

This project is open-source and intended for educational purposes in the specialty coffee community.

---

Would you like me to **add a specific section on how to interpret the JSON export data**, or should I **expand the "Physics" section** with more detailed formulas?
