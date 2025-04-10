# topic_model_workshop

These scripts are intended as basic introductions to two topic modeling methods: structural topic models (STM; Roberts et al., 2014) and BERTopic (Grootendorst, 2022).

**STM** is a "semiautomated approach" of analyzing text data that "discover[s] topics" within documents (e.g., open-ended responses, narratives). The result is "a model where each open-ended response is a mixture of topics" that also "allow[s] for the inclusion of covariates of interest into the prior distributions for document-topic proportions and topic-word distributions" (e.g., "the author’s gender, political affiliation, and treatment assignment"). (pp. 1064-1067)

> Roberts, M. E., Stewart, B. M., Tingley, D., Lucas, C., Leder-Luis, J., Gadarian, S. K., Albertson, B., & Rand, D. G. (2014). Structural topic models for open-ended survey responses. *American Journal of Political Science*, *58*(4), 1064–1082.[https://doi.org/10.1111/ajps.12103](https://doi.org/10.1111/ajps.12103)

**BERTopic** is another method that "extract[s] coherent topic representation" by "approach[ing] topic modeling as a clustering task". Specifically, it "generates document embedding[s] with pre-trained transformer-based language models, clusters these embeddings, and finally, generates topic representations with the class-based TF-IDF procedure." (p. 1)

> Grootendorst, M. (2022). BERTopic: Neural topic modeling with a class-based TF-IDF procedure. arXiv preprint arXiv:2203.05794. [https://doi.org/10.48550/arXiv.2203.05794](https://doi.org/10.48550/arXiv.2203.05794)

For instructional purposes, the scripts work off of the Dreaddit dataset (Turcan & McKeown, 2019).

> Turcan, E., & McKeown, K. (2019). Dreaddit: A reddit dataset for stress analysis in social media. arXiv preprint arXiv:1911.00133. [https://doi.org/10.48550/arXiv.1911.00133](https://doi.org/10.48550/arXiv.1911.00133)

## **Usage**

Scripts for a given method (STM, BERTopic) are housed within their respective folders (`/stm/`, `/bertopic/`)

### STM

For STM, launch `stm.RProj` and then the script (`stm.qmd`, a Quarto file). The script is configured to point to the example Dreaddit dataset in the `/input/` folder, but adjust as necessary if using your own data. Note that you can browse `dreaddit-train.csv` in the `/input/` folder for an example of how the input data file can/should be set up. If using different formatting or variable names, please adjust the script (`stm.qmd`) to match.

### BERTopic

<a target="_blank" href="https://colab.research.google.com/github/ryancyeung/topic_model_workshop/blob/main/bertopic/bertopic.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

For BERTopic, the script (`bertopic.ipynb`) is currently configured to be run in Google Colab (see [hopefully functional] button above). In order to run the script in Google Colab, you'll need to also upload the example Dreaddit data file (`dreaddit-train.csv` in the `/input/` folder) or whichever other data file you'd like to work with onto your Google Drive. The script will have instructions as to how to then point to that uploaded data file in your Google Drive. Again, adjust as necessary to make sure it's pointing to the correct variables and file locations.

## **Authors and Acknowledgment**

Authors:
* [Ryan Yeung](https://ryancyeung.github.io)

Adapted from [Make a README](https://www.makeareadme.com/) template and [Best-README-Template](https://github.com/othneildrew/Best-README-Template).