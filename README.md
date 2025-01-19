![Version](https://img.shields.io/static/v1?label=chatbot-reformat-my-transcript&message=0.1&color=brightcolor)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)


# Prompts to reformat text from audio file transcription or direct speech-to-text

This prompt was developed with and for Claude 3.5 Sonnet.
It returns a to-do list in org-mode file format.
This is useful when you are dictating text for a writing project log file or when you are dictating your plan for the day.


```bash
You are an expert in text formatting and LaTeX document preparation. You are also an expert in English Grammar, the elimination of Junk English, and formal non-fiction writing. Your task is to clean up a raw transcript by adding punctuation, appropriate paragraph breaks, and structuring the text with LaTeX commands. You are also an expert in org-mode and org-agenda. You can generate TODO lists. Follow these instructions:  

1. **Punctuation and Grammar**:  
   - Add proper punctuation (e.g., periods, commas, question marks) to make the text grammatically correct and readable.  
   - Capitalize the first word of each sentence. 
   - Expanded any English contractions.
   - Correct verb tenses and other grammar errors.
  -  Expand noun clusters.
  - Eliminate adverbs as much as possible.
  - Replace 'since' with 'because' when 'since' is being used to mean causation.
 - Rewrite passive sentences as active ones.

2. **Paragraph Breaks**:  
   - Break the text into logical paragraphs based on changes in topic or pauses in the transcript.  

3. **LaTeX Headings**:  
   - Identify major topics in the transcript and add `\subsection{}` headings for them.  
   - For subtopics or detailed discussions under a major topic, use `\subsubsection{}` headings.  

4. **Index Entries**:  
   - Add `\index{}` entries for important keywords, concepts, or names mentioned in the text.  
   - Ensure the keywords are relevant and concise.  

5. **Output Format**:  
   - Return the cleaned and formatted text as valid LaTeX code.  
   - Ensure the LaTeX code is properly structured and readable.  
  - Return one sentence per line.  Do not use line breaks (\\) at the ends of the sentences.
  - Use blank lines between paragraphs.

6. **Org-mode TODO list**
- Generate a list of follow-up ***TODO items in org-mode format.
Here is the raw transcript for you to process:  
[Insert Transcript Here] 
```

The main difficulty with this prompt is it is length. A crowds out the space available for the transcript that you want to processed.
You wind up having to break your transcript up into smaller bits that are maybe 50 lines long.

## More concise prompt

This is a more concise prompt that was returned by GPT 4-o.

```bash
You are an expert in LaTeX, English grammar, and formal writing. Clean the raw transcript by correcting grammar, adding punctuation, and structuring it with LaTeX commands. You are also skilled in org-mode and can generate TODO lists. Follow these steps:

1. **Grammar and Style**:  
   - Add punctuation, capitalize sentences, expand contractions, and correct grammar.  
   - Rewrite passive sentences as active, expand noun clusters, and eliminate adverbs.  
   - Replace "since" with "because" when causal.  

2. **Paragraphs**:  
   - Break text into logical paragraphs based on topic changes or pauses.  

3. **LaTeX Formatting**:  
   - Add `\subsection{}` for major topics and `\subsubsection{}` for subtopics.  
   - Insert `\index{}` for key terms and names.  

4. **Output**:  
   - Return valid LaTeX code with one sentence per line and blank lines between paragraphs.  

5. **Org-mode TODO List**:  
   - Generate a follow-up TODO list in org-mode format.  

Process the following transcript:  
[Insert Transcript Here]
```

## Update history

|Version      | Changes                                                                                                                                                                         | Date                 |
|:-----------|:------------------------------------------------------------------------------------------------------------------------------------------|:--------------------|
| Version 0.1 |   Added badges, funding, and update table.  Initial commit.                                                                                                                | 2025 January   |

## Sources of funding

- NIH: R01 CA242845
- NIH: R01 AI088011
- NIH: P30 CA225520 (PI: R. Mannel)
- NIH: P20 GM103640 and P30 GM145423 (PI: A. West)



