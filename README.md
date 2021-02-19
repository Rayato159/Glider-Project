# Gliding Project

 **Submitted by**
 1.	Ruangyot	Nanchiang	B6116736	(Project Manager)
 2.	Sahassawat	Rattanamongkolkul	B6113056	(CAD)
 3.	Kamonlaphat	Sitthitharanon	B6130268	(Documentation)
 4.	Apisit	Butprom	B6005375	(Manufacture)
 5.	Kobsiri	Seedakaew	B6007874	(Manufacture)
 6.	Chonlatorn	Sawangjit	B6007836	(Manufacture)
 
Present to Dr. Atthaphon Ariyarit.  
Semester 2-2563  
Suranaree University of Technology  

**Preface**  
This report is a part of the 537314 Flight Mechanics. The purpose of this report is to explain whole about of glider which we design whether why we need design like this.  
It’s just not only about to glider design but include manufacture, flight testing, inspection after flight testing and financial report.  
We describe step by step for who want to learn how to produce some small glider by our concept.  
This project is full of obstacles, because we just study the mechanics of flight and don’t know as much about aircraft design. Therefore, we used all the knowledge from aerodynamics and this subject by the full of power for produce the best glider as we can.  
Finally, If you read to this. We hope you to get the highest of knowledge by our report.  

**Define Objective**
 1.	Wingspan 1 m
 2.	Reynold number <= 400000 (Incompressible Flow)
 3.	Initial attitude 2 m
 4.	Longest range gliding
 5.	Low weight
 6.	High Cl/Cd and AR
 7.	High stiffness

**Conceptual Design**  
	The most important of glider is about to design for low weight, high Cl/Cd and AR, but in this project. We must design for high stiffness for structural test in another project.
	First step. We need to define wing shape. From objective we need high Cl/Cd and AR then we define chord about 100 mm and we are all know as the best wing shape is elliptic wing (For lift produce on wing. Because elliptic wing has Oswald efficiency number = 1) But elliptic wing is hard to manufacture. Then taper wing is better to manufacture. Taper wing give speed more than rectangular wing for long range gliding. The good taper ratio are about 0.3 to 0.4. We choose taper ratio 0.4 and sweep angle 0 degree because is easy for manufacture. Then choose T tail for stable.
	Next step. We used the RC plane calculator website to define all dimension and improve some dimension for suitability to structure.
	Finally. We used Solidworks CAD software to design this glider, find center of gravity and calculate empty weight. Assume material to balsa wood.

**Airfoils Selection**  
	This step is also equally important, Because to improve Cl/Cd we need to meticulous with airfoil selection.
	First step is about collection airfoils data. (We choose only NACA airfoils for standard) Go to “Airfoil Tools” website and collect all NACA airfoils coordinate point to JavaFoil. In JavaFoil set all parameters (Standard sea levels condition, Re = 400000, M = 0.3) for simulation to find the angle of attack to that give Cl = 0.5 and calculate Cl/Cd.
	Then analytics all data with Python coding and do some machine learning with Scikit learn module to choose the best airfoils.  

We used tree decision model because to define what if we need airfoil that have angle of attack and Cl/Cd  by some value we expect. If wing we need lowest angle of attack and highest Cl/Cd for easy to launch the glider. If stabilizer we need symmetry airfoils and highest Cl/Cd for not disrupt the aerodynamics performance of the wing. what are airfoils we should get. And model score is 0.9833.
Thus, the result is NACA6409 for wing and NACA0008 for stabilizer (But used flat plate for tail because it’s can’t produce in reality for us).

**XFLR5 Simulation**  
	XFLR5 is free software and easy to use for RC plane simulation. This software can analysis airfoils and analysis RC plane. Then. Then pull all information from conceptual design for define boundary conditions and get result below. Assume V = 9 m/s.  
By plane analysis at angle of attack = 0 deg, Cl/Cd = 7.489, Cm = -0.064;

**Performance Calculation**  
	Consider an airplane in power off flight. The force acting on glider are lift, drag and weight. Thrust is zero because power off glider. Assume glider is constant velocity and flight path is horizontal parallel with ground. (L = W; T = D;)  
By the free body diagram is clearly whether if less of theta then range of glider will increase. If we want to know how far of glider can gliding.

R = 14.925 m  
AOT = 7.63 deg  
Sink rate = 1.2 m/s  
E = 1.67 s  
Tr = 1 kg  

**Define Materials**  
	At the first on conceptual Design. We assume all aircraft is filled by Balsa wood because Balsa wood is easy for manufacture, low cost and low weight. But in reality we can’t do that because we need to care about structure. Then we need to do some composite materials for more stiffness.
 
**Manufacture**  
	This process is full of obstacles. Because We have tools and resources in finite. We need to take carefully when we do all the parts by part of aircraft. We do “Handmade Workshop”. 
Step by step
1.	Fuselage: Cut the balsa wood and PE foam then stick together then fillet.
2.	Stabilizer: Cut PE foam for 2 pieces first is vertical stabilizer second is horizontal stabilizer. Then cut some stick of balsa wood and stick together finally stick all to fuselage.
3.	Airfoils: Cut come balsa wood and rasp to airfoils shape we select in first (7 pieces).
4.	Wings: Used 2 carbon stick for wings spar and stick together with airfoils the cut some balsa wood to do bones of wings.
5.	Wings Skin: Attach kite paper to wings.
6.	Finally Step: Attach wing with fuselage by tape.

**Flight Test**
	We took too many times for flight test and back to fix our glider. We do more and more to find the best result as expect. The link below is show some flight test.  
**Result on the real day test our glider can glide about 12.6 m error from theory by 16%.**

**Inspection**
	On the real test day our glider got some problem. There’s no stabilize because the last day before real flight got some damage with the trees too many times. Every time we fix we need to attach glue that will cause to no balance weight. Another problem is about stabilizer is not manufacture good enough.
 
**Financial Report**  
About 1373 Baht.

And finally, We need to say thanks to Mr. Sanya Phanprasert (He is our friend but not study with us.) for facilitate us to used workshop place and borrow tools to work.

**References**
1.	John D. Anderson Jr. Introduction to Flight. 8th ed. New York: McGraw-Hill. 2016
2.	Federal Aviation Administration. Aerodynamics of flight. U.S. Department of Transportation. 2013
3.	Andy Lennon. Basic of R/C MODEL AIRCRAFT DESIGN. Air Age Media Inc. 1996
