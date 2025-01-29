# **Product Name: AutoCorrect+ (AI-Enhanced Descriptive Answer Evaluation)**

## **Product Description** ##

Evaluating descriptive answers takes a long time and requires a lot of physical effort. It is prone to grader fatigue, partiality, and inconsistency caused by differing standards.  We have developed a solution to address the above mentioned concerns. Our automated grading system uses strong NLP and machine learning algorithms to deliver consistent grades for descriptive responses.

AutoCorrect+ uses a few natural language processing (NLP) packages and techniques to accurately assess descriptive answers. It employs NLTK for breaking text into smaller units (tokenization) and removing commonly used words (stop word removal). In addition to that, it also uses the scikit-learn (sklearn) package to calculate text similarity using methods like cosine similarity and Jaccard distance. By combining these NLP approaches, AutoCorrect+ establishes a solid foundation for evaluating descriptive answers effectively.

Moreover, AutoCorrect+ is integrated with the Django framework, which provides a user-friendly interfaces for both administrators and students. Administrators can login and manage user registrations, analyze exam results, and add or modify courses and questions through the interface. Similarly, students can easily register, log in, attempt exams, view their results, and update their profiles using the provided interface.

The aim of AutoCorrect+ is to enhance traditional manual grading methods by introducing efficiency, accuracy, and scalability to educational assessment systems using  NLP techniques and user-friendly interfaces.

The first step involves preparing the textual data by tokenizing the answers into individual words . Additionally, common stop words (e.g., "the," "and," "a") are removed from the tokenized texts to focus on the more meaningful words.

The preprocessed textual data is then converted into numerical vectors using the CountVectorizer from the scikit-learn library. This vectorization process captures the importance of words through their frequencies, allowing for a numerical representation of the text that can be used for similarity calculations.

Two complementary techniques are employed to measure the semantic similarity between a student's answer and the predefined correct answer:
Cosine similarity: This measure calculates the cosine of the angle between the answer vectors, indicating the degree of text similarity. Cosine similarity ranges from -1 to 1, with 1 indicating that the vectors are identical, and -1 indicating that they are diametrically opposed.

Jaccard Distance/Similarity: This measure calculates the distance or similarity between the unique sets of words in the two answers. The Jaccard distance is first computed, and then converted to a similarity score ranging from 0 to 1, where 1 indicates that the sets are identical, and 0 indicates that they are completely different.

The similarity scores obtained from the cosine similarity and Jaccard similarity measures are mapped to predefined grading ranges. These individual scores are then aggregated to derive a total score for the student's answer.

The application is developed using the Django web framework, which provides a user-friendly interface for administrators to manage user registrations, tests, and courses. Students can also access this interface to attempt exams and view their results.

CountVectorizer: CountVectorizer transforms text data into a numerical representation, allowing us to analyze and process it effectively.
Jaccard Distance: Think of this as a measure of how similar two sets are. Jaccard Distance helps us quantify the similarity between two texts based on the intersection and union of their words.
Cosine Similarity: Imagine it as a way to measure the angle between two vectors in a multi-dimensional space. Cosine Similarity helps us measure the similarity between two texts regardless of their size, making it a powerful tool for text analysis.

You can use Visual Studio code for frontend peojects. You need to install VSCode, ensure all plugins are installed successfully, and install Angular extension pack in extensions. 
Step -1 – In git, codespace install angular extensions pack
 ![image](https://github.com/user-attachments/assets/1694bb45-3ed9-487a-9d08-5eb901dd8268)

Step 2 - Go to your project repo and clone the repository into the git code space go to the integrated terminal and install angular cli use npm install -g @angular/cli

And check whether angular cli is installed successfully or not using ng --help


