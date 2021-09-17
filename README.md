# NFL Health & Safety


## Product Definition
A highly discussed topic as of late, with still far to many unknowns, is the topic of head related injuries in sports and more specifically, CTE in the game of the football. CTE is a term for the degeneration of the brain caused by head traumas. The scariest part of CTE is that it can only be diagnosed after the individual passes away through an autopsy. A new study that was published in the Journal of the American Medical Association, the brains, donated to Boston University, of 202 deceased football players were examined. These players played at a variety of levels from High School all the way up to the NFL. These brains were then analyzed for CTE in conjunction with player history on the field.  Of the 202 players, 87% were diagnosed with CTE while 111 of these players played in the NFL, 110 of which were diagnosed with CTE. This is a very scary, yet very real issue in not on the NFL, but major contact sports and this product aims to help.

Many steps are being taken to mitigate this risk and this project is one them. The mission of this project is to provide data on player “exposures” in an NFL play or game by assign players to their helmets. By “exposures”, we are referring to helmet impacts throughout the game which will give the NFL much more meaningful data when it comes injury surveillance and mitigation techniques. This data can then be used to better diagnosis and treat injuries, while also monitoring players that sustain substantial higher numbers of “exposures”. This information can be used not only for preventative reasons, but also informative reasons in regards to a players future in the sport.

### Links to these articles
- [Time Article](https://time.com/4871597/degenerative-brain-disease-cte-football/)

- [CTE](https://www.mayoclinic.org/diseases-conditions/chronic-traumatic-encephalopathy/symptoms-causes/syc-20370921)

## Users and User Stories
The users of the project is first and foremost the NFL. The NFL wants this information to help mitigate the risk associated with playing in their league and to ease the minds of those concerned with the safety. Secondly, I believe that the NFLPA, or the NFL Players Association, should have access to this information to better self-assess not only their style of play, but their health and duration of career. I truly believe that if players were equipped with this type of information, we would see the way players approach the game differently, along with dramatically shorter careers across all positions. This though may not be something that the NFL wants shared with the players. Thirdly, I believe that medical professionals would be another group of users. This type of information can drastically help in the diagnosis and link to CTE that some players develop. Additionally, employees at AWS will be users as this is something that they will be supporting and monitoring. Lastly, parents and players not in the NFL may use this product as well, assuming they are given access. This will give the ability to make much more informed decisions about their futures in football and whether they allow their children to continue. While these are just a handful of users specific to this football project, I do believe that this product can be applied to many other contact sports.

## MVP (Minimum Value Product)
The minimum value product in this case is quite a bit. We first need the video footage of the game. We need that video footage to be from the endzone view and the sideline view to be able to properly analyze the game. This footage will be provided by the NFL and AWS in this case. It is vital to this project to have the two locations specified for the camera angle. Next, we need to be able to analyze the distinction between what is a helmet and not a helmet. We are focused specifically on head traumas and it is vitally important to make sure that other parts of the body or equipment are not counted as the helmet. Some players may take many more body blows than head shots, and that is not something that we can afford to double count. This comes in the form of helmet mapping and four our situation, this is part of the MVP. We also need to be able to recognize player number to link the helmet and player together. This is very important to distinguish which players take the most hits to the head and properly diagnose the issue. We can again run into the issue of double counting if the numbers of the players are incorrectly predicted. Lastly, we need to determine what an “exposure” is and collect that information for each player. An “exposure” can mean many different things to different people and that determination needs to be confirmed to attain accurate information. There needs to be a standard for counting an exposure and apply it to our video.


## Open Source Review
The open source available for the project is through the website Kaggle, with the vast majority of the code holding an Apache 2.0 open source license. This means that I am able to reproduce and distribute copies of the work or derivatives of the work in any form. The open source that I chose to begin my project working with holds this same license, along with the code that it references. This is the 11th version of the project and was updated just 4 days ago, which shows me that it is extremely relevant to the current information provided. This open source uses an adaptation of DeepSort along with helmet mapping, to determine an “exposure” along with the tracking of helmets and their associated players. DeepSort is a type of Deep learning that allows users to track custom objects in a video. Mutiple object detection and tracking will need to be utilized to achieve our goal. The helmet mapping comes from another open source, which is also listed below, and aids in the helmet mapping portion of analysis. This helmet mapping open source, also utilizes another open source to help get things started. All of these open sources have the Apache 2.0 license and allow me to utilize this code for my work.

### Links to Open Source
- [Tuning DeepSort](https://www.kaggle.com/firefliesqn/tuning-deepsort-helmet-mapping)
- [Helmet Mapping](https://www.kaggle.com/its7171/nfl-baseline-simple-helmet-mapping)
- [Starting Guide](https://www.kaggle.com/robikscube/nfl-helmet-assignment-getting-started-guide)

-----------------------

## Outputs

### Running Analysis
When I looked at running the code and attempting to simulate results, I first needed to make sure all necessary libraries were installed. This was necessary to be able to import the needed libraries in the code. Once this was done, I then needed to make sure that I had the correct files downloaded for the code to read, while also making sure that the filepath to these files was correctly indicated in each block of code. Parts of the code were correctly simulated, while others have been running for 15+ hours. Shown below is video that is going to be our end product and gives of visual of how the DeepSort algorithm works along with helmet mapping. 

For this example, we were given the two following videos, one with a angle from the endzone, and the other with an angle from the sideline. Both starting videos are shown below.


https://user-images.githubusercontent.com/74614080/133801835-4213a1dd-f89b-4d28-9a22-8f88bd6f6880.mp4



https://user-images.githubusercontent.com/74614080/133801859-285549a9-6321-4768-bdd5-41d4de569a7a.mp4

### After Application
We can see even before the video is played, the helmet mapping being done on each player in the cameras view. We can see all the players in the green and yellow uniforms have an H and then a number above their heads, representing their jersey number. The H stands for home in this case, while the opposing team has a V for visitors above their helmets. As we play the video, we can see that video pauses for a second everytime an "exposure" is detected, and the associated players helmet box changes colors. This gives us not only a visual representation of overall exposures, but by having the video pause for a split second, it indicates to the viewer that an exposure has occured at this time period and to take notice. We can see how powerful this video can be for the different types of users listed above and will give meaningful information that can change lives forever.


### Video Example

[Video Example of DeepSort](https://user-images.githubusercontent.com/74614080/133792317-c50d7445-8258-4476-8b32-555336f0b6c2.mp4)



### Data Example
Attached below is a csv file of about 5500 rows data. Each row of data contains the video frame and the data on the helmet mapping box at that time frame. It shows the bounding box of the left side, along with the width of the box, the top of the box, and the height of that box. It also gives the predicted label of the player that the helmet mapping box is assigned to, in this case, his jersey number. This is what the competition is judged on and provides a metric to determine if the helmet mapping is correct. In the case of this code, it is correct. I have also attached a screenshot of the beginning of this file to give an idea of how this data is formatted.

![Example of Data Format](https://user-images.githubusercontent.com/74614080/133804035-6f83eac3-ceac-41f0-938c-fbd94cfa4cad.png)


[Helmet Mapping Data](https://github.com/Nhildenbrand19/EC601_Project1/files/7186354/submission.csv)

