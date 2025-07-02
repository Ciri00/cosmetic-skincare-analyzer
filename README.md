# Cosmetic Skincare Analyzer

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Libraries](https://img.shields.io/badge/Libraries-scikit--learn%2C%20Bokeh%2C%20Pandas%2C%20Numpy%2C%20Matplotlib%2C%20Seaborn%2C%20TextBlob-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## 🌟 Project Overview

This project presents a **comprehensive cosmetic ingredient analysis system** designed to empower consumers with data-driven insights into skincare products, particularly moisturizers suited for dry skin. Leveraging **machine learning** and **interactive visualizations**, the system evaluates and compares products based on their ingredient composition, safety, and effectiveness.

The core idea is to transform complex ingredient lists into actionable information, helping users make informed and safer product choices.

##  Key Features

- **Ingredient-Level Analysis**: Detailed breakdown and analysis of cosmetic ingredients.
- **Allergen Identification**: Flags common undesirable ingredients (e.g., alcohol, fragrance, parabens) to help users avoid potential irritants.
- **Product Similarity & Clustering**: Uses t-SNE and K-Means clustering to visualize and group products with similar ingredient profiles.
- **Interactive Dashboard (Bokeh)**: An intuitive web-based tool allowing users to:
  - Explore product clusters.
  - View product details on hover.
  - Compare two products side-by-side based on ingredients, price, and safety.
- **Predictive Modeling**: Machine learning models (Linear Regression, Random Forest) trained to predict product ratings based on engineered features like ingredient count, price per ingredient, and allergen presence.
- **Sentiment Analysis**: Calculates polarity scores based on ingredient composition and synthetic review generation to understand perceived product quality.
- **Content-Based Recommendation System**: Helps users discover alternative products matching their skin type and preferences.

##  Dataset

The project is built on a dataset of **1,472 cosmetic products from Sephora**, focusing on moisturizers suitable for dry skin. Key attributes include:

- **Brand**
- **Product Name**
- **Price**
- **User Rating (Rank)**
- **Ingredient Lists**
- **Skin Types**

## 🛠 Technical Workflow

The system employs a robust data science pipeline:

1. **Ingredient Tokenization**: Breaking down ingredient strings into individual tokens.
2. **One-Hot Encoding**: Converting ingredient lists into binary vectors for machine learning.
3. **Document-Term Matrix (DTM)**: Creating a matrix representing products and their ingredient presence.
4. **Dimensionality Reduction (t-SNE)**: Reducing high-dimensional ingredient data to 2D for visualization.
5. **Cosine Similarity**: Measuring ingredient-based similarity between products for comparison.
6. **K-Means Clustering**: Grouping similar product formulations.
7. **Feature Engineering**: Creating new features like `Ingredient Count`, `Price per Ingredient`, `Has_Fragrance`, `Has_Parabens`.
8. **Predictive Modeling**: Training and evaluating Linear Regression and Random Forest models to predict product ratings.
9. **Sentiment Analysis**: Analyzing ingredient polarity and synthetic reviews.
10. **Interactive Visualization (Bokeh)**: Developing the user-facing dashboard.

## 📈 Analysis & Insights

The project provides several key insights:

- **Most Common Ingredients**: Water, Glycerine, and Dimethicone are highly prevalent.
- **Brand-Independent Similarity**: Products cluster based on ingredients, not just brand.
- **Price vs. Ingredients**: Higher ingredient counts do not always equate to higher prices; lower-cost products can have identical ingredient profiles to expensive ones.
- **Allergen Distribution**: Alcohol and fragrance are the most common potential irritants (found in ~40% and ~30% of products respectively), while parabens, phthalates, sulfates, and formaldehyde show minimal presence.
- **Sentiment Alignment**: Sentiment scoring based on ingredients and synthetic reviews aligns closely with actual product perceptions.

##  Getting Started

### Prerequisites

- Python 3.8+
- `pip` package manager

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/cosmetic-skincare-analyzer.git
    cd cosmetic-skincare-analyzer
    ```

2. **Create a virtual environment (recommended):**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install the required libraries:**

    ```bash
    pip install -r requirements.txt
    ```

    *(Note: You'll need to create a `requirements.txt` file by running `pip freeze > requirements.txt` after installing all libraries used in your notebooks.)*

### Running the Project

The core analysis and dashboard are implemented in Jupyter Notebooks:

- `notebook.ipynb`: Contains the main preprocessing, analysis, and model training.
- `dashboard.ipynb`: Contains the code for the Bokeh-powered interactive dashboard.

To run the notebooks:

```bash
jupyter notebook
 ```

Project Structure
.
├── data/
│   ├── cosmetics.csv             # Raw dataset
│   ├── moisturizers_dry.csv      # Filtered dataset (moisturizers for dry skin)
│   ├── ingredient_matrix.npy     # Binary ingredient vectors
│   └── corpus.npy                # Tokenized ingredient lists
├── notebook.ipynb                # Main preprocessing, analysis, and model training
├── dashboard.ipynb               # Bokeh interactive dashboard implementation
├── cosmetic_analysis_report.md   # Generated project report
├── README.md                     # This file
└── requirements.txt              # Python dependencies

##  Future Enhancements

*   **Real-time User Inputs**: Allow users to input allergies or preferences for personalized recommendations.
*   **Product Image Display**: Integrate product visuals alongside ingredient information.
*   **Web Deployment**: Launch the system as a public web tool for broader accessibility.
*   **Real-time Allergen Detection**: Implement a feature for instant allergen flagging.
*   **Mobile Integration**: Develop a mobile application for on-the-go analysis.

##  Contributing

Contributions are welcome! If you have suggestions for improvements or new features, please open an issue or submit a pull request.


##  License

This project is licensed under the **MIT License**.  
See the [LICENSE](LICENSE) file for details.


##  Contact

For any inquiries, please reach out to [LinkedIn](https://www.linkedin.com/in/Maeghasree)  
