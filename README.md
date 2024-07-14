# sara_shield_forest_recipes
Collection of forest recipes for CONCERT with sara_shield. 

# How to use
```
[sudo] pip3 install hhcm-forest
mkdir my_workspace && cd my_workspace
forest init
source setup.bash
forest add-recipes git@github.com:TUM-CONCERT/sara_shield_forest_recipes.git --tag master
forest <recipe-name> -j 4 
```

To set up the CONCERT project workspace, follow the instructions listed here: https://github.com/TUM-CONCERT/sara-shield-stack-CONCERT

# Modifications from ADVRHumanoids/multidof_recipes
* `tum_catkin_ws.yaml`
 
    Contains a list with all relevant Repositories that are ROS packages, and should therefore be cloned into the `catkin_ws`

* `tum_src.yaml`

    Contains a list with all relevant Repositories that are non-ROS packages. These should be cloned outside the `catkin_ws`

* `concert_msgs.yaml`
    
    Contains build instructions for the ros package [concert_msgs](https://github.com/ADVRHumanoids/concert_msgs)

* `eigen34.yaml`
    
    Contains build instructions for Eigen 3.4. Note that Eigen3.4 is not installable with `apt` in Ubuntu 20.04

* `human-gazebo.yaml`
    
    Contains build instructions for the ros package [human-gazebo](https://github.com/TUM-CONCERT/human-gazebo)

* `sara-shield.yaml`

    Contains build instructions for the sara-shield-xbot2 repository [sara-shield-xbot2](https://github.com/TUM-CONCERT/sara-shield-xbot2)

* `rviz_plugin_humans.yaml`
    
    Contains build instructions for the ros package [rviz_plugin_humans](https://github.com/TUM-CONCERT/rviz_plugin_humans)

* `rviz_plugin_sara_shield.yaml`
    
    Contains build instructions for the ros package [rviz_plugin_sara_shield](https://github.com/TUM-CONCERT/rviz_plugin_sara_shield)

* `sara_shield_utils.yaml`
    
    Contains build instructions for the ros package [sara_shield_utils](https://github.com/TUM-CONCERT/sara_shield_utils)


# Notes

*Note #1* to enable the *xeno flags*, you can use the command `forest -m xeno <recipe-name> -j 4`

*Note #2* to enable the xacro generation for robot repositories, you can use the command `forest -m xacro_gen <recipe-name> -j 4`
