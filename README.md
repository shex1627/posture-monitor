## How to Setup
* Step1. train your own posture model via [teachable machine](https://teachablemachine.withgoogle.com/train/pose) and upload the model to Google cloud
    Use class1 as correct posture
    Class2 as bad posture.
    
    I created around 150 good-posture images, and ~180 bad-posture images, including 
        leaning left, leaning right and leaning in.  
    remember to backup all your training images and model locally.
* Step2. copy the model link and replace the link in the html code
* Step3. open the html file in Chrome upon use

## How to use

* click `start` button to start camera input and model prediction
* input `session length` in seconds in text box
* click `count down` to start a posture monitoring session. It tracks the number of seconds/total seconds you hold a `correct posture`. A sound alert will be triggered if you score <=1 in the last 5 seconds (variables that you can adjust in the html file).

## Export session data to csv file
You can export your session's score over time by clicking `export CSV`. The csv file format is the following  
`<epoch timesteamp>_<session length in minutes>m_<input activity(replace any space with '-')>`  
note when you `paused` and `unpaused` a session, all the seconds in-between will be `undefined`.
