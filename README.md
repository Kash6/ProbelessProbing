# ProbelessProbing

🧠 Probe-less Probing of BERT’s Layer-Wise Linguistic Knowledge
This project explores a novel approach called Probe-less Probing to analyze how different layers of BERT encode linguistic information. Rather than relying on external classifiers, we use masked word prediction as a behavioral signal to probe BERT’s internal understanding.

🔍 What We Did

Reimplemented the study using the STREUSLE 4.4 dataset, which includes rich lexical-semantic and syntactic annotations.

Ran layer-wise masked token prediction using BERT-base (12 layers).

Evaluated BERT’s ability to:

Predict the correct word.

Predict the correct part-of-speech (POS).

Analyzed accuracy trends across layers and calculated expected layers for different POS tags and multiword expressions using differential scoring.

📊 Key Findings

BERT achieves ~43.27% accuracy for masked word prediction and ~67.08% accuracy for POS tagging.

POS and word prediction accuracies increase with layer depth, peaking around layer 6–7.

Multiword expressions (MWEs) show different behavior, with later layers often performing better.

Our reproduction sometimes outperformed the original results, possibly due to model or tokenizer updates.

⚙️ Technologies Used

Hugging Face Transformers

Google Colab

Python (NumPy, pandas)

Stanza (for POS tagging)

Custom differential gain analysis

📁 Contributions

Akash Mehta: Analysis and computation of expected layers for various linguistic features across layers; result comparison.

Rithvik Reddy Sama: POS, word match accuracy, and layer gain calculations.
