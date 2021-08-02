# EDC-1
SEE 550 EDC 1
This file contains the analysis of the model created for an airport with two types of planes arriving and departing.

Fernando Uribe
SEE 550
Professor Boadi
EDC 1 

This model begins with a demand module that has two types of planes arriving, small and big. The small planes arrive with an inter-arrival times of exponential (60) and exponential (65) minutes respectively. This module is followed by a queue module made for both types of planes as they await to cross the intersection. Following that is a decision module that assigns a priority of 1 to small planes and 2 to big planes. This allows the decision module to only send small or big planes to their respective boarding gate process module separating each type of plane. Each process module also only accepts its designated type of plane type, adding an extra step of security that a wrong type of plane is being sent over. Only one plane is allowed to go at a time in a first-come first-serve basis. Each type of plane then uses its designated gate and waits with a uniform distribution of (20, 30) for small planes and uniform distribution of (40, 50) minutes for big planes. As soon as one plane leaves the gate, another of the same type goes in to take its place. They then wait in a queue to be inspected that leads on to an inspection point. This inspection requires a uniform distribution wait time of (20, 40) minutes for both kinds of plane that then leads on to a decision module with a 10% chance of extending the inspection. The decision module uses 10% probability of sending the same plane back for inspection before moving on to the take-off queue. One issue I did encounter was that if a plane got held for extra inspection, I could not tell if that same plane would possibly be sent again. This shortcoming has little to no consequences on the overall picture though because it would just mean that plane would go again and still not go over to the takeoff module, keeping the same number of flights documented. No more than 8 planes wait for takeoff as can be seen in the results under the queue when the program runs, meeting the requirements set in the problem statement. Each plane then moves on to the same take-off process module which is uniformly distributed (4, 7) minutes. This model was able to complete a little below 1400 flights in one month (43200 minutes) so in order to meet the requirement of having 39011 flights per month, the airline capacity needs to increase 28-fold. This means 27 additional terminals must be constructed along with the taxiways and gates for each. Additionally, the results show that the run-times are all below 70% and most are below 50% meaning there is room for growth and the people working the stations are not being overworked which indicates a healthy work environment. Below are the utilization rates for each process:

•	Small plane runway: 42.19%
•	Big plane runway: 68.53%
•	Small plane boarding gate: 50.77%
•	Big plane boarding gate: 45.42% 



