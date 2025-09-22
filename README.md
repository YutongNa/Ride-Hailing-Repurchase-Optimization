# Ride-hailing Platform Repurchase Rate Optimization

> **Note**: This project showcases my data analysis internship work. To maintain confidentiality, this repository contains no proprietary code or data, only methodology and results summary.

## 📊 Project Overview

During my internship, I worked on improving the **7-day repurchase rate** of first-time users on a ride-hailing platform, particularly those who placed their first order via **Alipay or WeChat**. These users had significantly lower repurchase rates compared to app users, dragging down the platform’s overall retention.  

The company launched an **A/B test** by sending selected users a discount coupon (4–10 RMB) via SMS the day after their first ride. My role was to **analyze the effectiveness of this coupon strategy** and provide actionable recommendations.

---

## 🔧 Responsibilities
- Designed and conducted **A/B tests** to measure coupon effectiveness  
- Performed **statistical analysis** (chi-square test) to confirm significance  
- Built an **uplift model (Causal Forest DML)** to identify heterogeneous treatment effects  
- Applied **segmentation analysis** to detect user groups negatively impacted by coupons  
- Optimized coupon allocation strategy by analyzing **cost-effectiveness vs. repurchase gain**

---

## ⚡ Key Challenges
- Ensuring **experiment validity** despite unbalanced treatment/control groups  
- Modeling **heterogeneous user responses**, since coupons worked for some users but not others  
- Balancing **absolute repurchase gains** with **cost efficiency** of coupon distribution  

---

## 🛠️ Tools & Technologies
- **Python**: pandas, numpy, matplotlib, seaborn  
- **Statistical methods**: A/B testing, chi-square test  
- **Causal inference**: EconML (CausalForestDML, uplift modeling)  
- **Machine learning**: RandomForest, GradientBoosting for baseline modeling  

---
## 📊 Results
- Coupons significantly improved repurchase rates
- User heterogeneity discovered
    - Some users (e.g., new users with very short waiting time but long trips) showed **negative response** to coupons  
- Optimal coupon strategy 
  - Repurchase-maximizing coupons: **8–10 RMB**  
  - Cost-effectiveness-maximizing coupons: **5–7 RMB**  
  - Recommended a **segmented strategy**:  
    - Allocate high-value coupons to high-potential users  
    - Use mid-range coupons for general users  
    - Exclude low-response segments  

---

## 🎯 Business Impact
- Provided **data-driven recommendations** for targeted coupon distribution  
- Helped the platform reduce marketing costs while maintaining repurchase uplift  
- Improved decision-making by demonstrating how **causal inference + machine learning** can optimize marketing interventions  

---

## ✨ Key Takeaways

This project demonstrates how **data science + causal inference** can be applied to **real-world business problems** such as customer retention and marketing ROI optimization.
