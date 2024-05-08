## Tutorial 10
Nama: Sita Amira Syarifah

NPM: 2206023023

Kelas: C

### Result of Execution<br>
![image](https://github.com/sitaamirasyarifah/tutorial10-adpro/assets/122429830/cc9f97c8-3f89-4247-82e1-9ef7389e4587)

The output above indicates that "hey hey" is printed before "howdy!" and "done!" because in the program code, the `main` function executes the print command "hey hey" first, followed by executing the two print commands in the queue queue in the executor.

### Multiple Spawn<br>
![image](https://github.com/sitaamirasyarifah/tutorial10-adpro/assets/122429830/e15aea3c-5d88-44fc-a26a-04c0fa5866dc)

### Without : `drop(spawner);`<br>
![image](https://github.com/sitaamirasyarifah/tutorial10-adpro/assets/122429830/89ee2357-be55-45c9-82e3-6db4db2d256d)

### Back using : drop(spawner);`<br>
![image](https://github.com/sitaamirasyarifah/tutorial10-adpro/assets/122429830/e15aea3c-5d88-44fc-a26a-04c0fa5866dc)


From the results of the experiment, it can be seen that when running multiple spawns, all spawned tasks are executed simultaneously. In the program code, there is a timer that delays printing all "done" strings for 2 seconds. Therefore, the program will print all "howdy" strings first before proceeding to print all "done" strings. If the statement `drop(spawner)` is removed, the program will still run as usual, but it will not finish because the function `drop(spawner)` itself is to inform the program that there will be no more tasks added to the executor. Thus, if `drop(spawner)` is removed, the program will continue to wait for the arrival of new tasks.