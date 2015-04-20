# Tweet-Sentiment-Analysis

This project has 5 phases:
1. Tweets are fetched from the twitter api using twitter4j.
2. These tweets are saved into a database while simiultaneously pushing them into SQS.
3. Tweets are fetched from the SQS by multiple worker threads who analyze the sentiment of the queue while sending them to SNS and saving them back to the DB.
4. The tweet sentiments are mapped onto a MAP using Google Map API.
5. The tweets are updated real time using web sockets.
