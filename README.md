# token · lens

token · lens is an interactive interpretability bench that runs entirely in your browser. It demonstrates the core mechanics of Large Language Models (LLMs) by training a tiny transformer and a byte-pair tokenizer from scratch the moment the page loads.

## 🌟 Features

- **Live Training**: Watch a small transformer model learn to predict the next token in real-time.
- **BPE Tokenizer**: A Byte-Pair Encoding tokenizer trained live on a small corpus.
- **Attention Visualization**: Interactive arcs and matrices showing exactly how tokens "look back" at previous context.
- **Probability Heatmap**: Visual representation of the model's surprise (cross-entropy loss) for each token.
- **Embedding Map**: A 2D PCA projection of the model's learned embedding space, showing how it clusters similar tokens.
- **Generation**: A "continue writing" feature with adjustable temperature to see the model's predictions in action.
- **BPE Replay**: A slider to "undo" BPE merges and see how words shatter back into characters.

## 🚀 How it Works

The project is a self-contained HTML/JavaScript application. It implements:

1.  **Byte-Pair Encoding (BPE)**: Learns common character sequences from a hardcoded corpus to build a vocabulary.
2.  **Tiny Transformer**: A lightweight transformer architecture (1 layer, 2 heads) implemented in vanilla JavaScript using typed arrays for performance.
3.  **Training Loop**: Uses the Adam optimizer and cross-entropy loss to train the model directly in the browser's main thread.
4.  **PCA Projection**: Reduces the 32-dimensional embedding vectors to 2D for visualization.

## 🛠️ Installation & Usage

Since it is a single-file web application, no installation is required.

1.  Clone the repository:
    ```bash
    git clone <repository-url>
    cd token_lens
    ```
2.  Open `index.html` in any modern web browser.

## 📖 Educational Goals

This project is designed to make the "black box" of transformers transparent. It allows users to explore:
- How tokenization affects model input.
- The relationship between loss and predictability.
- The geometric nature of embeddings.
- How attention heads develop different "habits" (e.g., looking at the previous token vs. the start of the sentence).

## 📄 License

MIT
