# 📊 Product Experimentation (A/B Testing) & ARR Impact Simulator

An interactive, analytics tool designed to bridge the gap between statistical significance and bottom-line business metrics. This tool helps product teams design scientifically sound A/B tests, prevent underpowered experiments, and calculate the financial return on investment (ROI).

### 🔗 Live Link: [View Interactive App Here](https://dhavalk21.github.io/Product-Experimentation-and-ARR-Impact--Simulator/)


## ✨ Core PM Competencies Demonstrated

* **Statistical Rigor:** Calculates minimum sample sizes and duration pre-flight using current active traffic to protect the product against false positives ($\alpha = 5\%$) and false negatives ($\beta = 20\%$).
* **Data-Driven Decision Making:** Analyzes active experiment conversion rates using a standard two-tailed pooled Z-test for proportions to verify statistical significance (p-value).
* **Financial Modeling:** Translates conversion rate lifts directly into annual recurring revenue (ARR) and incremental acquisitions based on average order or contract values.
* **Executive Communication:** Instantly generates a clean, plain-English executive summary memo of the experiment's findings that is ready to be shared with stakeholders.

## ⚙️ How the Math Works

1. **Pre-Flight Sample Size ($n$):** Calculated using standard statistical power analysis for two-sample proportions:
   $$n \approx \frac{2 \cdot (Z_{\alpha/2} + Z_{\beta})^2 \cdot p \cdot (1-p)}{MDE^2}$$
   Where $Z_{\alpha/2} = 1.96$ (95% confidence level), $Z_{\beta} = 0.8416$ (80% statistical power), $p$ is your baseline conversion rate, and $MDE$ is the absolute target Minimum Detectable Effect.

2. **Z-Score and Significance:** Computed using pooled proportion standard error ($SE$) to discover the two-tailed $p$-value:
   $$Z = \frac{p_B - p_A}{SE}$$

3. **Annualized Bottom-Line Lift:**
   $$\Delta \text{ARR} = \text{Annual Addressable Traffic} \times (p_B - p_A) \times \text{Avg. Contract Value} \times \text{Purchase Frequency}$$


## 🚀 Technical Features

* **Widescreen & Responsive Layout:** Crafted with a modern, high-contrast UI using Tailwind CSS.
* **Zero Dependencies:** Runs entirely on client-side vanilla JavaScript, no database, no tracking cookies, and no heavy packages.
* **Interactive Tooltips:** Every input field features a clear, helpful tooltip explaining the terminology, making it easy for stakeholders and recruiters to understand the metrics.
