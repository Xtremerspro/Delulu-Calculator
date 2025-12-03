# **🦄 Delulu Calculator (US Edition)**

**"How picky are you?"**

The **Delulu Calculator** is a humorous, single-file web application that calculates the statistical probability of finding your ideal partner in the United States. It compares your preferences against demographic data (Census, CDC, etc.) to determine if your standards are "Realistic" or if you need to "Get Therapy."

## **🎮 Features**

* **Dual Gender Support:** Switch between "Girl" and "Boy" modes with gender-specific attributes.  
* **Real-time Probability Engine:** Calculates the mathematical chance (e.g., "0.0004%") and "1 in X" ratio.  
* **Dynamic UI:** Uses Tailwind CSS for a responsive, glass-morphism design with interactive range sliders.  
* **Delulu Score:** Assigns a "Delusion Level" ranging from *Realistic* to *Terminally Delulu*.

## **🧮 How It Works**

The calculator starts with the total adult population and applies cumulative probability filters based on the user's selection. While this is a "toy" app for entertainment, the underlying logic mimics demographic filtering.

### **The Algorithm**

The core calculation follows this logic chain:

$$P\_{total} \= P\_{race} \\times P\_{height} \\times P\_{hair|race} \\times P\_{eyes|race} \\times P\_{body} \\times P\_{age} \\times P\_{specifics}$$

1. **Height:** Uses a **Normal Distribution** (Bell Curve) calculation based on US mean height and standard deviation to find the percentage of the population taller than the selected value.  
   * *Female Mean:* \~63.7" (SD 2.7)  
   * *Male Mean:* \~69.1" (SD 2.9)  
2. **Correlations:**  
   * **Hair/Eye & Race:** The app accounts for genetic correlations. For example, selecting "Asian" \+ "Blonde" \+ "Blue Eyes" results in a significantly lower probability than "White" \+ "Blonde."  
   * **Body Type & Cup Size (Female Mode):** Logic exists to penalize statistically rare combinations, such as "Underweight" BMI combined with "DD+" cup sizes.  
3. **Income (Male Mode):** Uses US individual income percentile brackets. Demanding a $100k+ salary drastically reduces the pool (top \~18% of men).  
4. **Age & Marriage:** Filters by the size of the selected age slice and adjusts for marriage rates within that age bracket.

### **Data Sources (Approximate)**

* **US Census Bureau:** Age, Race, Marital Status, and Income data.  
* **CDC:** Height, Weight, and BMI anthropometric data.  
* **Health Studies:** Eye and hair color distribution estimates.

## **🛠️ Tech Stack**

* **HTML5**  
* **Tailwind CSS** (via CDN for zero-build setup)  
* **Vanilla JavaScript** (No frameworks required)  
* **FontAwesome** (Icons)

## **🚀 Usage**

Since this is a single-file application, no build process or server installation is required.

1. Clone the repository.  
2. Open delulu\_calculator.html in any modern web browser (Chrome, Safari, Firefox).  
3. Select your preferences and click **Calculate**.

## **📝 License**

Distributed under the MIT License. See LICENSE for more information.

*Disclaimer: This calculator is for entertainment purposes only. Please do not base major life decisions or breakups on a web app.*
