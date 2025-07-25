# CL-LLM-ABSC
Implementation of curriculum learning for Aspect-Based Sentiment Analysis (ABSA) using large language models (LLMs), as performed in the research 'Enhancing Aspect-Based Sentiment Analysis with Large Language Models through Curriculum Learning'. Underneath, the code files to perform the research are explained. The notebooks should be run in Google Colab.

### KATE
Use KATE.ipynb to retrieve the k most similar training instances, for every test instance, by performing KATE.
Input: 2015_Restaurants_Train.xml, 2015_Restaurants_Test.xml, 2016_Restaurants_Train.xml, and 2016_Restaurants_Test.xml
Output: top_k_indices_2015.csv, top_k_indices_2016.csv

### SL and SWN complexity scores
Use SL+SWN.ipynb to compute the SL and SWN complexity scores.
Input: Input: 2015_Restaurants_Train.xml, 2015_Restaurants_Test.xml, 2016_Restaurants_Train.xml, and 2016_Restaurants_Test.xml
Output: sentence_lengths_2015.csv, sentence_lengths_2016.csv, swn_complexity_scores_2015.csv, and swn_complexity_scores_2016.csv

### CE complexity scores
Use CE.ipynb to compute the CE complexity scores for every all three LLMs.
Input: 2015_Restaurants_Train.xml and 2016_Restaurants_Train.xml
Output: ce_mistral_2015.csv, ce_mistral_2016.csv, ce_llama_2015.csv, ce_llama_2016.csv, ce_gemma_2015.csv, and ce_gemma_2016.csv

### ICCL
Use ICCL.ipynb to compute the zero-shot and few-shot classification results for all three off-the-shelf LLMs.
Input: 201x_Restaurants_Train.xml, 201x_Restaurants_Test.xml, top_k_indices_201x.csv, sentence_lengths_201x.csv, swn_complexity_scores_201x.csv, and ce_model_201x.csv, with model being either mistral, llama or gemma and 201x being either 2015 or 2016.
Output: Zero-shot and few-shot classification results for the corresponding dataset and model.

### FTCL
Use FTCL_Mistral.ipynb to compute the classification results for the fine-tuned Mistral models.
Input: 201x_Restaurants_Train.xml, 201x_Restaurants_Test.xml, sentence_lengths_201x.csv, swn_complexity_scores_201x.csv, and ce_mistral_201x.csv, with 201x being either 2015 or 2016.
Output: FTCL results for Mistral on the corresponding dataset.

Use FTCL_Llama.ipynb to compute the classification results for the fine-tuned Llama models.
Input: 201x_Restaurants_Train.xml, 201x_Restaurants_Test.xml, sentence_lengths_201x.csv, swn_complexity_scores_201x.csv, and ce_llama_201x.csv, with 201x being either 2015 or 2016.
Output: FTCL results for Llama on the corresponding dataset.

Use FTCL_Gemma.ipynb to compute the classification results for the fine-tuned Gemma models.
Input: 201x_Restaurants_Train.xml, 201x_Restaurants_Test.xml, sentence_lengths_201x.csv, swn_complexity_scores_201x.csv, and ce_gemma_201x.csv, with 201x being either 2015 or 2016.
Output: FTCL results for Gemma on the corresponding dataset.
