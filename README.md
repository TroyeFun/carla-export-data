# Carla Export Data
Generating training data from the Carla driving simulator in the KITTI dataset format. Supports Carla 0.9.13.

![Screenshot_3](https://user-images.githubusercontent.com/30608533/58124632-5c87b380-7c17-11e9-907b-f7cfdbb697a7.jpg)



## KITTI dataset format

### An example of KITTI dataset format
- poses
    - 00.txt
    - 01.txt
    - ...
- sequences
    - 00
        - image_2
            - 000000.png
            - 000001.png
            - ...
        - velodyne
            - 000000.bin
            - 000001.bin
            - ...
        - label_2
            - 000000.txt
            - 000001.txt
            - ...
        - calib.txt
        - times.txt
    - 01
        - ...
    - ...


## Running the client after running the Carla Server

```bash
# Run carla server
$ cd carla_docker
$ ./docker_run_carla.sh

# Run the client
$ cd /path/to/repo
$ python export_data.py

# Visualize carla data if needed (in a new terminal)
$ bash carla_docker/run_carlaviz.sh

# Stop carla server after data generation
$ cd carla_docker
$ ./stop_carla.sh
```


### References:

-  KITTI Vision Benchmark Suite    
[KITTI website](http://www.cvlibs.net/datasets/kitti/raw_data.php)
-  Karlsruhe Institute of Technology  
[Karlsruhe Institute of Technology website](http://www.kit.edu/english/index.php)
-  Toyota Technological Institute at Chicago 
[Toyota Technological Institute website](https://www.ttic.edu/)
-  Carla-training-data [github](https://github.com/enginBozkurt/carla-training-data)
-  Carla PythonAPI example - automatic_control.py [github](https://github.com/carla-simulator/carla/blob/0.9.13/PythonAPI/examples/automatic_control.py)

