# **LodgeLogic: Multi-Dimensional Hotel Analytics Suite**

**LodgeLogic** is a data-driven intelligence platform designed to extract actionable insights from complex hotel booking records. Developed in **Scala**, the system utilizes functional programming techniques and mathematical normalization to evaluate hotel performance across three critical business dimensions: market demand, consumer value, and operational profitability.



### **Core Analytical Modules**

* **Market Dominance Tracker:** Automatically aggregates global booking data to identify geographic hotspots. By grouping transactions by destination, the system pinpoints which countries are leading the market in terms of sheer booking volume.
* **Economical Value Index (EVI):** Uses a multi-criteria scoring algorithm to find the best "deal" for customers. It doesn't just look at price; it calculates a weighted score based on low average prices, high discount rates, and thin profit margins to identify the most consumer-friendly options.
* **Profitability Performance Engine:** Identifies the most lucrative hotel assets by balancing high-volume foot traffic (total visitors) against high-yield operations (average profit margins). This allows stakeholders to identify "star" properties that maximize both scale and efficiency.

---

### **Technical Architecture Highlights**

| Feature | Technical Implementation |
| :--- | :--- |
| **Data Parsing** | Integrated CSV reader using `com.github.tototoshi` for seamless ingestion of raw booking logs. |
| **Data Modeling** | Case-class architecture (`HotelData`) ensures type-safety and structured access to 24+ data points per row. |
| **Smart Normalization** | A specialized `Normalizer` object that converts disparate units (SGD, %, counts) into a unified 0-100 score. |
| **Logic Flexibility** | Supports both "Lower-is-Better" (for pricing) and "Higher-is-Better" (for ratings/margins) scoring logic. |
