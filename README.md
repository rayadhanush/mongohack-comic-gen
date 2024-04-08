# Comic Strip Generator

This project generates extended scenes from any given story, visualizes them in the style of anime comic strips, and combines them into a unified image. The generation pipeline leverages advanced NLP and image generation models to produce creative outputs. We have a RAG-based model that will enhance the story using a vectorized DB of books and scripts.

## Usage

1. **Extend Story:** Query the system with a prompt like:

```
Take the ending of the Pokémon story, extend the story, and write dialogues.
```

2. **Generate Comic Strip:** Visualize the extended scenes as comic strips.

![Comic Strip](assets/comic_strip.png)

## Project Overview

The Comic Strip Generator utilizes a combination of NLP and deep learning models to extend stories and generate visually appealing anime-style comic strips. The project follows a multi-step process to achieve the following:

1. **Story Extension**: Using a RAG-based model and vectorized database of books and scripts, the system enhances the original story by generating additional scenes.
2. **Image Generation**: The extended scenes are visualized into anime-style comic strips using an image generation model.
3. **Image Compilation**: All generated comic strips are combined into a single, cohesive image for easy viewing.

### Key Components:

1. **Vectorized Database (RAG Model)**:

   - Enhances the story by retrieving related information and generating new scenes.
   - Uses the `BAAI/bge-large-en-v1.5` embedding model for accurate story enhancements.

2. **Text to Image**:

   - The extended story scenes are fed into a Hugging Face model for image generation, using anime-style prompts to create a unique visual representation.

3. **Comic Strip Creation**:
   - The generated comic strips are stitched together and overlaid with the story text in a visually appealing way, resulting in a comic strip-style image.

## Models Used

### Embedding Model

- **Model**: `BAAI/bge-large-en-v1.5`
- **Capabilities**:
  - Multilingual support, including Chinese.
  - Ideal for medical dialogue datasets like [MedDialog](<https://paperswithcode.com/dataset/meddialog#:~:text=Medical%20Dialogue%20Datasets-,The%20MedDialog%20dataset%20(Chinese)%20contains%20conversations%20(in%20Chinese),more%20dialogues%20will%20be%20added.>).

### Language Model

- **Model**: `Mistral-7B-Instruct-v0.2`
- **Features**:
  - Fine-tuned instruct version.
  - Enhanced generation capabilities for interactive storytelling.
