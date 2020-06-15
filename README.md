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

Now, you have to options, one, to upload the audios or to record them with your computer's microphone. Download the [audios.zip](audios.zip) file that contains 5 audios, uncompress them and then upload the files along with the next utterances:

+ Audio: *pulpo.mp3*, Utterance: *pulpo a la gallega*
+ Audio: *pulpoalagallega.mp3*, Utterance: *i want pulpo a la gallega*
+ Audio: *iwanttomakeareservation.mp3*, Utterance: *i want to make a reservation*
+ Audio: *findakoreanrestaurant.mp3*, Utterance: *find a korean restaurant*
+ Audio: *iwantareservationforsaturday.mp3*, Utterance: *i want a reservation for saturday for 2*
+ Audio: *findarestaurant.mp3*, Utterance: *find a restaurant*

Your annotation set should look like:
![Annotation set](/screenshots/annotation-set.png)

Click **Save Annotation Set** and follow up.

### Step 3. Test an annotation set

Go back to your interaction model, clicking any Intent. Hit the **Evaluate model button**, **ASR Evaluation**, select the annotation set you've just created and run a test, you should get:
![test](/screenshots/test.png)

### Step 3. Improve your model

Now you can see the failures and uncorrect transcriptions. 

Let's map the values and improve our results. First, let's map the utterance **pulpo a la gallega** as a synonym for **spanish** in the **foodType** slot, you should have:
![Map slot](/screenshots/map-slot.png)

And then, map the utterance **i want pulpo a la gallega** to the **searchRestaurant** and mark **pulpo a la gallega** as **foodType** slot. You should see:
![Map slot](/screenshots/map-intent.png)






