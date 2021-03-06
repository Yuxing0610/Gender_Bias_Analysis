# “He” and “She”：Explorative Data Analysis on Gender Equality Based on Quotebank Dataset

## Data Story

Here is the link to the webpage of our data story : 

http://www.adaysmj.com/

## Abstract

In recent years, various efforts have been made around the world for the protection of women's rights. Many people believe that we are now in a society of relative gender equality, but does this optimism hold? Unfortunately, we still have a long way to go on the road to gender equality. The gender equality we have established is incomplete and fragile, which was revealed by the Covid-19 epidemic. According to UN Women, women have a much higher rate of unemployment due to the epidemic than men, 11 million girls may lose access to education forever, and 47 million women are expected to end the year in extreme poverty because of the economic consequences of the epidemic, reversing decades of progress...

We believe that we need to quantify the persistent sexism in our society through data, and one good approach is through conducting analysis on the voices of people from all walks of life in the media. Quotebank [1] made it possible to achieve this goal. In this project, we conducted various analyses on the dataset to explore people's gender stereotypes and discriminations and accordingly revealed women’s social status, which brought to light the severity of gender inequality and urgency of making a change with solid evidence.

## Research questions

#### Part 1 Exploratory statistical analysis: does gender inequality exist?

- How do masculine/feminine words’ count and ratio change as time goes overall and in different categories?
- Who contributes to the use of masculine/feminine words w.r.t the speakers' gender?
- What are the most frequently used feminine/masculine words and can these results reflect the gender inequality in the society?
- Does a difference between languages used by Republicans and Democrats really exist w.r.t the masculine/feminine words usage?

#### Part 2 Gender bias indeed exists: from the view of word embeddings

- Do word embeddings trained on the Quotebank dataset contain gender biases concerning occupations and personality?
- What word analogies like 'he'-'she' generated by the embeddings can exhibit gender biases?

#### Part 3 What are people's attitudes toward gender equality?

- How much attention are people paying to gender equality?
- What are people's attitudes toward gender equality, positive or negative?

## Proposed additional datasets

- To reveal the frequency of using gender-neutral words, a dataset of gender-propelled words (with roughly 100 feminine - masculine word pairs, e.g. actress-actor) from a relative research and a smaller dataset of gender-neutral words (e.g. policewoman-policeman-police officer) are employed.(https://github.com/uclanlp/gn_glove/tree/master/wordlist)
- To explore the difference between the language used by Democratic Party and Republican Party, a score sheet including 700 words with scores ranging from 1 (most feminine) to 7 (most masculine) was introduced.(https://journals.sagepub.com/doi/suppl/10.1177/1065912919874883)

- To investigate the attention given to the issue of gender equality, a dataset of gender equality related words and phrases is used to obtain the relevant quotations.
- WIKI dump data of attribute: Including the Nationality, gender, party and occupation of all attributes proposed by the dataset.

- Profession wordlist with their score evaluating whether it's definitional or stereotype male/female word (https://github.com/tolga-b/debiaswe/blob/master/data/professions.json).
- Personality adjectives obtained from the internet (https://www.enchantedlearning.com/wordlist/adjectivesforpeople.shtml).

## Methods

#### Data pre-processing

- Text data cleaning: Remove punctuations, normalize the case etc.
- Topic categorization: Exploit existing categories of quotations implied by its url and text content.
- Collection of character information: Extract people’s information from Wiki dump and build tables.
- Word bank acquisition: Use existing wordbank online.
- Gender-related qutations extraction: Use keywords matching to extract quotations.

#### Data analysis

- Do statistics by matching the masculine words and feminine words in the text of fixed subset of data of specific newspaper, year and topic to obtain information on gender concerns.
- Use word2vec to train word embeddings and analyze whether the embeddings contain gender stereotypes
- Use sentiment analysis on the quotations relevant to the issue of gender equality to infer people's attitude towards this issue.

#### Results visualization and interpretation

- Visualize the results achieved in the previous steps and compare the results between different years, different topics, different parties to capture different or trending trends on the timeline.

- Refer to relative researches and literatures to try to interpret if there’s causality existing in observed trends or differences.

## Proposed timeline

| **Week** |    **Date**     |                      **Task**                       |
| :------- | :-------------: | :-------------------------------------------------: |
| Week 9   | 15 Nov - 21 Nov | Doing problem definition and data preparation works |
| Week 10  | 22 Nov - 28 Nov |              Performing data analysis               |
| Week 11  | 29 Nov - 05 Dec |              Performing data analysis               |
| Week 12  | 06 Dec - 12 Dec |               Writing the data story                |
| Week 13  | 13 Dec - 17 Dec |              Constructing the website               |

## Contributions within the team

- Yueqing Shen: Collect masculine words and feminine words and build a thesaurus, perform corresponding text matching, and analyze the frequency and proportion of words, etc., and perform corresponding data visualization work.

- Junzhe Tang: Construct the data story website.

- Zhipeng Mao: Preprocess and classify the raw Quotebank data; Train word embeddings on the dataset and perform analysis.

- Yuxing Yao: Extract and analyze attributer's features through wiki dump and build sentiment analysis models to analyze people's attitudes towards gender-related topics.

## Questions for TAs

- Some attributers in quotebank data correspond to more than one qid, which causes difficulties in feature extraction and processing of the attributer. Is there any way to solve the corresponding problem? (e.g. introduce more restrictions, such as nationality, party affiliation, birthday, etc.)
- To ensure no bias in statistical analysis, we employ approximately 100 pairs of feminine words and masculine words (for example, actress - actor). If the dataset is big enough for us to reach convincing results and if using these word pairs is an effective implementation to reduce bias?
