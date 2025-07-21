# BMC_Extractor
AI-Powered BMC Extraction from Research Articles

💡 What It Does 

Automatically extracts BMC segments (e.g., Value Proposition, Revenue Streams) from PDFs. 

Uses Zero-Shot learning to classify sentences without needing prior training on BMC-specific data. 

Summarizes each BMC block using Latent Semantic Analysis (LSA) for a clear, concise overview. 

 

🧠 About Zero-Shot Learning 

Zero-Shot learning enables models to classify data into categories they’ve never been explicitly trained on by leveraging pre-trained language understanding (e.g., facebook/bart-large-mnli). It’s ideal when labeled data is limited or unavailable. 

 

⚙️ How It Works 

Setup & Dependencies 
 Libraries: transformers, nltk, PyPDF2, sumy 

PDF Upload & Text Extraction 
 Clean and filter academic PDFs by removing irrelevant content (e.g., citations, URLs). 

BMC Dictionary Preparation 
 Text is mapped into predefined BMC segments. 

Sentence Tokenization & Classification 
 Sentences are classified into BMC categories using Zero-Shot inference with a dynamic confidence threshold. 

Summarization 
 Each BMC category is summarized using LSA to generate a structured and readable output. 

 

🎯 Threshold Tuning 

Confidence thresholds (default ≥ 0.3) are adjusted per document: 

Too low: Too much irrelevant info 

Too high: Missing relevant insights 
 Each case requires manual review for quality control. 

 

⚖️ Zero-Shot vs. Few-Shot 

Zero-Shot: Simpler, no training data needed, general-purpose outputs. 

Few-Shot: Better for context-specific insights but requires curated examples and more complex setup. 
 Due to limited sample size (37 papers), we chose Zero-Shot for efficiency. 

 

📊 Evaluation & Limitations 

Performs well for Customer Segments and Key Partners. 

Some ambiguity in Value Proposition and Key Activities due to the generalization limits of the Zero-Shot model. 

Domain-specific BMC insights (e.g., for energy prosumers) may require enhanced data or paid APIs for higher accuracy. 

 

🧭 Final Thoughts 

This tool serves as a starting point for automating BMC extraction in academic research. Iteration and refinement remain essential, as even powerful models require human oversight to ensure meaningful results. 

 
