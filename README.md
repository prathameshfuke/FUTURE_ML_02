
# Movie Revenue Prediction

This project is designed to predict the revenue of movies based on various features like budget, runtime, release date, and genres. The data is preprocessed, and machine learning models are trained to predict the revenue of movies. The project includes data preprocessing, model training, and visualization components.

## Project Structure

The project is structured as follows:

```
project_root/
├── data/
│   ├── raw/                # Raw data files
│   └── processed/          # Processed data files
├── src/
│   ├── __init__.py         # Package initialization
│   ├── data_preprocessing.py  # Preprocessing script
│   ├── model_training.py      # Model training script
│   ├── visualization.py       # Visualization script
│   └── utils.py              # Utility functions
├── notebooks/               # Jupyter Notebooks for EDA and modeling
│   ├── EDA.ipynb
│   ├── Modeling.ipynb
│   └── Results.ipynb
├── models/                 # Folder to store trained models
├── plots/                  # Folder to store plots/graphs
├── reports/                # Folder to store reports
├── requirements.txt        # Project dependencies
└── README.md               # Project description
```

## Installation

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <project_root>
   ```

2. Set up a virtual environment (recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On macOS/Linux
   venv\Scriptsctivate      # On Windows
   ```

3. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### 1. Data Preprocessing

To preprocess the raw movie data, run the `data_preprocessing.py` script. This will clean and prepare the data for model training:

```bash
python src/data_preprocessing.py --filepath /path/to/raw/TMDB_movie_dataset_v11.csv
```

The script will generate a `processed_data.csv` file in the `/data/processed/` directory.

### 2. Model Training

Once the data is preprocessed, you can train the machine learning models using the `model_training.py` script:

```bash
python src/model_training.py
```

This script will train the models and output evaluation metrics such as RMSE, MAE, and R2.

### 3. Visualization

To visualize the data and model results, use the `visualization.py` script:

```bash
python src/visualization.py
```

This will generate various plots like feature importance, model performance, and other visualizations.

## Jupyter Notebooks

1. **EDA.ipynb**: Perform exploratory data analysis (EDA) on the raw data.
2. **Modeling.ipynb**: Train and evaluate models using the processed data.
3. **Results.ipynb**: Visualize the model's results and evaluation metrics.


To use this project, you need to download the dataset from Kaggle. Follow the steps below to download the dataset using the `kagglehub` Python library.

### Prerequisites

Make sure you have `kagglehub` installed. If not, you can install it by running:

```
pip install kagglehub
Downloading the Dataset
Once you have the required library installed, you can use the following Python script to download the dataset:

import kagglehub

# Download latest version
path = kagglehub.dataset_download("asaniczka/tmdb-movies-dataset-2023-930k-movies")

print("Path to dataset files:", path)
This script will download the dataset and provide the path to where the files are stored on your local machine.
```

Notes

Make sure to replace asaniczka/tmdb-movies-dataset-2023-930k-movies with the correct dataset identifier if using a different dataset.
The dataset will be saved in the specified location, and you can use it for your machine learning tasks.
After downloading, make sure to load the data in the appropriate format for use in the project.

css
Copy
Edit

This provides both the steps to install the necessary library and the script to download the dataset.

## Contributing

Feel free to fork the repository and submit pull requests with improvements, bug fixes, or new features. Ensure you write tests and update documentation as needed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
