This is a NLP task to summarise a conversation .

I have used pretrained transformers to execute it.

Firstly,the input file in the format of docx file  was made to read in python and then I extracted paragraphs from the file.

Then I made a loop which performs 2 objectives:

a) Forms the summary of the extracted paragraphs

b) Then determines the cosine similarity scores between the summarised statements and the original sentences.

I have taken 0.50 value as a threshold value for cosine similarity score to clssify any summary as an useful insight of the text.

So the the cosine similarity scores greater than 0.50 are significant to us.

Logic behind the cosine similarity score:

It takes a sentence and converts it to a vector.When we convert language into a machine-readable format, the standard approach is to use dense vectors.
A neural network typically generates dense vectors. They allow us to convert words and sentences into high-dimensional vectors — organized so that each vector's geometric position can attribute meaning.

Then it finds the smallest Euclidean or smallest angle i.e.cosine similarity between them.

Cosine similarity considers vector orientation, independent of vector magnitude.

Cosine similarity formula: 
Cos(x, y) = x . y / ||x|| * ||y||

Then I read the text file in the following format:

Paragraph:

Summary of the paragraph:

Insights of the paragraph:

Cosine similarity scores of summary with each Insight:

Only those insights were taken into consideration whose similarity scores were greater than 0.50.
