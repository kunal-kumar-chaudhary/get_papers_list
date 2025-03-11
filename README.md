# Get Papers List

A Python CLI tool designed to fetch research papers from PubMed based on a user-specified query. It identifies papers authored by individuals affiliated with pharmaceutical or biotech companies and exports the results as a CSV file.

## Features

- Fetches research papers using PubMed's powerful API.
- Filters papers to identify authors affiliated with pharmaceutical/biotech companies.
- Outputs detailed information in CSV format.
- Customizable command-line options for output and debugging.

## Installation

This project uses [Poetry](https://python-poetry.org/) for dependency management.

1. **Install Poetry** (if not already installed):

```bash
curl -sSL https://install.python-poetry.org | python3 -
```

2. **Clone the repository**:

```bash
git clone https://github.com/yourusername/get-papers-list.git
cd get-papers-list
```

3. **Install dependencies**:

```bash
poetry install
```

## Usage

Use the CLI tool directly via Poetry:

```bash
poetry run get-papers-list "your search query"
```

### Options

- `-f` or `--file`: Specify the filename to save the results (default prints to console).
- `-d` or `--debug`: Enable debug mode to see detailed execution logs.
- `-h` or `--help`: Show help message and usage instructions.

### Example

```bash
poetry run get-papers-list "COVID-19 vaccine efficacy" --file results.csv --debug
```

## CSV Output Structure

The CSV file will contain the following columns:

- **PubmedID**: Unique identifier for the paper.
- **Title**: Title of the research paper.
- **Publication Date**: Date when the paper was published.
- **Non-academic Author(s)**: Names of authors affiliated with pharmaceutical/biotech companies.
- **Company Affiliation(s)**: Names of the affiliated companies.
- **Corresponding Author Email**: Email address of the corresponding author (if available).

## Project Structure

```
get-papers-list/
├── pyproject.toml
├── README.md
├── main.py
└── get_papers_list/
    ├── __init__.py
    ├── fetch.py
    ├── parse.py
    └── cli.py
```

## Dependencies

- [Requests](https://docs.python-requests.org/en/latest/)
- [Pandas](https://pandas.pydata.org/)
- [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)

## Contributing

Contributions are welcome! Please open issues or submit pull requests via GitHub.