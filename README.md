# Urdu Poetry Generator using N-gram Models

This project is a poetry generation tool designed to create Urdu poems using n-gram language models. The generator is trained on a corpus of Urdu poetry from poets like Faiz, Ghalib, and Iqbal. It uses unigram, bigram, and trigram models to produce a poem with three stanzas, each containing four verses.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithm](#algorithm)
- [Challenges](#challenges)
- [Example Output](#example-output)
- [Contributing](#contributing)
- [License](#license)

## Features

- Generates Urdu poetry based on n-gram language models (unigram, bigram, trigram).
- Produces poems with three stanzas, each containing four verses with 7–10 words.
- Allows rhyming of verses (optional bonus feature).
- Utilizes Conditional Frequency Distribution (CFD) to select the most probable next word.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Hasnain2430/Urdu-Poetry-Generator.git
   ```

2. Install the required libraries:
   ```bash
   pip install nltk
   ```

3. Download NLTK data (if not already downloaded):
   ```python
   import nltk
   nltk.download('punkt')
   ```

4. Place the Urdu poetry corpus file (e.g., `ghalib.txt`) in the root directory.

## Usage

1. Run the script (`urdu_poetry_generator.py`) in a Python environment.
2. At the start of the script, you will be prompted to input the first word for the poem.
3. The script will generate a poem with three stanzas, each containing four verses. Each verse will have a randomly generated length between 7 and 10 words.

## Algorithm

The poetry generation follows these main steps:

1. **Load the Poetry Corpus**: The script loads an Urdu poetry corpus and cleans the text by removing punctuation.
2. **Tokenize the Corpus**: The corpus is split into individual words for analysis.
3. **Generate n-gram Models**: Unigram, bigram, and trigram models are created using NLTK.
4. **Generate Verses**:
   - For each stanza and each verse:
     - A random verse length is selected (between 7–10 words).
     - The first word is either user-provided or chosen from common words in the corpus.
     - Using bigram or trigram probabilities, subsequent words are generated until the verse reaches the desired length.
     - [Bonus] Rhyming can be implemented by creating a custom dictionary for rhyming words.
5. **Print Stanzas**: Each stanza is printed with an empty line separating it from the next stanza.

## Challenges

This project presents several challenges:
- **Word Prediction**: Selecting the next word based on the previous word(s) requires carefully computed probabilities. Conditional Frequency Distribution (CFD) is used to determine the likelihood of each possible next word.
- **Rhyming Verses**: Rhyming adds complexity, as Urdu words do not follow English phonetic patterns. A custom rhyming dictionary may be needed.
- **Urdu Right-to-Left Text**: Urdu is written right-to-left, so it is crucial to handle text directionality properly.

## Example Output

The script will output three stanzas of Urdu poetry with each stanza containing four verses. For instance:

```
دل سے نکال یاس کہ زندہ ہوں میں ابھی،
ہوتا ہے کیوں اداس کہ زندہ ہوں میں ابھی،
مایوسیوں کی قید سے خود کو نکال کر،
آ جاؤ میرے پاس کہ زندہ ہوں میں ابھی،

...

```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request to improve the project.
