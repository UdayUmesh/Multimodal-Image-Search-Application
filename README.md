# Multi-Modal Image Search Application

This project implements a multi-modal image search application using CLIP (Contrastive Language-Image Pre-Training) model and MyScale vector database. The application can process both text and image inputs to find relevant images from the Unsplash-25k dataset.

## Features

- Multi-modal search: Combine text and image inputs for more accurate search results
- Utilizes CLIP model from Hugging Face for generating embeddings
- Stores and queries vector embeddings using MyScale database
- Supports image-only and text-only searches as well

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- CLIP (Contrastive Language-Image Pre-Training) model
- MyScale vector database
- Unsplash-25k dataset

## Setup and Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-username/multimodal-image-search.git
   cd multimodal-image-search
   ```

2. Install the required packages:
   ```
   pip install datasets clickhouse-connect requests transformers torch tqdm pandas matplotlib pillow
   ```

3. Download and extract the Unsplash-25k dataset:
   ```
   wget https://unsplash-datasets.s3.amazonaws.com/lite/latest/unsplash-research-dataset-lite-latest.zip
   unzip unsplash-research-dataset-lite-latest.zip -d tmp
   ```

4. Set up a MyScale account and create a cluster. Update the connection details in the script.

## Usage

1. Run the main script to process the dataset and store embeddings in MyScale:
   ```
   python process_dataset.py
   ```

2. Use the search functionality:
   ```
   python search_images.py --text "A man standing on the beach" --image_url "https://example.com/image.jpg"
   ```

## Project Structure

- `process_dataset.py`: Script to process the Unsplash dataset and store embeddings in MyScale
- `search_images.py`: Script to perform multi-modal image search
- `utils.py`: Utility functions for image processing and embedding generation

## Future Improvements

- Implement a web interface for easier user interaction
- Optimize embedding generation for larger datasets
- Explore advanced techniques for combining text and image embeddings

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).
