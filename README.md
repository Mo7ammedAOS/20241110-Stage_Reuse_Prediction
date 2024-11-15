# 🚀 SpaceX Rocket Landing Success Prediction

## **Background**
SpaceX, a leader in the space industry, aims to make space travel affordable for everyone.  
Its key accomplishments include:
- Sending spacecraft to the International Space Station.
- Launching a satellite constellation for global internet access.
- Conducting manned space missions.  

SpaceX achieves cost efficiency by reusing the first stage of its Falcon 9 rockets, reducing launch costs to $62 million compared to $165 million for competitors. Using public data and machine learning models, this project predicts the success of first-stage landings, providing insights into launch costs.

---

## **Research Goals**
1. Explore the relationship between payload mass, launch site, number of flights, orbits, and first-stage landing success.  
2. Analyze the rate of successful landings over time.  
3. Identify the best predictive model for binary classification of successful landings.

---

## **Executive Summary**
This project identifies factors contributing to a successful rocket landing through:
- **Data Collection:** Using the SpaceX REST API and web scraping.  
- **Data Wrangling:** Creating a success/fail outcome variable.  
- **Exploratory Data Analysis (EDA):** Visualizing trends by payload, launch sites, and time.  
- **SQL Analytics:** Calculating payload statistics, success rates, and launch site proximity analysis.  
- **Model Building:** Comparing logistic regression, SVM, decision trees, and KNN.

---

## **Results**

### **Exploratory Data Analysis (EDA):**
- Launch success has improved over time.  
- KSC LC-39A has the highest success rate among launch sites.  
- Orbits ES-L1, GEO, HEO, and SSO have a 100% success rate.

### **Visualization and Analytics:**
- Most launch sites are near the equator and close to the coast.

### **Predictive Analytics:**
- All models performed similarly on the test set.  
- The decision tree model slightly outperformed others in terms of accuracy.

---

## **Methodology**

### **Data Collection - SpaceX API:**
1. Request rocket launch data using SpaceX API.  
2. Convert responses to DataFrame using `.json()` and `.json_normalize()`.  
3. Filter for Falcon 9 launches.  
4. Handle missing payload values using the mean.  
5. Export the data to a CSV file.

### **Data Collection - Web Scraping:**
1. Scrape Falcon 9 launch data from Wikipedia using BeautifulSoup.  
2. Parse HTML tables and extract relevant data.  
3. Convert data to a DataFrame and export it to CSV.

### **Data Wrangling:**
- Convert outcomes into binary values (1 for success, 0 for failure).

### **EDA with Visualization:**
- Create charts to analyze relationships and show comparisons.

### **EDA with SQL:**
- Query data for insights such as total payloads and success rates.

### **Maps with Folium:**
- Visualize launch sites, outcomes, and distances to proximities.

### **Dashboard with Plotly Dash:**
- **Pie Chart:** Displays successful launches by site.  
- **Scatter Plot:** Payload Mass vs. Success Rate by Booster Version.

### **Predictive Analytics:**
1. Prepare data with `StandardScaler` and split into training/testing sets.  
2. Use `GridSearchCV` with 10-fold cross-validation for optimization.  
3. Evaluate models (Logistic Regression, SVM, Decision Tree, KNN) using:
   - **Jaccard Score**
   - **F1 Score**
   - **Accuracy**

---

