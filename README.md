# Woof
A synthetic monitoring system. 

## Table of contents
* [General Info](#General info)
* [Prerequisites](#Prerequisites)
* [Setup](#Setup)
* [How to Run](#How to run)
* [Technologies](#Technologies)
* [Contributors](#Contributors)
* [Demo](#Demo)
* [Future Improvements](#Future improvements)

## General Info
The synthetic monitoring system measures the time of the process starting with an API call and ending with event delivery. It returns the total time is taken, minimum, maximum, and average time.
* Team: IoT Execution team
* Period: May 18, 2020 - Aug 21, 2020

## Prerequisites
* Must use Open JDK 11

## Setup
To run this project, run docker locally:

```
$ docker-compose up -d
```

## How to Run
* Open two terminal for `goalie` and `woof`
```
$ ./gradlew goalie:bootRun
```
It will be ready to receive events from `woof`
```
$ ./gradlew woof:bootRun
```
It will send events to `goalie` in every 5 seconds     
It will also read events from `goalie`

## Technologies
* Java
* Spring Boot
* Gradle
* Spock
* Groovy

## Contributors
[//]: contributor-faces
<a href="https://github.com/hyunjineeey"><img src="https://avatars3.githubusercontent.com/u/46205089?s=400&u=3089ab4d55f576fd12690831e69246e8d4d812b1&v=4" title="Jin Jae" width="80" height="80"></a>
[//]: contributor-faces

## Future Improvements
* Report the time result to DataDog
* Finish up the integration testing as it's only done with the unit testing
* Could use KCL in the background to handle the multiple consumers from Kinesis
* Remove the manual code of time measurement and use JVM library instead

