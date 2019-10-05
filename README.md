# smart-banking-app
![](https://media.giphy.com/media/26zzjqiSqWzBdqU00/giphy.gif)

[View app deployment](https://smart-banking-app-api.herokuapp.com/)

Smart Banking Chat Bot- This is an AI based project which uses several ML algorithms for Natural Language Understanding which identifies intent and entities from user-issues and generates dialogue.

This project may assist Financial Institutions to add chatbot in their web-application, so customers can ask questions to the chatbot without having to visit his/her Bank.

>Requirements
  - Python (v3.6.3) and Libraries required for AI and Natural Language Processing(NLP)
  - Rasa Core (v0.11.12)
  - Rasa NLU (v0.13.7)
  - Bootstrap (v3.3.7)
  - AngularJS (v1.6.4)
  - jQuery (v1.10.2)
  - SQL Server 2014
  - PHP (v5.6.32)
 
To install database with data, we have added a SQL file in the repostory.

>To train model,
  1. go to train directory
    - cd train
  2. run command to train nlu which actually understands natural langauge examples given in training_data.json which have classfied
    - python Bank-bot.py train-nlu
  3. run command to train core which predicts actions using training data given in stories.md file
    - python Bank-bot.py train-nlu
  4. to train model online, run (using this we can have more data of predicting action which makes model more accurate :) )
    - $ python -m rasa_core_sdk.endpoint --actions actions & python -m rasa_core.train --online -o models/dialogue -u models/nlu/default/bank_nlu  -d bank_domain.yml -s data/stories.md --endpoints endpoints.yml --batch_size 500 --epochs 200 --history 15 --validation_split 0.2 --nlu_threshold 0.2 --core_threshold 0.2 --fallback_action_name action_fallback
  5. And to finally run bot, use
    - $ python -m rasa_core.run --enable_api  -d models/dialogue -u models/nlu/default/bank_nlu --endpoints endpoints.yml 
    - $ python -m rasa_core_sdk.endpoint --actions actions
    - which have to run both in different terminals
  
  
# Ai Stats News: 86% Of Consumers Prefer Humans To Chatbots, Wow!
## RIHAD VARIAWA
  
A recent surveys, studies, forecasts and other quantitative assessments of the progress of Ai, highlighted the growing reluctance of U.S consumers to chat with chatbots, the growing expectations of Ai as a critical business component, and the growing employee skills gap due to the deployment of new technologies.

## Ai business impact
According to a [survey of 1,000 U.S consumers by CGS,](https://www.cray.com/resources/enterprise-ai-adoption-survey) 86% of consumers prefer to interact with a human agent; 71% said they would be less likely to use a brand if it didn’t have human customer service representatives available; only 30% believe that chatbots and virtual assistants make it easier to address customer service issues; only 29% of consumers looking for a quick answer would choose chat over all other channels, down from 50% in 2018, and 40% chose the phone or voice option first.

Over 34% of IT professionals believe Ai is already *critical to business* capability in their organization, or that it will be at some time during 2019; nearly half said Ai had a positive effect on their daily working experience in the past year [Cray survey of more than 300 IT professionals](https://www.cgsinc.com/en/resources/2019-CGS-Customer-Service-Chatbots-Channels-Survey)

## Ai's expected business impact
41% of IT professionals expect Ai to become critical to their business within the next three years; nearly 70% believe Ai could improve operational efficiency; more than half said Ai could help improve the customer experience, create competitive advantage and make data more actionable; over 44% believe Ai could help with controlling costs and growing revenue; more than 65% believe Ai will have a positive effect on their daily working experience in the next year; only 5.6%  believe they won’t benefit from Ai [Cray survey of more than 300 IT professionals](https://www.cgsinc.com/en/resources/2019-CGS-Customer-Service-Chatbots-Channels-Survey)

## Business adoption of Ai
The Sgt. Star chatbot, which has answered more than 16 million questions since its debut in 2004 on the Army’s website, has an accuracy rate that exceeds 95% [The Wall Street Journal](https://www.wsj.com/articles/army-to-deploy-female-chatbot-to-help-recruit-women-11569576606) Over 70% of companies already have Ai applications in use or under development; nearly 60% of IT professionals identified cost-effectiveness as a top consideration when selecting an infrastructure solution for Ai, 51% cited the ability to integrate Ai systems into existing architecture, 49% mentioned ease of use and 40% scaling with increasing uses and demands [Cray survey of more than 300 IT professionals](https://www.cgsinc.com/en/resources/2019-CGS-Customer-Service-Chatbots-Channels-Survey)

84% of businesses say implementing Ai “at scale” in their organizations is necessary for them to be successful over the next three years; 70% say these efforts are designed to strengthen competitive positions for the long-term. [PwC survey of 775 US business leaders](https://www.pwc.com/us/en/library/fit-for-growth/automation-survey.html) While in January 2019, 62% of IT leaders were considering or actively adding virtual support agents, 6 months later HR leaders still struggle to leverage Ai to improve the employee experience—26% would need IT approval even if HR had funding, and another 24% said that funding would have to come from IT [Expressive and AWS survey of senior HR leaders](https://www.espressive.com/press/new-survey-reveals-that-hr-leaders-are-prioritizing-artificial-intelligence-to-improve-the-employee-experience/)

## The future of work
56% of organizations believe they have a moderate to severe skills gap today; 60% percent of employees believe that, to some extent, their current skill set will become outdated in the next three to five years; 43% percent believe managers don’t know how to upskills and reskill employees, and another 39% feel they don’t have the time to do so; of employees who will need reskilling by 2022, 35% will need training that could take up to 6 months, while 10% will require training that could take more than a year; in the past year, 70% of organizations have introduced at least one new technology designed to increase employee capacity but 33% of employees say they were never trained on this new technology they were tasked with using [West Monroe Partners survey of 432 HR professionals (manager level and above) and 1,000 U.S. workers](https://www.westmonroepartners.com/News/Press-Releases/2019/09/The-Upskilling-Crisis)

45% of managers don’t feel confident in their ability to develop the skills employees need today; managers spend on average 9% of their time on developing their direct reports; 70% of employees have not mastered the skills they need for their jobs today, let alone the skills needed for their future roles [Gartner](https://www.gartner.com/en/newsroom/press-releases/2019-09-18-gartner-says-45--of-managers-lack-confidence-to-help-)

## The digital competitiveness of nations
The U.S held on to the number one spot in IMD World Digital Competitiveness ranking (WDCR) in 2019, with all top five economies in the index unchanged: USA, Singapore, Sweden, Denmark and Switzerland. In the Top 10, the Netherlands, Hong Kong SAR and Republic of Korea moved up (to 6th, 8th and 10th, respectively), while Norway dropped to 9th and Canada fell from 8th to 11th. Taiwan and China moved up to 13th and 22nd respectively [IMD](https://www.imd.org/wcc/world-competitiveness-center/)

## The Life of Data, the fuel for Ai
52% of IT professionals know someone who still has access to a former employer’s applications and data [Ivanti online survey of more than 400 IT professionals](https://www.ivanti.com/blog/ivanti-identity-survey-results)

## Ai market forecasts
The worldwide market for enterprise applications of Ai is estimated to reach $107.3 billion in 2025, up from $7.6 billion in 2018 [Tractica](https://www.tractica.com/research/artificial-intelligence-for-enterprise-applications/)

By 2020, Gartner predicts that 30% of all B2B companies will employ some kind of Ai to augment at least one of their primary sales processes [Gartner](https://www.gartner.com/en/newsroom/press-releases/2019-09-19-gartner-says-ai-to-have-significant-impact-on-sales-t)

## The robotics market worldwide is estimated to reach $248.5 billion by 2025, up from $48.9 billion in 2018 [Tractica]
The Ai systems market in the Middle East and Africa is expected to reach $374.2 million in 2020, up from $261.8 million in 2018 and an anticipated $310.3 million in 2019 [IDC}(https://www.idc.com/getdoc.jsp?containerId=prMETA45546719)

Telecommunications service providers will spend $11.2 billion annually on AI-driven software solutions across eight use cases by 2025, up from $419.0 million in 2018 [Tractica](https://www.tractica.com/research/artificial-intelligence-for-telecommunications-applications/)

The worldwide market for smart home devices is expected to grow 23.5% year over year in 2019 to nearly 815 million device shipments and more than 1.39 billion in 2023 [IDC.](https://www.idc.com/getdoc.jsp?containerId=prUS45540319) In 2018, China’s video surveillance equipment market (excluding home video surveillance) reached $10.6 billion and is expected to reach $20.1 billion in 2023; driven by Ai technology, especially Edge Ai, the application of video surveillance has gradually expanded to more fields, such as passenger flow analysis, environmental pollution monitoring and insurance loss determination [IDC](https://www.idc.com/getdoc.jsp?containerId=prCHE45536619)

## Ai quotable quotes
“There is little doubt that Ai will contribute to profound transformations over the next decades. At its best, the technology has the potential to release us from mundane work and create a utopia in which all time is leisure time. At its worst, World War III might be fought by armies of superintelligent robots. But they won’t be led by HAL, Skynet or their newer Ai relatives. Even in the worst case, the robots will remain under our command, and we will have only ourselves to blame”—Anthony Zador and Yann LeCun

“The sensor hardware we are using is still a work in progress, especially in terms of achieving mass production and automotive-grade quality”—Alan Hall, Ford’s Argo Ai self-driving car subsidiary

“One of the key pain points is turning data into a human-friendly narrative, suitable for normal people”—Colin Priest, vice president of Ai strategy, DataRobot

## Data is eating the world quote of the week

“Data is the crude oil of the modern economy. And we are now in an environment where. We don’t know who should own these new oil fields. We don’t always know who should have the rights or the title to these gushers of cash. And we don’t know who decides how to use that data. Can these algorithms be trusted with our lives and hopes? … Digital authoritarianism is not, alas, the stuff of dystopian fantasy but of an emerging reality”—Boris Johnson, Prime Minister, UK
