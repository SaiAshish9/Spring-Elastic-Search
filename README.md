```
ES => NoSQL DB

ES Indexing and Retrieval:

how es indexes our data so that it can return result sets us in extremely low latency

how the search results in es rank acc. to relavance

Indexing is a technique in which es builds s index out of all the documents that are provided for the same

1. ES is able  to achieve low latency in responses because, instead of searching the text directly, it
searches in an index instead.

2. Document is a basic unit of data in es

3. Inverted index(look at the back of the book)

few terms will be listed there and the page no.'s where they can be found, it's exactly the way es quickly return us the search results.

es will be provided with a set of documents, it will tokenize the contents, split text into diff. words then it will create s unique set of all these
words which will be in sorted order. Only unique terms will be present at the set.

various types of NLP can be applied for tokenization which is fully configurable by the user and many stock words might have been removed from this
unique set after the we'll associate a list of documents with which the terms are found so we can see how easy it makes the search

similar to the index at the back of a book
```

```
how the search results sorted acc. to relavance:

Retrieving

Term Fequency (TF) : frequency of term in a given document

Document Fequency (DF) : frequency of term in all the documents

Inverse Document Frequency (IDF) : 1/DF

Doc1: I am learning the cool stuff
Doc2: I am learning to learn

Search term : learn

Relavance = TF * IDF

TF1 = 1
TF1 = 2
IDF = 1/(1+2) = 1/3

Rev1 = 1/3 , Rev2 = 2/3

Rev2 > Rev1 

when we search learn , it's more relavant in document 2 because it occurs there multiple times.

IDF is there to decrease the relavance of common terms like "The" in this case

Search Query: learning to code

Relavance of each term will be taken separately, added and search results will be ran.
```

https://www.elastic.co/guide/en/elasticsearch/guide/current/practical-scoring-function.html

<img width="650" alt="Screenshot 2023-03-12 at 9 44 18 PM" src="https://user-images.githubusercontent.com/43849911/224557568-8002cbe5-7520-463c-935b-e4df3bc983b6.png">

<img width="883" alt="Screenshot 2023-03-12 at 9 43 24 PM" src="https://user-images.githubusercontent.com/43849911/224557521-890ef4ad-acf8-4781-a261-fe2a7d1c7da6.png">

<img width="727" alt="Screenshot 2023-03-12 at 9 42 28 PM" src="https://user-images.githubusercontent.com/43849911/224557482-e35aa9d6-5851-4d7b-8e77-691827ddecb2.png">

<img width="733" alt="Screenshot 2023-03-12 at 9 36 11 PM" src="https://user-images.githubusercontent.com/43849911/224557163-c194c61c-2d5a-4a5c-b7f3-0e9fc83f996f.png">

<img width="756" alt="Screenshot 2023-03-12 at 9 32 52 PM" src="https://user-images.githubusercontent.com/43849911/224556966-2613d13d-2f3c-4f09-a1c6-814b1f2aa8f9.png">

<img width="1603" alt="Screenshot 2023-03-12 at 2 45 25 PM" src="https://user-images.githubusercontent.com/43849911/224535521-bf6364c8-d4bf-4f4f-9e87-cec906c77d6d.png">

```
docker-compose up
```

<img width="880" alt="Screenshot 2023-03-12 at 5 33 35 PM" src="https://user-images.githubusercontent.com/43849911/224543364-78534cd0-3e80-4138-88ce-5ad4294e3224.png">

<img width="876" alt="Screenshot 2023-03-12 at 5 33 54 PM" src="https://user-images.githubusercontent.com/43849911/224543380-9228d1c2-1f59-475f-9a92-227c8f8f9217.png">

<img width="863" alt="Screenshot 2023-03-12 at 5 34 11 PM" src="https://user-images.githubusercontent.com/43849911/224543405-eda8afb3-47c2-4e87-8295-329270553644.png">

```
create index and dataview with name springboot-test-log
```

```
sudo kill -9 $(sudo lsof -t -i:9001)

kill -9 $(lsof -t -i tcp:5000)

data views and index management
```

<img width="1586" alt="Screenshot 2023-03-12 at 7 05 44 PM" src="https://user-images.githubusercontent.com/43849911/224548196-9ede63dc-4ec3-42a5-a0a6-2d9d165d858f.png">

<img width="882" alt="Screenshot 2023-03-12 at 6 23 01 PM" src="https://user-images.githubusercontent.com/43849911/224545924-f69032bd-d8a5-479e-ba14-65493d892812.png">

<img width="1584" alt="Screenshot 2023-03-12 at 6 27 17 PM" src="https://user-images.githubusercontent.com/43849911/224546123-27ae572e-debf-4422-9c70-4b08eb130087.png">

<img width="1604" alt="Screenshot 2023-03-12 at 6 35 00 PM" src="https://user-images.githubusercontent.com/43849911/224546506-7c4539f7-2a62-465a-82a1-cd9f87fefa3a.png">

<img width="1589" alt="Screenshot 2023-03-12 at 6 36 33 PM" src="https://user-images.githubusercontent.com/43849911/224546590-bb1ea002-129e-4fe3-b964-0c46c76cdbda.png">

<img width="1383" alt="Screenshot 2023-03-12 at 6 55 17 PM" src="https://user-images.githubusercontent.com/43849911/224547641-a3c72018-6645-4249-900b-c39ff7adafd3.png">

<img width="1602" alt="Screenshot 2023-03-12 at 6 56 38 PM" src="https://user-images.githubusercontent.com/43849911/224547708-9078d0af-b88e-4c38-a7ad-1658200ae651.png">

<img width="1599" alt="Screenshot 2023-03-12 at 6 57 26 PM" src="https://user-images.githubusercontent.com/43849911/224547748-db596a46-67c5-403e-bbd4-94bbf24a3418.png">

<img width="1598" alt="Screenshot 2023-03-12 at 6 58 18 PM" src="https://user-images.githubusercontent.com/43849911/224547804-38d4b7c7-e47e-4e4d-a86d-21827a9efec6.png">

<img width="1596" alt="Screenshot 2023-03-12 at 6 59 02 PM" src="https://user-images.githubusercontent.com/43849911/224547835-7a533e10-6bea-4bae-9e23-df7d97330a6d.png">

<img width="921" alt="Screenshot 2023-03-12 at 7 01 55 PM" src="https://user-images.githubusercontent.com/43849911/224548005-ef34f264-4f55-4198-a361-c5cd068db0d7.png">

<img width="1233" alt="Screenshot 2023-03-13 at 9 37 24 PM" src="https://user-images.githubusercontent.com/43849911/224759741-0612f786-783d-459c-a8cd-466d6ad35834.png">

