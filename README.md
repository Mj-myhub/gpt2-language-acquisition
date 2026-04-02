# gpt2-language-acquisition
Fine-tuned GPT-2 (117M-774M) on CHILDES child-directed speech to model language acquisition
GPT-2 for Modelling Language Acquisition

Master's Thesis - University of Siena
Author: Majid Jafari
Supervisors: Prof. C. Chesi, Prof. A. Belletti (collab. Prof. L. Rizzi)

Overview
This project investigates whether GPT-2 can simulate cognitive processes in child language acquisition. We fine-tuned GPT-2 at three parameter scales (117M, 345M, 774M) on child-directed speech from CHILDES, then evaluated:

Wh-question answering (subject, object, who-questions)
Auxless question processing (ill-formed child utterances)
Morphological generalisation to nonsense words (Berko's wug test)

Key Results
Experiment                     117M      345M      774M 

Wh-Question Accuracy           ~22%      ~55%      72-78%  

Subject Question Error          40%       25%       15%  

Morphological Generalisation  Partial   Partial    Strong

3.5x improvement on subject questions across scales
150+ experiments across all model sizes
Clear scaling-law patterns

Data Sources
Uses data from CHILDES (Child Language Data Exchange System).
Experiment                      Corpus                  Child                      Age 
Wh-Questions            Bliss (norwilli.cha)            Willie                     6;1
Auxless Questions       Wells (Tony/030608.cha)         Tony                       3;6
Training                Warren-Leubecker           (david.cha)David                5;10
Access: https://childes.talkbank.org/ (freely available for research)
Structure
notebooks/     # Google Colab experiment notebooks
data/          # Data sources and CHILDES info
thesis/        # Full thesis PDF
Theoretical Framework

Relativized Minimality (Rizzi, 1990)
Growing Trees (Friedmann et al., 2020)
Wug Test (Berko, 1958)

Citation
Jafari, M. (2021). How Children Accurately Predict the Integration of
Incoming Words into Phrase Structure. MSc thesis, University of Siena.
