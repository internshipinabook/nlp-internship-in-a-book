# CustomerCare-50K Dataset Suite
## The NLP Internship — InternshipInABook™ Book 2

This folder contains three datasets used across the 12-week internship.

---

## Files

### customercare_50k.csv — Weeks 0-4
50,000 customer support tickets from LinguaAI Labs (synthetic).
- **Languages:** English (65%), Nigerian Pidgin (20%), code-switched (10%), Yorùbá (3%), Hausa (2%)
- **Channels:** email, chat, social
- **Columns:** ticket_id, text, language, channel, timestamp, customer_region
- Used for: corpus characterisation, text cleaning, topic modelling

### tickets_labelled_5k.csv — Weeks 5-9
5,000 labelled tickets for supervised text classification.
- **Categories:** account (24%), billing (20%), technical (20%), delivery (14%), feedback (14%), abuse (8%)
- **Columns:** ticket_id, text, text_clean, category, language, channel, annotator_confidence
- Used for: TF-IDF + LR classifier, word vectors, BERT fine-tuning, AfroXLMR evaluation

### sentimentng_2k.csv — Weeks 10-12
2,000 Nigerian social media posts for multilingual sentiment analysis.
- **Sentiment:** negative (45%), positive (30%), neutral (25%)
- **Cities:** Lagos, Abuja, Kano, Port Harcourt, Ibadan
- **Columns:** post_id, text, language, sentiment, city, platform, date
- Used for: fairness audit, dialect bias analysis, Week 12 capstone

---

## Language Notes

**Nigerian Pidgin (pcm)** is a creole language spoken by ~75 million people.
It is not broken English. Key markers:
- "abeg" = please
- "don" = have/has (completed action)
- "una" = you (plural)
- "dey" = is/are (continuous)
- "wahala" = trouble/problem
- "oga" = boss/sir

A model trained only on English will have a 26-31% OOV rate on Pidgin tickets.
This is the central engineering problem of the book, resolved in Week 9 with AfroXLMR.

---

## Licence
CC0 (synthetic data, no personal information).
Generated with seed=42 for reproducibility.
