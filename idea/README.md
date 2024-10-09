# Guildies

Guilds session is the regular sessions in an org or an internal community to provide an opportunity for everyone to either demonstrate their capability by hosting a session or increase their knowlege and learn new techs by attending to the sessions.

Session are still doing virtually/online via Microsoft Teams, in the near future we will plan for in-person sessions as well.

Project: Guildies App 
Platforms: Available on Web, PWA on mobiles, MSTeams channels

Design flow:

## [App 1]: Nexus
A central point where engineers connect their knowledge and propose ideas.A place where ideas are crafted and transformed into sessions

**Purpose:** Engineers express interest in hosting sessions, providing details about themselves and their proposed topics.
- An engineer who would like to host a session will register his/her expression of interest including his/her about me part
- the request will then review by guild editors. they could be able to communicate on the topic to understand more and have an option to nourish the idea and eventually approve or reject the guild topic 
- once it's been approved, the engineer will have opportunity to propose a closest date for his/her session
### Tech stacks


## [App 2]: OpsHub
A hub for operational management, providing powerful tools for organizers to coordinate efficiently.

**Purpose:** Organizers manage the guild sessions, including scheduling, notifications, and calendar integration.
- an organizar will then manage the guild sessions in a dashboard portal 
- Once the date has been confirmed a notification will pushed to the engineer for his/her acceptance.
- once the engineer accept, his profile will push to speakers board
- the app will then books a room, publishes the new sessions to the calendars and channels (App Calendar, MSTeams Channel Announcement, Subscribed Emails) and ask for RSVP
- the app should be able to communicate the same way to remind for the upcoming sessions and ask for RSVP
- Anyone who RSVP the session, they will get some additional info about speaker and the session updates
### Tech stacks

## [App 3]: Cronos
A vigilant system, constantly automating tasks, reminders, and managing co-host requests and surveys.

**Purpose:** Background workers handle automated tasks like preparing resources, managing co-hosts, surveys, and blog recommendations.
- A background worker will provide a basic ppt templates, documents, images and resources to the new speacker
- A background worker will request for co-host to help the speakers and their sessions from the editors
- A background worker will check finalized sessions and gather all the available documents and resources to editors 
- A background worker will check finalised sessions and trigger a survey to the participants
- A background worker will check all the sessions that has higher scores to propose the session to be posted in the guild blog
### Tech stacks

## [App 4]: Vault
A secure storehouse for session materials, articles, and session statistics.

**Purpose:** Speakers manage session details, upload documents, track statistics, and view session scores.
- This app is a portal that provides capability to speakers to provide more details on their session including but not limited to documents, slides, references, articles, etc.
- The editors could have an option to assign co-hosts to the sessions
- at the day of the every session, all the participants (anyone who did RSVP) will get additional session resources if available (such as invitation/SWAGS/gifts/vouchers/etc.)
- Once the session has been finalised the editors have an option to score the session based on the quality of the session and the result of the relevant survey
- the speakers will then gets some statistics on his/her profile
- There should be some PowerBi reports and dashboards to demonstrate some statistics
### Tech stacks



## Overall Structure


## [Possible Mobile applications?]

## [Possible Ai integrations?]