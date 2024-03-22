# text to Neo4j Graph Database Project

## Introduction
This project is designed to showcasing how to transform text data from Wikipedia articles about movies into a structured Neo4j graph database. Using ChatGPT, the code extracts detailed information about movie casts, including actor names, their roles, and the movie title, and then formats this information into a Neo4j-compatible graph structure.

## Project Significance

-   **Enhanced Data Structure:** By converting unstructured text into a graph database, the project ensures more structured and reliable data retrieval.
-   **Reduced Hallucination:** The structured nature of graph databases helps in providing more accurate and contextually relevant data to the RAG model, potentially decreasing the chance of generating incorrect or hallucinated information.
-   **RAG Model Improvement:** This approach can be seen as a refinement or a supplementary method for the RAG model, especially in applications where data accuracy and structure are crucial.

## Features
-   Extraction of cast information from text files containing Wikipedia movie articles.
-   Identification and structuring of actor/actress names, their roles, and associated movie titles.
-   Conversion of this information into a JSON format with fields 'name', 'role', and 'movie' under the element 'cast'.
-   Strict adherence to data integrity: no imputation of missing values and no missing out on any actor-related information.

## How It Works
The script reads text files containing movie articles from Wikipedia. It then processes these articles to extract the cast section using ChatGPT. The extracted information is structured into JSON format and subsequently converted into a DataFrame. This DataFrame is then used to populate a Neo4j graph database.

## Example of unstructured data

> Leonardo DiCaprio as Dom Cobb, a professional thief who specializes in
> conning secrets from his victims by infiltrating their dreams.
> DiCaprio was the first actor to be cast in the film. Both Brad Pitt
> and Will Smith were offered the role, according to The Hollywood
> Reporter. Cobb's role is compared to "the haunted widower in a Gothic
> romance".
> 
> Ken Watanabe as Saito, a Japanese businessman who employs Cobb for the
> team's mission. Nolan wrote the role with Watanabe in mind, as he
> wanted to work with him again after Batman Begins.: 10  Inception is
> Watanabe's first work in a contemporary setting where his primary
> language is English. Watanabe tried to emphasize a different
> characteristic of Saito in every dream level: "First chapter in my
> castle, I pick up some hidden feelings of the cycle. It's magical,
> powerful and then the first dream. And back to the second chapter, in
> the old hotel, I pick up [being] sharp and more calm and smart and
> it's a little bit [of a] different process to make up the character of
> any movie".


## Graph database output

After transforming the unstructured data into a Pandas DataFrame, we are now capable of creating a graph database using Cypher syntax.

![](https://github.com/PetePhuaphan/text-to-neo4j-graph/blob/main/visualisation.png)
