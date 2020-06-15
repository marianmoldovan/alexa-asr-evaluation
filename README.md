# alexa-asr-evaluation

The purpose of this guide it's to learn how to use the ASR Evaluation tools for Alexa.

The step 0 is to create yourself an Amazon Developer account, it's free and can be done at [developer.amazon.com](https://developer.amazon.com/).

### Step 1. Create an Alexa Skill

Go to the [Alexa developer dashboard](https://developer.amazon.com/alexa/console/ask) and create a new skill.

Name: **my restaurant**
Language: **English (US)**
Model: **Custom**
Host: **Alexa-Hosted (Python)**

Click next

Template: **Hello World**

Import the interaction code from the example, for that, go to **Build**, **JSON Editor**, copy and paste the json from [interactionmodel.json](interactionmodel.json), hit **Save Model** and finally **Build Model**.

After the build has finished, click on **Evaluate Model**, on **Utterance profiler** and type *I want a spanish restaurant* and check that the returned intent is *searchRestaurant*

