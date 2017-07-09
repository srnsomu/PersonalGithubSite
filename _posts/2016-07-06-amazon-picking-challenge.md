---
layout: page
title: Amazon Picking Challenge 2016 - Leipzig, Germany
author: Feroze Naina
---

Amazon Picking Challenge is a competition for designing a robot system to complement Amazon's Kiva shelf system in warehouses. The workspace consists of a 12-bin shelf and a storage box. Each shelf bin can have multiple items placed in any configure with partial occlusions. A task list is provided of the required items. The goal is to pick the correct item from the bin and place it in the storage box. 

As a part of MRSD course project, our 5-person team worked on the project from September 2015 to May 2016. You can see our course project webpage  at [http://mrsdprojects.ri.cmu.edu/2015teamd/](http://mrsdprojects.ri.cmu.edu/2015teamd/). During this period, we designed the system from the ground up.

We were mentored by Prof. Maxim from the Search Based Planning Lab at CMU. We intially developed the system on a Willow Garage PR2 robot but found its reachability too poor for our task - in order to reach all the regions in our shelf, we would have had to change the spine height and move the robot, both of which would have added a layer of complexity in planning and increased time. Universal Robots was kind enough to lend us a UR5 arm. Migrating our code to the UR5 was a breeze. We were super psyched when we were shortlisted as finalists sometime in February 2016.

During summer, 3 members of our team started their internships in California. We would work on this project in the evenings after work and during weekends.

**Day -1:** June 27

We disassembled and packaged the robot, mounting frame, controller, items and the two computers. It was 450lbs between 4 of us. We had decided to take the robot as a check-in luggage instead of shipping it before as it would buy us more development time.

**Day 0:** June 28

We were scheduled to fly out of Pittsburgh in the afternoon and reach Berlin on June 29, just in time for the robot setup and testing day. As Murphy's law would have it, our connecting flight to Newark got cancelled twice due to ATC issues. We spent the night camping at the airport as the next available flight was in the morning.

Fort HARP!
![Fort HARP!]({{ site.url }}/assets/IMG_2510.JPG)

**Day 1:** June 29

Spent in airports and air. Our quickest route to Berlin was to fly backwards to Chicago, go to Frankfurt and then to Berlin. We were super concerned about our robot cargo not making it on time.

**Day 2:** June 30

We finally landed in Berlin! We were delayed by 28 hours. We rented a Peugot and raced to Leipzig on the Autobahn. Rick and Bhatia had already got there before us.

Today was the practice run day where we get and item arrangement closest to the competition - a mock competition.We saw a lot of teams tweaking their perception system to adjust to the warehouse lighting.

We turn up at the conference venue and frantically unpacked and setup our robot. Much to our chagrin, we found our computer cases smashed with dangling CPU cooler, RAM and the power supply cables. Thankfully, we could patch it up enough.

Then our linear actuator wasn't being powered properly, our linear power supply wasn't working and our shop-vac suction system was super loud. Power supply conked. Then we realized we were powering 110VAC 60hz equipment with 240VAC 50Hz. In my hurry, I mistook the power junction box to be a 110VAC-240VAC. We had to run out and get a new Shop-vac. We then rigged a power source for the linear actuator using a drill battery! 

Kinect was giving *very* noisy pointclouds. Later we learnt it was due to the Halogen lamps which emit IR.
Our Kinect was 2 - using Time of Flight instead of structured light which was more immune.



**Day 3:** July 1st

Stow task finals

We finally got it up and running.
//pic

Due to an error, we were giving the wrong JSON file. So we had to run twice. First time, we stowed 7 items we got 88. Second item, we stored 8 items but misidentified one, fetching us 77. 

We were placed 6th in the stowage competiton out of the 16 finalists.

// talk about our performance and other teams

Delft did really well. They were done and had 6 minutes to spare.

// pic - show our system
// pic - show final scores?


**Day 4:** July 2nd

Picking task finals
// talk about our performance and other teams

We made a decision to modify logic for certain items in fear of dropping. We had a lot of time and were looping between 2 shelves. 7/12 items

4 items - 33 points

We were placed 7th in picking.

evening was reception


There was this kid from UAE who must have been in 5th or 6th grade. He was asking the MIT team member what language his robot was programmed in and was noting it down in Arabic!

**Day 5:** July 3rd

Demo and media day

Each team had a 15 minute presentation. And there were a lot of people asking questions about sub-systems


**Day 4:** July 4th

Return to pittsburgh
 Just in time to catch the 4th of July fireworks!

Overall, it was awesome and we were very happy with our performance.
We would like to thank John Dolan, Dimi and Maxim for their support throughout this competition.

Team HARP had a successful run! We would be handing over the project to the next year's MRSD team
