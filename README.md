# AeroBrief AI: Plain-English Aviation Weather & Delay Assistant
Building AI course project

## Summary
AeroBrief AI translates complex aviation weather reports (METAR and TAF) into simple, plain-English briefings and predicts potential weather-related flight delays. It helps student pilots, dispatchers, and travelers make faster, safer decisions.

## Background
Aviation weather reports are packed with critical safety data, yet they are written in dense, coded abbreviations that can be slow and confusing to read under pressure.
* **Steep learning curve:** Student pilots and new flight dispatchers often spend extra time manually decoding wind, visibility, and cloud ceiling codes.
* **Unclear delay impacts:** Passengers and ground staff see raw weather alerts without knowing whether those conditions will actually cause a departure delay.
* **Motivation:** Combining aviation operations with artificial intelligence makes flight safety information clearer and more accessible to everyone.

## How is it used?
A user enters a 4-letter airport code (such as `VIDP` for Delhi or `KJFK` for New York) and their planned departure time into a simple web or mobile interface.
1. **Weather Translation:** The system fetches the latest airport weather report and displays a plain-English summary highlighting wind speed, visibility, and flight category (VFR/IFR).
2. **Delay Risk Score:** The AI evaluates current weather conditions alongside historical airport traffic to output a clear delay probability (for example, *Low Risk: 15% chance of delay*).
3. **Target Users:** Student pilots preparing pre-flight briefings, flight dispatchers monitoring multiple routes, and everyday travelers checking weather disruptions.

## Data sources and AI methods
This project relies on publicly available aviation and meteorological datasets:
* **Weather Data:** Live and historical METAR/TAF reports from the [Aviation Weather Center API](https://aviationweather.gov/data/metar/) and historical time-series observations from the [Iowa Environmental Mesonet](https://mesonet.agron.iastate.edu/request/download.phtml).
* **Flight Delay Data:** Historical airline on-time performance records from public repositories like the [Kaggle Flight Delay Dataset](https://www.kaggle.com/datasets/hrishitpatil/flight-data-2024).
* **AI Methods:** 
  * **Natural Language Processing (NLP):** Rule-based parsing paired with a lightweight language model to convert raw aviation codes into clear, readable sentences.
  * **Supervised Machine Learning:** Gradient Boosted Decision Trees and Logistic Regression trained on past weather and flight logs to predict delay probabilities.

## Challenges
* **Not a replacement for official briefings:** AI summaries can occasionally misinterpret rare weather remarks, so pilots must still verify official regulatory sources before flying.
* **Sudden weather shifts:** Rapidly developing thunderstorms or sudden fog cannot always be predicted accurately hours in advance.
* **Data bias:** Historical flight delay datasets are heavily concentrated in North America and Europe, meaning predictions for regional airports elsewhere may be less accurate until local data is added.

## What next?
* **Add voice briefings:** Integrate text-to-speech so users can listen to audio weather summaries hands-free.
* **Include NOTAMs:** Expand the NLP translator to summarize Notice to Air Missions (NOTAM) runway and airspace alerts.
* **Skills needed:** Collaborating with frontend developers to build a clean mobile interface and aviation subject-matter experts to validate safety phrasing.

## Acknowledgments
* Created as part of the **Building AI** course by Reaktor and the University of Helsinki.
* Inspired by open aviation weather tools from the NOAA Aviation Weather Center.
