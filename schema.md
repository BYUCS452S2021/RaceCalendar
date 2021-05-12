# Schema

## Overview:

Athlete (athlete_id*, first_name, last_name, username, password, email, state, race_counter)

UpcomingRace (upcoming_race_id*, race_id, athlete_id)
- Foreign Key race_id references Race
- Foreign Key athlete_id references Athlete 

SuggestedRace (race_id*)

Race (race_id*, race_title, start_time, date, type, city, state, url)

## Detailed Description:
#### Athlete (athlete_id*, first_name, last_name, username, password, email, state, race_counter)
The Athlete table represents all the users that create an account on the app.

Column explanations:

- athlete_id is the primary key for the Athlete table.
- first_name is the athlete’s first name.
- last_name is the athlete’s last name.
- username is the athlete’s username.
- password is the athlete’s password.
- email is the athlete’s email that they register with.
- state is the state that the athlete lives in.
- race_counter is an integer showing the number of races the athlete has completed in the current year.

#### UpcomingRace (upcoming_race_id*, race_id, athlete_id)
- Foreign Key race_id references Race
- Foreign Key athlete_id references Athlete

Represents all the upcoming races that the athlete is registered for.

Column explanations:
- race_id is the primary key for the UpcomingRaces table.
- athlete_id is the foreign key referencing the Athlete table.

#### SuggestedRace (race_id*)
(Query on the AllRaces table to populate this table)
Represents suggested races that an athlete may sign up for. Based on the state the athlete lives in.

Column explanations:
- race_id is the primary key for the SuggestedRaces table.

#### Race (race_id*, race_title, start_time, date, type, city, state, url)
- Foreign Key athlete_id references Athlete

Represents all the races stored in our database.

Column explanations:
- race_id is the primary key for the SuggestedRaces table.
- race_title is the official name of the race.
- start_time is the hour that the race will begin.
- date is the month, day, and year that the race will take place.
- type is the description of the race (i.e. 5k, marathon, triathlon, etc.)
- city is the city that the race will take place in.
- state is the state that the race will take place in.
- url is the link to the race website, which includes registration and course info.

### Evidence of Normalization:
Every table in the schema contains a key. We have eliminated redundancy from our SuggestedRaces and UpcomingRaces table.
