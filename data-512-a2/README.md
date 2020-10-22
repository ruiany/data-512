# DATA512 - A2: Bias in data

## Goal of the project
The [Wikipeida Detox project](https://meta.wikimedia.org/wiki/Research:Detox) aims to provide a better dicussion environment and has collected large hhuman-annotated 
datasets to train models to identify hostile language use on Wikipedia Talk page discussions. Google data scientists used these annotated datasets to train machine learning models as part of a project called [Conversation AI](https://github.com/conversationai/perspectiveapi). The models have been used in a variety of software products and made freely accessible to anyone through the Perspective API. 
<br>
<br>
For this assignment, the annotated Wikipeida Talk comments for aggression and toxicity are used to identify potential bias in human-labled and analyze implications of models trained using the labled data.

## Source data
The labeled datasets can be downloaded from [Figshare](https://figshare.com/projects/Wikipedia_Talk/16731).
<br>
The raw data used for the analysis can be found as csv files in [raw data](https://github.com/ruiany/data-512/tree/main/data-512-a2/raw_data).

## Output data
The output data used for making visualization can be found as csv files in [output data](https://github.com/ruiany/data-512/tree/main/data-512-a2/output_data).
### aggression_worker_annotations.csv
| Column | Description |
|--------|-------------|
| `worker_id`   | Anonymized crowd-worker id |
| `gender`  | The gender of the crowd-worker. Takes a value in {'male', 'female', and 'other'} |
| `english_first_language`   | Does the crowd-worker describe English as their first language. Takes a value in {0, 1} |
| `age_group`  | The age group of the crowd-worker. Takes on values in {'Under 18', '18-30', '30-45', '45-60', 'Over 60'} |
| `education`   | The highest education level obtained by the crowd-worker. Takes on values in {'none', 'some', 'hs', 'bachelors', 'masters', 'doctorate', 'professional'}. Here 'none' means no schooling, some means 'some schooling', 'hs' means high school completion, and the remaining terms indicate completion of the corresponding degree type |
| `ratio`  | The ratio of aggressive comments over total comments labeled by the annotator |

### toxicity_worker_annotations.csv
| Column | Description |
|--------|-------------|
| `worker_id`   | Anonymized crowd-worker id |
| `gender`  | The gender of the crowd-worker. Takes a value in {'male', 'female', and 'other'} |
| `english_first_language`   | Does the crowd-worker describe English as their first language. Takes a value in {0, 1} |
| `age_group`  | The age group of the crowd-worker. Takes on values in {'Under 18', '18-30', '30-45', '45-60', 'Over 60'} |
| `education`   | The highest education level obtained by the crowd-worker. Takes on values in {'none', 'some', 'hs', 'bachelors', 'masters', 'doctorate', 'professional'}. Here 'none' means no schooling, some means 'some schooling', 'hs' means high school completion, and the remaining terms indicate completion of the corresponding degree type |
| `ratio`  | The ratio of toxic comments over total comments labeled by the annotator |

### agreement_ratio.csv
| Column | Description |
|--------|-------------|
| `aggression`   | The ratio of agreement among all annotators for a comment for aggression |
| `toxicity`  | The ratio of agreement among all annotators for a comment for toxicity |


## License
[MIT](https://choosealicense.com/licenses/mit/)

