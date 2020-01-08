# Project Overview

## Project Name

Entertainment IQ

## Project Description

A one-player trivia game that allows users to test their entertainment knowledge in three categories: film, television and music. The app will fetch a random 12 questions and score based on number of correct answers. The game is over when a user has answered all 12 questions and will present an assessment of the user’s knowledge (e.g. Expert, Intermediate and Novice). 

## API and Data Sample

[Open Trivia DB](https://opentdb.com/api_config.php)

### API Data Sample

```JSON
{
    "response_code": 0,
    "results": [
        {
            "category": "Entertainment: Television",
            "type": "multiple",
            "difficulty": "easy",
            "question": "In the TV show &quot;Cheers&quot;, Sam Malone was a former relief pitcher for which baseball team?",
            "correct_answer": "Boston Red Sox",
            "incorrect_answers": [
                "New York Mets",
                "Baltimore Orioles",
                "Milwaukee Brewers"
            ]
        },
        {
            "category": "Entertainment: Television",
            "type": "multiple",
            "difficulty": "easy",
            "question": "In the TV show &#039;M*A*S*H&#039;, what was the nickname of Corporal Walter O&#039;Reilly?",
            "correct_answer": "Radar",
            "incorrect_answers": [
                "Hawkeye",
                "Hot Lips",
                "Trapper"
            ]
        }

```

## Wireframes

https://wireframe.cc/pro/pp/84310c826302744 

### MVP/PostMVP - 5min 

#### MVP 

- Allow user to choose a category (3 options)
- Display question and answer choices
- Track score - every correct answer is 1 point, every wrong answer earns 0 points
- Display correct answer if the user answered wrong
- Reset game option to start over


#### PostMVP 

- Implement session token to not repeat questions if restarted
- Local Storage to store questions and user answers
- More categories to choose from (e.g. Books, Video Games, Sports, etc.)
- Multi-player functionality - compete with another person
- Choose a new category for each question turn 


## Project Schedule

This schedule will be used to keep track of your progress throughout the week and align with our expectations.  

You are **responsible** for scheduling time with your squad to seek approval for each deliverable by the end of the corresponding day, excluding `Saturday` and `Sunday`.

|  Day | Deliverable | Status
|---|---| ---|
|Thursday, 1/2| Project plan; Project approval | Completed
|Friday, 1/3| Pseudocode functionality; Core App Structure (HTML & CSS) | Completed
|Monday, 1/6| Code fetching questions from API and record user answers | Completed
|Tuesday, 1/7| Code functionality to track score; Code functionality to display final result | Completed
|Wednesday, 1/8| Reset Game Button to restart; Finalize CSS with media queries; Completed MVP  | Completed
|Thursday, 1/9| Present | Incomplete


## Priority Matrix

![Priority Matrix](https://res.cloudinary.com/db0kbxvhr/image/upload/c_scale,w_500/v1577996310/Priority-Matrix_q44ll0.jpg)

## Timeframes

| Component | Priority | Estimated Time | Time Invested | Actual Time |
| --- | :---: |  :---: | :---: | :---: |
| HTML Structure | M | 1hr| 30 min | 30min |
| Basic CSS Styles | M | 2hrs| 2hrs | 2hrs |
| Category Buttons | M | 2hrs | 1hr | 1hr |
| API to Display Question and Randomize Position of Answer Choices | H | 4hrs | 4hrs | 4hrs |
| Record User Answers - Evaluate Right/Wrong | H | 4hrs | 2hrs | 2hrs |
| Track Score | H | 4hrs | 30 min | 30 min |
| Finish Game & Display Result | H | 3hrs | 1hr | 1hr |
| Reset Game Function | M | 3hrs | 30 min | 30 min |
| Additional Styling Effects (e.g. Animation, Responsive Media Queries) | L | 2hrs | 6hrs | 6hrs |
| Total | H | 25hrs| tbd | tbd |


## Code Snippet

Effectively implemented code to randomize the position of values in an array for multiple choice questions. Proud of implementing it from Google research results. Oftentimes, I would get overwhelmed and confused by the results I find but I'm getting better at sifting through what works vs. doesn't.  

```
        if (triviaQuestions[i].type === 'multiple') {
            let randomizedAnswers = []
            while(potentialAnswers.length !== 0) {
                let randomIndex = Math.floor(Math.random() * potentialAnswers.length);
                randomizedAnswers.push(potentialAnswers[randomIndex]);
                potentialAnswers.splice(randomIndex, 1)
            }            
            triviaQuestions[i].all_answers = randomizedAnswers; 
        } else if (triviaQuestions[i].type === 'boolean') {
            triviaQuestions[i].all_answers = ['True', 'False']
        }

```

## Change Log
 Finished MVP early, so added visual cues and animations with extra time available.