# ML-Recommendation-System-

Company Name: CODTECH IT SOLUTIONS

Name : HARINI N

Intern ID: CT04DL783

Domain : MACHINE LEARNING

Duration: 4 weeks

Mentor : NEELA SANTOSH

DESCRIPTION OF THE RECOMMENDED SYSTEM:
Introduction
The Review-Based Place Recommendation System is a machine learning project designed to suggest tourist attractions based on review statistics, such as the Google review rating and the number of reviews. The goal is to help users find places similar to those they already like, even when no personal user data is available. This system is ideal for travel platforms, guide apps, or individual travelers seeking alternatives to popular destinations.

Dataset Description
The dataset used in this project includes detailed information on various tourist places across different cities and states in India. Each record contains several attributes that describe a place, such as its Zone, State, City, Name, and Type (e.g., Temple, Park, Museum). Additional fields include the year of establishment, time needed to visit (in hours), entrance fee in INR, whether an airport is located within a 50 km radius, weekly off days, and significance (e.g., historical, scientific).
Most importantly, the dataset includes two core review-based fields:
Google Review Rating: A score between 1 and 5.
Number of Google Reviews: Represented in lakhs (hundreds of thousands).
These two fields serve as the foundation for building the recommendation logic.

Approach and Methodology
Since the dataset lacks explicit user interaction data (e.g., user IDs and individual ratings), traditional collaborative filtering techniques are not directly applicable. Instead, a content-based recommendation approach is adopted, using review-related attributes to simulate a collaborative experience.

Feature Selection and Preprocessing:
Only the Google review rating and the number of reviews are selected to define the popularity and quality of each place. These features are normalized using Min-Max Scaling to ensure they are on the same scale.

Similarity Computation:
Cosine similarity is applied to the normalized data to compute a similarity score between each pair of places. This score quantifies how alike two attractions are based on their public reception.

Recommendation Logic:
A custom function allows users to input the name of a place. The system identifies that place’s index in the dataset, calculates similarity scores with all other entries, sorts them in descending order, and returns the top N most similar places. Each recommendation includes the place name, city, review rating, and review count.

Example Use Case
If a user enters "India Gate", the system recommends places with similar review profiles. The top suggestions might include iconic sites like Mysore Palace, Taj Mahal, and Charminar—all highly rated and widely reviewed destinations. This allows users to discover similarly acclaimed locations across the country.

Applications and Benefits:
Personal Travel Planning: Users can discover new places based on crowd opinions.
Travel Apps & Websites: Easily integrable into existing platforms to enhance user engagement.
Scalability: Since the method doesn't rely on user history, it can scale across any dataset with sufficient review data.

Future Enhancements:
The system can be extended by adding:
Filters for zones, place types, or seasonal availability.
A graphical interface using tools like Streamlit.
Clustering techniques to group attractions by themes (e.g., religious, historical).

In conclusion, the Review-Based Place Recommendation System offers a practical and scalable solution for exploring similar attractions based solely on review insights, making it a valuable tool in the domain of travel recommendation services.

