# Sentiment Book Recommender

The **Sentiment Book Recommender** project leverages **Large Language Models (LLMs)** to recommend books based on their description, category, and tone (e.g., happy, sad, etc.). This project demonstrates how to use LLMs in combination with vector search, text classification, and sentiment analysis to build a sophisticated recommendation system.

## Project Structure

The project is divided into several parts to explain each component and its functionality clearly:

1. **Part 1: EDA and Data Cleaning** (`data_exploration.ipynb`)
   - This part explores the dataset and performs necessary data cleaning steps, including handling missing values, removing duplicates, and formatting text fields for further processing.

2. **Part 2: Theory about LLMs and How They Work** (`LLM Notes`)
   - Provides a comprehensive theoretical background on Large Language Models, their working principles, and how they can be applied to text-based tasks such as book recommendations.

3. **Part 3: Creating the Vector Search Database** (`vector_search.ipynb`)
   - Creates a vector search database using embeddings generated from book descriptions, enabling efficient semantic search for similar books.

4. **Part 4: Text Classification for Categories** (`text_classification.ipynb`)
   - Uses machine learning to classify books into different categories based on their descriptions. This enables the recommender system to provide more specific and targeted suggestions.

5. **Part 5: Sentiment Analysis for Tone** (`sentiment_analysis.ipynb`)
   - Performs sentiment analysis on book descriptions to identify their tone (e.g., happy, sad, etc.), which helps refine book recommendations based on the user's mood or emotional preferences.

6. **Part 6: Creating a Dashboard** (`gradio_dashboard.py`)
   - Creates an interactive dashboard using **Gradio** to allow users to interact with the recommendation system and receive personalized book suggestions based on description, category, and tone.

## Technologies Used

- **Python**: The primary programming language for implementing the project.
- **LangChain**: A framework used for integrating LLMs with various tools and workflows.
- **OpenAI**: For using GPT-based models to generate embeddings and perform sentiment analysis.
- **Hugging Face**: Provides pre-trained models for text classification and sentiment analysis.
- **Gradio**: Used for building the interactive dashboard to showcase the book recommender.
- **Pandas**: For data manipulation and analysis.
- **Scikit-learn**: For machine learning tasks like text classification.

## Dataset

The project uses the **7k Books Dataset**, which includes information about books such as:

- ISBN
- Title
- Description
- Category
- Sentiment

This dataset is publicly available on Kaggle and provides the foundation for book recommendations.

## Steps to Run the Project

### Prerequisites

Make sure you have the following dependencies installed:

- Python 3.7 or later
- `pip` for package management

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/kishita1810/Semantic-book-recommender.git
    cd sentiment-book-recommender
    ```

2. Set up a virtual environment:

    ```bash
    python -m venv book-recommender
    source book-recommender/bin/activate  # On Windows use `book-recommender\Scripts\activate`
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Make sure you have an OpenAI API key set up in a `.env` file:

    ```bash
    OPENAI_API_KEY=your-openai-api-key
    ```

### Running the Project

Once the setup is complete, you can run the different parts of the project:

1. **Part 1: EDA and Data Cleaning**

    ```bash
    jupyter notebook data_exploration.ipynb
    ```

2. **Part 2: Theory about LLMs and How They Work**

    Read the notes in `LLM Notes`.

3. **Part 3: Creating the Vector Search Database**

    ```bash
    jupyter notebook vector_search.ipynb
    ```

4. **Part 4: Text Classification for Categories**

    ```bash
    jupyter notebook text_classification.ipynb
    ```

5. **Part 5: Sentiment Analysis for Tone**

    ```bash
    jupyter notebook sentiment_analysis.ipynb
    ```

6. **Part 6: Creating a Dashboard**

    ```bash
    python gradio_dashboard.py
    ```

    This will start a local web server at `http://127.0.0.1:7860` where you can interact with the book recommender.

## How It Works

1. **Data Preprocessing**: The data is cleaned and preprocessed to ensure it is in a usable format for building the recommendation system.
2. **Vector Search Database**: The descriptions of books are converted into embeddings using OpenAI's models and stored in a vector database to allow semantic search.
3. **Text Classification**: Books are categorized using a classification model that analyzes the book description and assigns categories (e.g., fiction, non-fiction).
4. **Sentiment Analysis**: The tone of each book's description is analyzed to classify it as happy, sad, etc.
5. **Recommendation**: Based on the user's input (description, category, tone), the system retrieves and recommends books with similar descriptions and appropriate tones.

## Conclusion

The **Sentiment Book Recommender** is an interactive and personalized book recommendation system that uses cutting-edge NLP techniques to analyze and recommend books based on descriptions, categories, and emotional tone. This project demonstrates how LLMs and vector search can be combined with traditional machine learning models to create a powerful recommendation system.

Feel free to explore and modify the project as needed. Happy coding!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
