# User Onboarding Flow

Here is a complete flow diagram for all user onboarding flow

![Onboarding Flow](onboarding-flow.png?raw=true "Onboarding Flow")


## **Agenda** 

> we want to create a user onboarding flow with minimal number of steps,so that user can easily and quickly onboard onto the application and start exploring the yogifi application.


Before Defining the user Onboarding flow lets first define different kinds of the user.

1. Mat User (user with Yogifi mat and they)
    1. With Trial User Subscription
    3. With Premium Subscription
    2. Without Premium Subscription
2. Non Mat User (User who doesn't have Yogifi Mat.)
    1. With Trial User Subscription.
    2. With Premium Subscription

> Non Mat User cannot practice after the free trail ends 

> Mat User can practice program even after his/her free trail has expired but he/she will not be able to track his different vitals data.

> both above points are open for the discussion 

> However Onboarding flow doesn't depend on the premium and non premium user, it will only get affected a little by the mat and non mat user.


### **Mat User**

here is the flow diagram for the mat user.

![Onboarding Flow](mat-user-onboarding-flow.png?raw=true "Onboarding Flow")

here is the video for the mat calibration flow.

video file need to be added.


### **Non Mat User**

here is the flow diagram for the non mat user.

![Onboarding Flow](non-mat-user-onboarding-flow.png?raw=true "Onboarding Flow")


### **List of Api Required for User Onboarding Flow on different Screen**


1. Splash Screen
    1. account/refreshToken (get)
2. Sigin Screen
    1. account/sigin (post)
    2. account/siginWithGoogle (post)
    3. account/siginWithFacebook (post)
    4. account/siginWithApple (post)
3. Namaste screen
    1. account/profile (post)
4. Welcome Name  screen
    1. account/profile (post)
5. Experience Screen
    1. account/experienceLevel (get)
    1. account/profile (post)
6. Goal Screen
    1. account/goal (get)
    2. account/profile (post)
7. Tall (length) Screen.
    1. account/lengthUnitsAndRange (get)
    2. account/profile (post)
8. Weight Screen.
    1. account/weightUnitsAndRange (get)
    2. account/profile (post)
9. Gender Screen.
    1. account/gender (get)
    2. account/profile (post)
9. Mat Connected Screen.
    1. account/tips
    2. account/profile (post)
10. Start Calibration Screen
    1. program/calibrationProgram


### **User Schema**


```
{
    _id: {
        "$oid": "6374d6747490bd53bd1b2fb8"
    }
    "email": {
        "address": "uday@wellnesys.com",
        "is_verified": true
    },
    "password": "",
    "name": "Uday Mishra",
    "user_type": "student",
    "time_zone":"",
    "experience_level":"",
    "goal": [
        "",
        "",
        ""
    ],
    "lenght":{
        "value": "",
        "unit": ""
    },
    "weight":{
        "value": "",
        "unit": ""
    },
    "gender": ""
    "mat_id": [
        ""
    ],
    "fcm_token": ["",""]
    "created_on": 2021-10-20T07:23:10.043+00:00
    "updated_on": 2021-10-20T07:23:10.043+00:00
}
```