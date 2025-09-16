# NLP-homework11. Q1_REGEX.ipynb – Regex Patterns in Python
##1. Q1_REGEX.ipynb – Regex Patterns in Python
Problem Statement:
Implement regex patterns to match and extract different text structures.
Approach:
Designed regex rules to capture U.S. ZIP codes, words without capital letters, numbers with special formats, email variations, interjections, and question-mark-terminated lines.
Results:
Correctly extracted matches for each category.
Demonstrated flexibility of regex in handling diverse text structures.
Conclusion:
Regular expressions are a powerful tool for text cleaning and validation. With careful design, regex can handle structured and semi-structured text effectively, though it requires attention to edge cases.

##Q2_PROGRAMMING_QUESTION.ipynb – Tokenization Exercise
Problem Statement:
Manually and automatically tokenize a paragraph, then compare methods.
Approach:
Applied naïve space-based tokenization.
Built a manually corrected token list.
Compared with spaCy’s English tokenizer.
Discussed multiword expressions (MWEs) and tokenization challenges in morphologically rich languages.
Results:
Naïve approach mishandled punctuation and contractions.
SpaCy performed better but still differed from manual corrections.
MWEs showed the limitations of both approaches.
Conclusion:
Tokenization is more than splitting text by spaces—it requires linguistic awareness. Tools like spaCy improve accuracy, but MWEs and complex languages highlight the need for customized tokenization strategies.

##3. Q3_Manual_BPE_on_a_toy_corpus.ipynb – Byte Pair Encoding (BPE)
Problem Statement:
Manually implement Byte Pair Encoding (BPE) to explore subword tokenization.
Approach:
Started with character-level vocabulary.
Iteratively merged frequent symbol pairs.
Applied BPE on toy datasets (low, lowest, newer, wider, new) and on a paragraph.
Results:
Discovered subwords like learn, process and suffixes like -ing, -est.
Efficiently handled unseen words like deepest → deep + est.
Reduced vocabulary size but sometimes split morphemes unnaturally.
Conclusion:
BPE strikes a balance between word-level and character-level models, making it practical for real NLP systems. It improves handling of rare words, though it sacrifices some linguistic naturalness in splits

4. Q4_WORD_PAIR.pdf – Edit Distance Problem
Problem Statement:
Transform “Sunday” → “Saturday” using edit operations under two cost models.
Approach:
Model A: Substitution = 1, Insertion = 1, Deletion = 1
Model B: Substitution = 2, Insertion = 1, Deletion = 1
Steps: Insert a, insert t, substitute n → r.
Results:
Model A → Edit Distance = 3
Model B → Edit Distance = 4
Conclusion:
Edit distance provides a measurable way to evaluate string similarity. By adjusting cost models, it adapts to different domains:
In spell-checking, substitutions can be treated as cheap.
In bioinformatics, substitutions can be treated as costly to model rare mutations.
