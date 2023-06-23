# Github_Automated_Analysis

## Introduction
This project provides an analysis of user repositories fetched from GitHub using Python code. The code retrieves repository information, downloads files, tokenizes their content, and calculates metrics for each repository. The project highlights the most complex repository based on the calculated complexity score.

## Code Explanation
The code performs the following tasks:

1. Fetching User Repositories:
   - The `fetch_user_repositories(github_url)` function extracts the username from the GitHub URL and constructs the API endpoint URL.
   - It sends a GET request to the GitHub API and processes the response to retrieve repository information.
   - The repository name and URL are printed for each repository.

2. Repository URL List:
   - The code initializes an empty list, `repository_urls`, to store the URLs of user repositories.

3. Fetching User Repositories:
   - The `fetch_user_repositories(github_url)` function is called, which populates the `repository_urls` list with repository URLs.

4. Importing Libraries:
   - The required libraries, including `requests`, `nltk`, and `pandas`, are imported for data retrieval, natural language processing, and data manipulation tasks.

5. File Extensions:
   - The code defines a list of file extensions (e.g., `.py`, `.ipynb`, `.md`) that will be considered for processing.

6. Tokenized Data:
   - An empty list, `data`, is created to store the tokenized data from repositories.

7. Processing Repositories:
   - The code iterates over the repository URLs in the `repository_urls` list.
   - For each URL, the code constructs the API URL by replacing "github.com" with "api.github.com/repos".
   - A GET request is sent to the API to retrieve the repository data.
   - The code creates a folder for the repository and checks for files with desired extensions.
   - For each file, its content is downloaded, saved to a file, tokenized, and added to the `data` list.

8. Creating a DataFrame:
   - The code creates a DataFrame, `df`, from the `data` list, containing repository names and tokenized data.

9. Data Preprocessing:
   - Stopwords and punctuation removal is performed on the tokenized data in the DataFrame using NLTK.
   - A function is defined to remove stopwords and punctuation, which is then applied to the "Tokens" column.

10. Metric Calculation:
    - The code calculates several metrics for each repository in the DataFrame, such as total tokens, unique token count, and average token length.
    - A complexity score is calculated based on the metrics.

11. Most Complex Repository:
    - The code identifies the repository with the highest complexity score and prints its name.

## Results and Findings
Based on the analysis of user repositories, the code identified the most complex repository as [most_complex_repository]. This repository exhibits a high complexity score, indicating potentially intricate code or extensive content.

## Conclusion
The Python code presented in this analysis project demonstrates a workflow for fetching user repositories from GitHub, extracting relevant information, and performing tokenization and metric calculations. The code provides valuable insights into the complexity of different repositories, aiding in further analysis or decision-making processes.
