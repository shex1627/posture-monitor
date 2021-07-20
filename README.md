## How to Setup
1. Train your own posture model via [teachable machine](https://teachablemachine.withgoogle.com/train/pose) and upload the model to Google Cloud.
    - Use Class1 for correct posture and use Class2 for bad posture.
      - I created around 150 "good posture" images, and around 180 "bad posture" images, including leaning left, leaning right and leaning in.
      - Remember to backup all your training images and model locally.
2. Copy the model link and replace the link in the HTML markup.
3. Open the HTML file locally in Chrome to use.

## How to Use

1. Click `Start` button to start camera input and model prediction.
2. Input `Session Length` in seconds in text box.
3. Click `Count Down` to start a posture monitoring session. It tracks the number of seconds/total seconds you hold a `correct posture`. A sound alert will be triggered if you score <=1 in the last 5 seconds (variables that you can adjust in the html file).

## CSV Session Export
You can export your session's score over time by clicking `export CSV`. The CSV filename will be generated as the following:

```
<epoch timesteamp>_<session length in minutes>m_<input activity(replace any space with '-')>
```

Note when you `paused` and `unpause` a session, all the seconds in-between will be `undefined`.
