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

### Step 2. Create an ASR Annotation Set

Go to the **Annotation Sets** tab, and select the **ASR Evaluation** option.

Here you can see the annotation sets you have configured for this skill, if you followed the steps in order, you shouldn't have any. So click on create annotation set.

Name it to: **SkillTest.v0**

Now, you have to options, one, to upload the audios or to record them with your computer's microphone. Upload the following files and add the utterances:

+ Audio: [pulpoalagallega.mp3](audios/pulpoalagallega.mp3)</a>, Utterance: *i want pulpo a la gallega*



