Toy transformer
=================

This repo contains a couple of jupyter notebooks that implement a basic self-attention mechanism. 

In the best "spherical cow" spirit, I skip the preprocessing steps of converting a token into an embedding vector. I simply initialize vectors of a certain embedding dimension with random numbers as components, according to the number of tokens provided. There is no MLP components here, and only one attention head.

📄`attention.ipynb`  
Implements self-attention for queries: attention scores, weights, context. All in numpy. No q,k,v arrays involved. 

📄`scaled-dot-p.ipynb`  
Scaled-dot product attention using weight matrices and query, key value arrays $q$, $k$, $v$ in numpy. Dumb `softmax`. For studying purposes.

📄`scaled-dot-p_comparison.ipynb`  
Same as the previous notebook, but this time compares with numpy and pytorch implementations to check for correctness. 

📄`QK-OV.ipynb`  
Inspired by the tensor calculus formulation of an attention head by [Elhage+2021](https://transformer-circuits.pub/2021/framework/index.html), here I compute the QK and OV matrices. I also implement bigrams and skip-trigrams for pedagogical purposes.