# Spam & Toxic Text Detection

### Using Machine Learning to detect irrelevant and inappropriate text, entirely in the browser.

---

Try it out live in the browser 👉🏻 [(link)](https://eloquent-chimera-125a10.netlify.app/)(https://aquamarine-zuccutto-8d6170.netlify.app/)

---

#### What is toxic text? 🤬

Anything disrespectful, abusive, unpleasant, harmful, and/or simply irrelevant (SPAM). Detecting toxic text directly in the browser allows you to filter it out at the origin, even before it reaches your servers.

#### How does it work?

Once a sentence is submitted, the text is tokenized and passed to the model. The model then returns a toxicity level, ranging from 0 to 100. If it's greater than a given threshold, the text is considered toxic. In the example you'll find in this repository, the threshold is **75**. Anything equal or above is considered inappropriate and will be visually marked as toxic. In your code, you can change this value to your liking and to best fit your needs.

#### About the model

The model is trained using the (https://www.tensorflow.org/lite/models/modify/model_maker/text_classification), trained on a custom dataset of almost 2 thousands classified comments from Youtube and other sources. I trained the original Python model using Google Colab, then converted it in the TensorFlowJS format to be used in the browser. The entire model is just **199KB**, which makes it very lightweight.

#### Future improvements 🚀

Currently the model only supports **English**. It would be great to add support for other languages in the future. The only challenge is to find good datasets to train the model on. Also, at present, for maximum accuracy the model can validate no more than **20 words** at a time. This is not much of a limitation though, as you can simply split a long text into smaller chunks and validate each one. Although great care has been put into compiling a comprehensive training dataset, inevitably there might be some false positives and negatives. If you find any, please do let me know, or even better, submit a pull request on the CSV file `trainingdataset/toxictext_trainingdata.csv`.



