# “He” and “She”： The improvement of gender equality from the perspective of spoken languages

## Data Story

Here is the link to the webpage of our data story : 

## Abstract

Following Emma Watson's speech at the United Nations, the public is paying increasing attention towards gender equality, and some of the words used in the past have changed. For instance, people may tend to use “firefighter” and “chairperson” instead of some gender-propelled languages such as “fireman” and “chairman”. The change in the frequency of using these “more equal” words can be an interesting way to indicate the attitude of nowadays social media.

Since the phenomenon is quite common in many aspects of lives, we classify the dataset by the topic and news media. After identifying and counting the masculine, neuter and feminine words, we want to compare the frequency of them in different fields, such as different balls in sports, different parties in politics and regional news. We also analyze the frequency changes of specific words between 2015 and 2020, the results will show whether the efforts of Emma et al. have paid off.

## Research questions

- Do people of different genders have the same opportunities to have a voice in public media?
- How much attention does “He” or “She” receive in public media?
- What is the frequency of using gender-neutral words like “firefighter” and “chairperson” compared to gender-propelled words usage like “fireman” and “chairman”?
- How do the answers of the above three questions evolve along with time?
- Are there any different trends on these gender equality questions in different aspects of topics(e.g. Politics, Health, Art, etc.)?
- An interesting follow-up question can be: are there any differences between the Democratic Party members and Republican Party members regarding the use of masculine language( based on this related research: [Linking Gender, Language, and Partisanship: Developing a Database of Masculine and Feminine Words](https://journals.sagepub.com/doi/10.1177/1065912919874883)
- What kind of social attention the topic of gender equality receives and what are people's attitudes towards gender equality？

## Proposed additional datasets

- To reveal the frequency of using gender-neutral words, a dataset of gender-propelled words (with roughly 100 feminine - masculine word pairs, e.g. actress-actor) from a relative research and a smaller dataset of gender-neutral words (e.g. policewoman-policeman-police officer) are employed.
- To investigate the attention given to the issue of gender equality, a dataset of gender equality related words and phrases is used to obtain the relevant quotations.
- WIKI dump data of attribute: Including the Nationality, gender, party and occupation of all attributes proposed by the dataset.

## Methods

**Data pre-processing:**

- Text data cleaning: Remove punctuations, normalize the case etc.
- Topic categorization: Exploit existing categories of quotations implied by its url and text content.
- Collection of character information: Extract people’s information from Wiki dump and build tables.
- Word bank acquisition: Use existing wordbank online.
- Gender-related qutations extraction: Use keywords matching to extract quotations.
**Data analysis:**

- Do statistics by matching the masculine words and feminine words in the text of fixed subset of data of specific newspaper, year and topic to obtain information on gender concerns.

- Use word embedding to determine whether some words that should be neuter words (such as " politician, housekeeper, strong, weak", etc.) are no longer neuter because they are more frequently to be used to describe or refer to people of one gender instead of another.

- Use sentiment analysis on the quotations relevant to the issue of gender equality to infer people's attitude towards this issue.

**Results visualization and interpretation:**

- Visualize the results achieved in the previous steps and compare the results between different years, different topics, different parties to capture different or trending trends on the timeline.

- Refer to relative researches and literatures to try to interpret if there’s causality existing in observed trends or differences.

## Proposed timeline

| **Week** |    **Date**     |                                     **Task**                                      |
| :------- | :-------------: | :-------------------------------------------------------------------------------: |
| Week 9   | 15 Nov - 21 Nov |  Building dataset
| Week 10  | 22 Nov - 28 Nov |          Statistical analysis          |
| Week 11  | 29 Nov - 05 Dec |              Investigating the bias of neuter words              |
| Week 12  | 06 Dec - 12 Dec |               Sentimental analysis               |
| Week 13  | 13 Dec - 17 Dec |              Writing the data story and preparing for the presentation               |

## Contributions within the team

- Yueqing Shen: Collect masculine words and feminine words and build a thesaurus, perform corresponding text matching, and analyze the frequency and proportion of words, etc., and perform corresponding data visualization work.

- Junzhe Tang: Writing data stories and analyze the lexicality of words through word embedding models.

- Zhipeng Mao: Processing the raw quotebank data, extract the needed data, and classify the topics and create a search engine for the dataset to facilitate subsequent data retrieval.

- Yuxing Yao: Extract and analyze attributer's features through wiki dump and build sentiment analysis models to analyze people's attitudes towards gender-related topics.

## Questions for TAs

- Some attributers in quotebank data correspond to more than one qid, which causes difficulties in feature extraction and processing of the attributer. Is there any way to solve the corresponding problem? (e.g. introduce more restrictions, such as nationality, party affiliation, birthday, etc.)
- To ensure no bias in statistical analysis, we employ approximately 100 pairs of feminine words and masculine words (for example, actress - actor). If the dataset is big enough for us to reach convincing results and if using these word pairs is an effective implementation to reduce bias?
