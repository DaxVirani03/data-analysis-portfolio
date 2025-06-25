<details>
  <summary><strong>🧪 Website A/B Testing for Conversion Optimization</strong></summary>

### 🔍 What I Did  
I ran a simulated A/B test to compare two versions of a website (Variant A and Variant B) to see which one leads to more conversions. The goal was to analyze if the improved version (Variant B) truly performs better—and whether that difference is **statistically significant**.

### 🧪 Setup  
- **Simulated Data**:  
  - 10,000 visitors to **Variant A** (true conversion rate = 10%)  
  - 10,000 visitors to **Variant B** (true conversion rate = 12%)  
- Tracked how many visitors converted on each version  
- Used statistics to decide if the better result is just luck or actually meaningful

### ⚙️ How I Did It  
- Simulated user conversions using the **binomial distribution**  
- Calculated conversion rates and **95% confidence intervals**  
- Performed a **Z-test for proportions** to check if the difference is statistically valid  
- Used **sequential testing** (split data into 60 batches) to track p-values and improvement (lift) over time  
- Visualized results to see when and how the difference became clear

### 📊 Key Results  
- **Conversion Rate A**: 9.73% (CI: 9.15% – 10.31%)  
- **Conversion Rate B**: 11.34% (CI: 10.72% – 11.96%)  
- **Lift** (B - A): Around **1.6%** overall  
- **p-value** fell below 0.05 in the very first batch and stayed low → strong evidence Variant B is better  
- The test confirmed that **Variant B consistently outperforms Variant A**

### 💡 What I Learned  
- Even a **small lift (2%)** can be statistically significant  
- **Sequential testing** helps detect significance early, saving time and resources  
- It's important to look at both **statistical and practical significance** — even if B is better, is a 2% improvement worth the cost of rolling it out?

### 📦 Tech Stack  
- Python (Jupyter Notebook)  
- Libraries: `numpy`, `pandas`, `scipy`, `matplotlib`, `seaborn`

### 🧠 Final Thought  
This experiment shows how A/B testing can guide smart website decisions. Variant B is statistically better—but whether it’s the right call depends on business priorities.

### ✒️ About Me  
**Dax Virani** — This project was part of my internship work focused on Data-Driven Decision Making.  
GitHub: [@DaxVirani03](https://github.com/DaxVirani03)

</details>
