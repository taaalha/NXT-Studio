# Implementing recipe as a state machine in a batch control system
The goal of this program was to implement 2 recipes for 2 different products in the same controller using state-based design in IEC 61499 standard. 

To start the process, the water should go to an Initial Level and Temperature using the START button in the HMI, which should be followed by either of the 2 product
recipes as per selected on the HMI screen. 

# Product 1

- Upon selection of product 1, the tank should drain and go to level 0 and temperature 0
- After the tank has been drained, the tank should go to level X1 and temperature Y1
- After it has approached the setpoint X1 and Y1, it should change and go to level X2 and temperature Y2
- After the tank has approached setpoint X2 and Y2, it should change and go to level X1 and keep the temperature at Y2
- Upon attaining setpoint X1 and Y2, the process would be considered complete


# Product 2
- Upon selection of product 2, the tank should drain and go to level 0 and temperature 0
- After the tank has been drained, the tank should attain level X3 and temperature Y3
- After the tank has attained setpoint X3 and Y3, the process should wait for time T1
- After time T1 has elapsed, the system should go to setpoint X4 and Y4
- After approaching setpoint X4 and Y4, the system should wait for time T2
- After time T2 has passed this system should go back to the initial level and temperature
- Once, the initial temperature and level have been attained the process would be termed complete

During the full process the following aspects are to be considered:
- If the product 1 button is active, then neither the product 2 or the sliders can function i.e. at one point only one product can run
- Once a product has been initiated it has to finish the cycle before some other product or the sliders can be used

# Set points

| Set Points    	| Values 	|
|---------------	|--------	|
| initial level 	| 100    	|
| initial Temp  	| 50     	|
| offset        	| 75     	|
| X1            	| 248    	|
| Y1            	| 78     	|
| X2            	| 359.50 	|
| Y2            	| 40.50  	|
| X3            	| 255.45 	|
| Y3            	| 65.10  	|
| T1(secs)      	| 3      	|
| X4            	| 160    	|
| Y4            	| 51.50  	|
| T2(secs)      	| 5      	|

# Some Screenshots
![image](https://user-images.githubusercontent.com/87899535/135578355-0005b028-0497-4ab9-99d7-54bee691cbb8.png)
![image](https://user-images.githubusercontent.com/87899535/135578471-c3f81469-9aff-4af8-a87e-9dc1f31b2e49.png)
![image](https://user-images.githubusercontent.com/87899535/135578550-cfd9661f-af07-4418-859d-5f1bc8fc68cf.png)

**Note**: This exercise was part of the course ELEC-C8201 "Control and Automation" at Aalto University Finland.

