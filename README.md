# Job Keywords Finder

This Python script allows users to find the top 10 most common words from a job description. You can use these keywords in your cover letter or resume to increase your chances of being hired. The idea came from the Sportsgrad podcast, where the host emphasized the importance of reading the job description multiple times. This script instantly identifies the most frequently used words and returns them to the user.

## Requirements

- Python 3.x
- NLTK
- Pandas

## Installation

1. Clone the repository or download the script.

2. Install the required Python libraries:
    ```bash
    pip install nltk pandas
    ```

3. Download the necessary NLTK data:
    ```python
    import nltk
    nltk.download('stopwords')
    nltk.download('punkt')
    nltk.download('wordnet')
    nltk.download('averaged_perceptron_tagger')
    nltk.download('omw-1.4')
    ```

## Usage

1. Ensure your job descriptions are in a CSV file with a column named `Job Description`.

2. Modify the script with your input and output file paths:
    ```python
    input_file_path = 'joblist.csv'  # Replace with your input CSV file path
    output_file_path = 'updated_joblist.csv'  # Replace with your output CSV file path
    ```

3. Run the script. The updated CSV file will contain a new column `Top 10 Keywords` with the top 10 most common words for each job description.

## Customization

- You can add more words to the `custom_words` set if there are specific words you want to exclude from the keyword analysis. For example, words like "help", "get", "work", and "responsibility" are excluded as they often appear in job descriptions but do not carry significant meaning.

## Example

```python
# Example usage
input_file_path = 'joblist.csv'  # Replace with your input CSV file path
output_file_path = 'updated_joblist.csv'  # Replace with your output CSV file path
process_csv(input_file_path, output_file_path)
