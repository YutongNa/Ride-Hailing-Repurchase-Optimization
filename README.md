# Ride-hailing Platform Repurchase Rate Optimization

> **Note**: This project showcases my data analysis internship work. To maintain confidentiality, this repository contains no proprietary code or data, only methodology and results summary.

## 📊 Project Overview

- **Business Context**: A ride-hailing platform observed declining 7-day repurchase rates, primarily driven by users completing first rides via WeChat/Alipay mini-programs (lower retention vs native app). 
- **My Role**: Data Analytics Intern
- **Key Objectives**:
    1. Quantify coupon campaign impact on repurchase rates through rigorous A/B testing
    2. Identify user segments insensitive to coupons using uplift modeling to save marketing costs
    3. Determine optimal coupon value balancing repurchase lift vs subsidy cost
    4. Design future A/B tests for strategy validation

## 🛠 Tech Stack & Tools

- **Languages**: Python
- **Libraries**: Pandas, NumPy, Scikit-learn, EconML, Matplotlib, Seaborn, SciPy
- **Methods**: Hypothesis Testing (Chi-square), Causal Inference (Uplift Modeling), Machine Learning (Causal Forests)

## 💡 Key Analyses & Results

#### 1. A/B Test Validation
- **Approach**: Conducted chi-square tests to compare repurchase rates between treatment (received coupon) and control groups
- **Result**: Statistically significant lift in repurchase rates for both platforms (**+3.95% for Alipay, +3.87% for WeChat**, p-value < 0.001)

#### 2. Uplift Modeling for Personalized Targeting
- **Approach**: Implemented `CausalForestDML` from EconML to estimate Individual Treatment Effects (ITE)
- **Result**: Identified **negative-response segment** (new users with short wait times + long trips) where coupons reduced platform entry probability by 0.8%. Recommended excluding this segment from campaigns.

#### 3. Cost-Benefit Optimization
- **Approach**: Analyzed marginal repurchase lift per additional RMB across coupon values (4-10 RMB)
- **Result**: While 8-10 RMB coupons maximized repurchase lift, **5-7 RMB coupons provided optimal cost-effectiveness**. Recommended tiered strategy based on budget constraints.

## 📈 Business Impact

- **Cost Savings**: Identified 8% of users as low/negative responders, enabling immediate cost reduction on SMS and coupon subsidies
- **ROI Improvement**: Data-driven coupon valuation increased expected ROI by 15% compared to one-size-fits-all approach
- **Strategic Foundation**: Established causal inference framework for future marketing optimization experiments

## 🧠 Lessons Learned

- **Technical**: Gained hands-on experience applying cutting-edge causal ML techniques to real-world business problems
- **Business**: Developed keen understanding of balancing customer acquisition costs with long-term retention value
- **Future Work**: Exploring advanced feature engineering (temporal patterns, geospatial data) to enhance model precision
