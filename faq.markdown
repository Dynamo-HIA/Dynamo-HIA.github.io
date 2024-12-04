---
layout: single
title: Frequently Asked Questions
permalink: /faq
---

This is the frequently asked question list of the 2.X series.


### General
Q: When I click on the names in the explorer tree nothing happens. 

A: In the DYNAMO program menus appear on right clicking only.

### Running DYNAMO-HIA.exe (on Windows XP)

Q: I want to have some technical background about the software. 

A: The DYNAMO-HIA program has been developed using the Java programming language. 
Its graphical user interface is based on the Eclipse Rich Client Platform.

WinRun4J has been used to make starting the program easy in Windows and provide icons and JFreeChart has been used for making the output plots.

The software runs on a standard Java Virtual Machine and minimally needs version 1.6 (it is configured to only accept this version). The parameters that are passed to the JVM can be found in the DYNAMO-HIA.ini file that can be found in the same directory as DYNAMO-HIA.exe.

Their lines start with “vmarg.” and they are all about memory: 
"-Xms128M" - Means initially 128 Megabytes of memory are made available for the application. 
"-Xmx1024M" - Means 1024 Megabytes is the maximum amount the program is allowed to take. 
"-XX:MaxPermSize=128M" - Means a certain sort of Java memory may not exceed 128 Megabytes.

When you want to run simulations that need more space than the standard configuration allows you may increase the number after –Xmx. Under Windows XP the maximum allowed amount of memory is 3 Gigabytes (approx. 3000 Megabytes) and because Windows needs memory as well setting it above 2048M is not a good idea. The amount of physical memory is important. When the amount of required memory exceeds the available physical memory Windows starts making “virtual” memory. This memory space is created by writing the content of a part of the used physical memory to the hard disk and reusing that physical memory. It is nice to have more space, but the price is usually very high: When the content has to be reloaded another part of memory has to be swapped out to hard disk and that process takes orders of magnitude more time than using physical memory. In practical terms: Your simulation will run extremely slow if its memory use (plus Windows’s memory footprint) exceed physical memory.


### Java heap space
Q: I run a simulation I get the following popup screen: "Errors during configuration of the model Message given: Java heap space"

A: The simulation you are running needs more memory than it allowed to have. See the “Running DYAMO-HIA.exe” on page 96 item in the User Guide and Manual" above for how to increase the amount of memory available as a possible solution for this problem.

### Reference Data Screens

Q: How can I change the risk factor class which has duration dependent relative risks? 

A: You can not change this class anymore. This is because otherwise relative risk files that could already have been entered are not usable anymore. However you can make a new risk factor with another class as the duration class, and import the prevalence and transition rates for this risk factor from the old version of the risk factor.

### Simulation Screen

Q: I can not choose a risk factor that I have entered in the reference data. 

A: Risk factors can only be chosen as they have been completely defined in the reference data section. For risk factors this means that there must be minimally a valid prevalence file and a valid transition file present.

Q: I can not choose a disease that I have entered in the reference data. 

A: Diseases can only be chosen as they have been completely defined in the reference data section. For disease this means that there must be minimally valid prevalence, incidence, excess mortality and dalyweights files present.

Q: I can not chose the right transition or prevalence file name on the scenario tab.

A: The first reason for this might be that model does not allow you to chose both the transition file and the prevalence file to be equal to that on the reference tab. So this Sometimes version 1.0 does not refresh the dropdown lists.

### Output screen

Q: On the “change scenario settings” tab I do not see any sliders and buttons to change the scenario. 

A: These sliders and buttons are only present when one or more an alternative scenario has be requested. When only the “business as usual” (reference) scenario is run, no such buttons are present, as they only apply to alternative scenarios.

Q: I do not see the legend of some of the figures. 

A: The plots in the output windows of DYNAMO-HIA have a fixed size. Maximize the output window. On low resolution screens this might not be sufficient. In that case increase the resolution of the screen to 768 pixels in the vertical direction (e.g. 1048 by 768). 