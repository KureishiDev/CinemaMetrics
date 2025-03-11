# Movie Revenue Prediction Analysis

This project involves analyzing movie data to predict the revenue based on various features like budget, popularity, and runtime. The dataset includes movie details such as genre, budget, revenue, and more, obtained from the TMDB (The Movie Database) dataset.

The script performs data preprocessing, exploratory data analysis (EDA), advanced data visualization, and builds a simple predictive model using linear regression to estimate movie revenue.

## Project Structure

The script performs the following tasks:

### 1. Data Loading and Merging
- Loads movie data (`tmdb_5000_movies.csv`) and credits data (`tmdb_5000_credits.csv`) from CSV files.
- Merges both datasets into one DataFrame, combining movie and credit-related information.

### 2. Data Cleaning and Preprocessing
- Cleans the `revenue` column by replacing zero values with `NaN` and drops rows with missing `revenue` values.
- Converts string representations of lists in the `genres` and `keywords` columns into actual lists using `ast.literal_eval`.
- Extracts and stores genre and keyword names for better analysis.
- Creates a `release_year` column by extracting the year from the `release_date`.
- One-hot encodes genre information to use it as features in the model.

### 3. Exploratory Data Analysis (EDA)
- Visualizes the relationship between movie budget and revenue using a scatter plot.
- Analyzes the average revenue over the years and visualizes the trend using a line plot.

### 4. Advanced Data Visualization
- Uses Plotly for an interactive scatter plot to explore the relationship between movie budget and revenue, where hovering over data points shows the movie title.

### 5. Predictive Modeling
- Prepares the features and target variables for model training.
- Splits the dataset into training and testing sets (80/20 split).
- Trains a simple linear regression model to predict movie revenue based on `budget`, `popularity`, and `runtime`.
- Evaluates the model's performance using Mean Squared Error (MSE).

## Requirements

To run this script, you will need the following Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `ast`
- `plotly`
- `scikit-learn`

You can install them using pip:

pip install pandas numpy matplotlib seaborn plotly scikit-learn


## Data

The dataset used in this project is the TMDB 5000 Movie Dataset. It consists of information on 5000 movies, including their revenue, budget, runtime, genres, and more. The CSV files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`) are used as input data.

## Usage

1. Download the dataset files (`tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`).
2. Ensure the dataset is stored in the correct path (`../data/`).
3. Run the script to perform the analysis:

python movie_revenue_analysis.py


### Output

  - The script will display the following:
  - A scatter plot showing the relationship between movie budget and revenue.
  - A line plot showing the evolution of average movie revenue over time.
  - An interactive scatter plot of budget vs. revenue using Plotly.
  - The Mean Squared Error (MSE) of the linear regression model's prediction.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

