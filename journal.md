---
title: "EZRouter"
author: "bcon"
description: "cheap but effective cnc router"
created_at: "2025-06-18"
---

## **6/18/2025 Log 1: Decisions, Decisions**

I knew I wanted to make a cnc router. I have also been into additive manufacturing, but subtractive manufacturing has been a field that I had yet to delve into. 

I have a few goals with this project. 

Desktop sized, rigid enough to cut stronger materials, fit in or close to the $350 budget. 

I started off with some research. I needed to determine what motors and spindle I would want to use, along with a rough bed size. 

After a LOT of extensive research, using gpt, reddit, whatever forum I could find I determined that [this](https://www.amazon.com/Daedalus-CNC-Brushed-Motor-KIT/dp/B07VLF63LX?th=1) 500W Brushed DC Spindle Kit was a good starting point for what I wanted. It is a good balance between the cheap 30 dollar 775 spindle that is weaker, and the more expensive brushless spindle. This will be good enough to accurately cut out most of the parts I want to make, and materials I want to work with. 

From there I went into CAD to start laying out key dimensions.
![image](https://github.com/user-attachments/assets/107e7033-f8bc-44e5-a6ff-81077f1e667d)

After working through some CAD sketches, I decided that I wanted at least a 200mm x 200mm cutting area. This is where I started laying out my frame. I wanted to use 2020 and 2040 for the frame as I have access to a large amount of it, but I did not know if it was going to be rigid enough so I did some more research and eventually determined that using mostly 2040 should be fine. 

I then went to 3D CAD to start my frame. I wanted to use linear rails on Y, and after some looing around found a specific extrusion that has a spot built in for mgn12 rails to be flush mounted. It was cool and worked well, so I decided to go for it. After some work, I ended up with this. 

![image](https://github.com/user-attachments/assets/f5d0827c-36af-45ae-83cd-04ceeb68f0a4)

I wanted to do duel carriage as that should be more rigid, but I did spend a few hours trying to figure out the best way to attach the gantry to the system. I also decided on a moving gantry system as that takes up less space than a moving bed. 

![image](https://github.com/user-attachments/assets/098ff6b2-9058-4c8e-bb4c-8e8836b4f597)

I also decided to reduce the footprint this needs by putting the electronics under the system as my bed is stationary. 
![image](https://github.com/user-attachments/assets/9be21cb2-9fe7-42fc-932a-26bf5f21ba80)
![image](https://github.com/user-attachments/assets/caab8807-e5c6-4644-a7ba-dbce37885f70)
I am going to bolt the mdf spoilboard to the 2020 crossbars such that it can easily be replaced when needed. 

Regarding the gantry mounting, I decided on a 3d printed part that uses many, many bolts in order to keep itself rigidly attached. 

![image](https://github.com/user-attachments/assets/c097920e-a14c-44be-8130-84b21a998d29)

This will hold the upright 2040 extrusion that makes up my gantry. 

Time Spent: 8 Hours

## **6/20/2025-6/21/2025 Log 2: Gantry**

After making a frame I was mostly happy with, I moved on to the gantry. Rigidity is important for this. 

![image](https://github.com/user-attachments/assets/b29fba9c-ab11-40a4-a64e-5e8b4447916d)

In all, I ended up making the my z axis, along with the gantry itself. I decided to use mgn12 linear rails combined with a 2040 and 2020 bar to connect the 2 sides and give it something to move on. This is driven by a Nema 23 stepper motor chosen for power. 

I ended up going through a few different versions of the z axis. I started with this monstrosity

![image](https://github.com/user-attachments/assets/f7c69b13-51c9-478d-913a-51651ce986f2)
that used one mgn9 rail and an impossibly weak 3d printed part to hold up the entire spindle. Needless to say, this was not going to work. It was too weak, not rigid enough, and put the spindle out from the gantry way farther than I liked. 

I decided to completely restart over and ended up, after many hours, with this. 

![image](https://github.com/user-attachments/assets/d8d6ba80-ae99-4865-a59b-014fbcb848a0)

This uses a 1/4in aluminum plate, 2 mgn9 rails for stability, and drives the system with a leadscrew down the middle. It is a lot more compact and doesn't bump out the spindle as far. 

Fleshed out, it looks like this. 

![image](https://github.com/user-attachments/assets/ff440313-5477-4e2b-9c6e-fdd8618649bc)

This system is compact, rigid, and should work well for my applications. 

Time Spent: 10 Hours

## **6/23/2025 Log 3: Big Swaps**

After doing some BOM work, I realized something had to change. The price was already way too high, so I decided to see where I could cut costs. I decided to switch back to Nema 17 motors for everything over Nema 23. While they are weaker, I can compensate by going slower with the machine. This was a worthwhile change, as not only did it make the pricing better, the proportions also look better
![image](https://github.com/user-attachments/assets/2b277fe8-1fb5-42c8-a4d4-eed31d2ae7ce)
This changed dropped my BOM by almost 50 dollars, but it is still going to be close. 
![image](https://github.com/user-attachments/assets/f2bd44ca-8a80-40b5-978c-15720df3631a)

Time Spent: 2 Hours

## **6/24/2025 Log 4: Starting the Polish**

Since the bulk of the big decisions were done I decided to polish up the little details. To start, my y axis got a second motor to evenly drive the gantry to keep it from racking
![image](https://github.com/user-attachments/assets/282adf70-31ef-4315-ac5f-40590ba8e9a2)

Then, I created a bearing holder to keep the x leadscrew from being cantilvered over a 250mm long span. 
![image](https://github.com/user-attachments/assets/6bb4047a-8219-49d0-87ee-21be1de13323)
This is huge for rigidity.

Finally, I got the y leadscrews into the CAD and made a part to attach them to the gantry. 
![image](https://github.com/user-attachments/assets/275c4938-24a8-440a-86ca-c4b4c2d7c68d)

There are still a lot of little details that I have to iron out, but this is looking good. 

Time Spent: 4 Hours

## **7/3/2025-7/4/2025** Log 5: More Polish

![image](https://github.com/user-attachments/assets/fb5d21b6-b03d-4480-8575-7e2936f7c24e)

I spent some time tidying up some of the last parts of the router. To start, I set colors to make it easier to see as well as bringing this under the same family as my printer (Since I have plenty of that filament left over)

![image](https://github.com/user-attachments/assets/d2ecf113-d0b0-4913-adb7-df62ed6be9ee)

I also added in the electronics - the control board and the two different power supplies.

![image](https://github.com/user-attachments/assets/87a4e291-9497-4828-a84f-c39e89a6d49e)

Front support plates as well as these linear rail hardstops were added. Finally, I put in the spoilboard from which I will attach all of my raw material to.

Time Spent: 4 Hours
