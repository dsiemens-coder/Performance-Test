# Overview  
  
The Project is developed to set up an performance Test on the https://integrateit-41c60.web.app/openapi/home tool.
	
# Requirements
- Internet Connection
- Java RunTime Environment (JRE) or Java Development Kit (JDK) version 1.8

# Setup

* Generate a new private key for your firebase DB and save the JSON file.
    * Help: https://firebase.google.com/docs/firestore/quickstart#java_1
* Rename file to firebase-admin-file.json.
* Save file in \PerformanceTest dir.
* Execute UiStarter class.

# Instructions

## How to initialize the Test
1. Start the UI.
2. Modify test settings.  
    2.1 Type in the number of entities N, generated for the test.
    
    2.2 Type in complexity c of test network.
        
    2.2.1 Define C
    * If C = 0, then the Network will only have one dimension and there will be only one path from Node 1 to Node N
    * If C = i, then every Node will have i additional edge(s) to (an)other randomly assigned node(s)
   
    2.2.1 Define C_lowerBound
     * If C_lowerBound = C, then every Node will i additional edge(s) to (an)other randomly assigned node(s) 
     * If C_lowerBound < C, then every Node will have in a randomly assigned number r of additional edge(s) to (an)other randomly assigned node(s). R will be in between C_lowerBound and C.
     * If C_lowerBound > C, this case will be treated as C_lowerBound = C 
    
    2.3 Define if loops in test networks are allowed.
3. Create test setup by clicking "Create Test".

## How to execute the Test
1. Initialize the test.
2. Goto https://integrateit-41c60.web.app/openapi/transformation
3. Select first entity (Performance Test - 1) as source.
3. Select last entity (Performance Test - [N]) as target.
4. Select only operation and response of source & target.
5. Execute test. 

## How to cleanup the DB after the Test
1. Cleanup DB from test entities by clicking "Delete Test Entities".

