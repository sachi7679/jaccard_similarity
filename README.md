# jaccard_similarity
A Python project to calculate the Jaccard Similarity between datasets
# Spelling Correction Using Jaccard Similarity

This project demonstrates a simple **Spelling Correction System** using **Jaccard Similarity** and **Character N-Grams** in Python.

## 📌 Project Overview

The objective of this project is to identify and correct misspelled words by comparing them with a predefined dictionary using the Jaccard Similarity algorithm.

The system:

- Generates character n-grams from words.
- Computes similarity scores between misspelled and correct words.
- Returns the closest matching word from the dictionary.

---

## 🚀 Features

✅ Character N-Gram generation  
✅ Jaccard Similarity implementation  
✅ Basic spelling correction system  
✅ Text preprocessing (lowercasing and removing special characters)  
✅ Improved correction for noisy inputs

---

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Regular Expressions (`re` module)

---

## 📂 Project Structure

```
Spelling-Correction-Using-Jaccard-Similarity/
│
├── Spelling Correction Using Jaccard Similarity.ipynb
└── README.md
```

---

## 🔍 How It Works

### 1. Create Character N-Grams

```python
def char_ngrams(word, n=2):
    word = word.lower()
    return [word[i:i+n] for i in range(len(word)-n+1)]
```

Example:

```python
char_ngrams("university")
```

Output:

```
['un', 'ni', 'iv', 've', 'er', 'rs', 'si', 'it', 'ty']
```

---

### 2. Calculate Jaccard Similarity

```python
def jaccard_similarity(a, b):
    set1 = set(a)
    set2 = set(b)
    return len(set1 & set2) / len(set1 | set2)
```

Formula:

\[
J(A,B)=\frac{|A \cap B|}{|A \cup B|}
\]

---

### 3. Correct Misspelled Words

Example input:

```python
wrong_word = ["recieve", "freind", "lernning", "machin", "scince"]
```

Sample output:

```
recieve ---> receive
freind ---> friend
lernning ---> learning
machin ---> machine
scince ---> science
```

---

## 🧹 Text Preprocessing

The project also includes preprocessing to remove unwanted characters and convert text to lowercase.

```python
def preprocessing(word):
    word = word.lower()
    word = re.sub(r'[^a-z]', '', word)
    return word
```

Example:

```python
preprocessing("Company#5")
```

Output:

```
company
```

---

## 📈 Future Improvements

- Use a larger dictionary dataset.
- Add support for edit distance algorithms.
- Develop a GUI or web application.
- Integrate with NLP libraries for better accuracy.

---

## 🤝 Contributing

Contributions are welcome. Feel free to fork this repository and submit a pull request.

---

## 📜 License

This project is open-source and available under the MIT License.

---

### ⭐ If you found this project useful, please give it a star on GitHub.
