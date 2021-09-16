# NFL Health & Safety


## Product Definition
A highly discussed topic as of late, with still far to many unknowns, is the topic of head related injuries in sports and more specifically, CTE in the game of the football. CTE is a term for the degeneration of the brain caused by head traumas. The scariest part of CTE is that it can only be diagnosed after the individual passes away through an autopsy. A new study that was published in the Journal of the American Medical Association, the brains, donated to Boston University, of 202 deceased football players were examined. These players played at a variety of levels from High School all the way up to the NFL. These brains were then analyzed for CTE in conjunction with player history on the field.  Of the 202 players, 87% were diagnosed with CTE while 111 of these players played in the NFL, 110 of which were diagnosed with CTE. This is a very scary, yet very real issue in not on the NFL, but major contact sports and this product aims to help.

Many steps are being taken to mitigate this risk and this project is one them. The mission of this project is to provide data on player “exposures” in an NFL play or game by assign players to their helmets. By “exposures”, we are referring to helmet impacts throughout the game which will give the NFL much more meaningful data when it comes injury surveillance and mitigation techniques. This data can then be used to better diagnosis and treat injuries, while also monitoring players that sustain substantial higher numbers of “exposures”. This information can be used not only for preventative reasons, but also informative reasons in regards to a players future in the sport.

### Links to these articles
- [Time Article](https://time.com/4871597/degenerative-brain-disease-cte-football/)

- [CTE](https://www.mayoclinic.org/diseases-conditions/chronic-traumatic-encephalopathy/symptoms-causes/syc-20370921)

## Users and User Stories
The users of the project is first and foremost the NFL. The NFL wants this information to help mitigate the risk associated with playing in their league and to ease the minds of those concerned with the safety. Secondly, I believe that the NFLPA, or the NFL Players Association, should have access to this information to better self-assess not only their style of play, but their health and duration of career. I truly believe that if players were equipped with this type of information, we would see the way players approach the game differently, along with dramatically shorter careers across all positions. This though may not be something that the NFL wants shared with the players. Thirdly, I believe that medical professionals would be another group of users. This type of information can drastically help in the diagnosis and link to CTE that some players develop. Additionally, employees at AWS will be users as this is something that they will be supporting and monitoring. Lastly, parents and players not in the NFL may use this product as well, assuming they are given access. This will give the ability to make much more informed decisions about their futures in football and whether they allow their children to continue. While these are just a handful of users specific to this football project, I do believe that this product can be applied to many other contact sports.

## MVP
The minimum value product in this case is quite a bit. We first need the video from both angles to be able to have footage of the game to analyze. This footage will be provided by the NFL and AWS. It is vital to this project to have the two locations specified for the camera angle. Next, we need to be able to analyze the distinction between a helmet and not a helmet. We are focused specifically on head traumas and it is vitally important to make sure that other parts of the body or equipment are not counted as the helmet. Some players may take many more body blows than head shots, and that is not something that we can afford to double count. We also need to be able to recognize player number to link the helmet and player together. This is very important to distinguish which players take the most hits to the head and properly diagnose the issue. Lastly, we need to determine what an “exposure” is and collect that information for each player. An “exposure” can mean many different things to different people and that determination needs to be confirmed to attain accurate information.


## Open Source Review
The open source available for the project is through the website Kaggle, with the vast majority of the code holding an Apache 2.0 open source license. This means that I am able to reproduce and distribute copies of the work or derivatives of the work in any form. The open source that I chose to begin my project working with holds this same license, along with the code that it references. This is the 11th version of the project and was updated just 4 days ago, which shows me that it is extremely relevant to the current information provided. This open source uses an adaptation of DeepSort along with helmet mapping, to determine an “exposure” along with the tracking of helmets and their associated players. DeepSort is a type of Deep learning that allows users to track custom objects in a video. Mutiple object detection and tracking will need to be utilized to achieve our goal. The helmet mapping comes from another open source, which is also listed below, and aids in the helmet mapping portion of analysis. This helmet mapping open source, also utilizes another open source to help get things started. All of these open sources have the Apache 2.0 license and allow me to utilize this code for my work.

### Links to Open Source
- [Tuning DeepSort](https://www.kaggle.com/firefliesqn/tuning-deepsort-helmet-mapping)
- [Helmet Mapping](https://www.kaggle.com/its7171/nfl-baseline-simple-helmet-mapping)
- [Starting Guide](https://www.kaggle.com/robikscube/nfl-helmet-assignment-getting-started-guide)



### Image

![alt text](https://www.markdownguide.org/assets/images/tux.png)


