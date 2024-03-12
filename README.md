# Ray Distributed Computing with FastEmbed and Qdrant

This repository contains code to demonstrate the usage of Ray distributed computing framework along with FastEmbed for embedding generation and Qdrant for similarity search. Specifically, it shows how to efficiently generate embeddings for text data, store them in Qdrant, and perform similarity search queries.

## Requirements
- Python 3.x
- Jupyter Notebook (for running `RayQdrant.ipynb`)
- PyPDF2
- nltk
- ray
- fastembed
- qdrant_client

You can install the required libraries using pip:

```bash
pip install PyPDF2 nltk fastembed qdrant-client[fastembed]
pip install -U "ray[data,train,tune,serve]"
```

## Usage

1. **Clone the Repository:**
   
   Clone this repository to your local machine:

   ```bash
   git clone https://github.com/yash9439/RayQdrantFastEmbed.git
   ```
   
2. **Start Docker Environment:**

   Open the `RayQdrant.ipynb` file using Jupyter Notebook:

   ```bash
   sudo docker pull qdrant/qdrant
   sudo docker run -p 6333:6333 -p 6334:6334 -v $(pwd)/qdrant_storage:/qdrant/storage:z qdrant/qdrant
   ```

3. **Run Jupyter Notebook:**

   Open the `RayQdrant.ipynb` file using Jupyter Notebook:

   ```bash
   jupyter notebook RayQdrant.ipynb
   ```

   Execute each cell in the notebook sequentially to run the code. Ensure you have the necessary dependencies installed.

4. **Interpret Results:**

   After running the notebook, you will see the time taken for embedding generation using Ray distributed computing. Additionally, you'll get the results of similarity search queries using Qdrant.

## Folder Structure

- **Docs/**: This directory contains the PDF documents for which embeddings are generated.
- **RayQdrant.ipynb**: Jupyter Notebook containing the code for embedding generation using Ray and similarity search using Qdrant.

## License

This code is provided under the Apache License 2.0.

Feel free to modify and distribute it as needed. If you find any issues or have suggestions for improvements, please feel free to open an issue or create a pull request.
