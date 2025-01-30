# GoTej: Navigate Smarter, Arrive Faster

![GoTej](https://github.com/mmahesh09/GoTej/blob/6993d32e50233722eeee8d8eb9066f7647a36ef8/Project%20assets/Credit-Card%20fraud%20detection%20(5).png)

>"In 2023, Bangalore and Pune recorded the longest traffic delays in India during rush hours, with commuters spending an average of 257 hours per year stuck in traffic. Mumbai followed closely behind, with individuals spending 198 hours annually in traffic during peak times. Furthermore, Bangalore had the highest average travel time, taking 28 minutes to cover just 10 kilometers."


## Problem Statement

Urban traffic congestion causes significant delays, economic losses, and fuel wastage, impacting productivity and daily life. Many lack real-time traffic insights, especially non-smartphone users. GoTej addresses this by providing instant, multilingual traffic updates via SMS and WhatsApp, enabling smarter and faster travel decisions.


## Existing Methods vs. GoTej
| Feature | Existing Methods (Google Maps, Waze, etc.) | GoTej |
|---------|--------------------------------------|------|
| **Traffic Updates** | Available via mobile apps | Available via SMS, WhatsApp, and web |
| **Multilingual Support** | Limited language options | Full multilingual support for diverse users |
| **Non-Smartphone Accessibility** | Requires internet and smartphone | Works on SMS, making it accessible to all |
| **Traffic Clearance Prediction** | Basic estimation | More user-friendly and region-specific insights |
| **Cost Efficiency** | Requires mobile data | Works with minimal data and low-cost SMS |
| **User Interaction** | App-based navigation | Simple text-based query and response system |
| **Integration with Messaging Platforms** | Not available | Fully integrated with WhatsApp and SMS services |


## **Process Flow of GoTej**  

Here’s how **GoTej** works in simple steps:  

![image](https://github.com/mmahesh09/GoTej/blob/9b6a915a020e09cdeb28994457fe9ad452a90581/Project%20assets/1.png)

### **1. User Request (Input)**  
- A user sends a message (via **WhatsApp** or **SMS**) with a location name.  
  - Example: **"Traffic Bengaluru"**  


### **2. Backend Processing**  
- The **Node.js backend receives the request**.  
- The backend extracts the **location name** from the message.  


### **3. Fetching Traffic Data**  
- The backend calls the **Google Maps API** to fetch live traffic data for that location.  
- It also estimates **how long it will take for traffic to clear**.  


### **4. Language Translation (If Needed)**  
- If the user has selected a preferred language, the response is translated using the **Google Cloud Translation API**.  
  - Example: If the user prefers **Hindi**, the message is translated before being sent back.  


### **5. Sending the Response**  
- The processed traffic update is sent back to the user via **WhatsApp or SMS**, using the **Twilio API**.  
  - Example Response:  
    > 🚦 **Traffic Update for Bengaluru**  
    > ✅ Heavy Traffic (30 min delay)  
    > ⏳ Estimated clearance: 45 minutes  


### **6. Optional Features**  
- **Machine Learning (Future Enhancement)**: AI-based prediction of traffic clearance time.  
- **Web Dashboard (Optional)**: A **React.js** dashboard where users can check traffic visually.  

