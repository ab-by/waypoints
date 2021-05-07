# waypoints

Pre-requisites : Gazebo9, ardupilot


Make sure that you have cloned the khancyr plugin following previous repositories , if not follow these steps


                         git clone https://github.com/khancyr/ardupilot_gazebo


                            cd ardupilot_gazebo


                                mkdir build


                                  cd build

 
                                    cmake ..


                                   make -j4


                                sudo make install



                  echo 'source /usr/share/gazebo/setup.sh' >> ~/.bashrc



Now we are Setting path for models follow these steps



                  echo 'export GAZEBO_MODEL_PATH=~/ardupilot_gazebo/models' >> ~/.bashrc



                                . ~/.bashrc
                                
                                
After these steps you are good to go with the setup, keep this mov.py file in your home directly and follow following steps for execution


Run Simulator in one terminal

                                                  gazebo --verbose ~/ardupilot_gazebo/worlds/iris_arducopter_runway.world 


launch SITL in another terminal


                                                       cd ~/ardupilot/ArduCopter/
                                                 sim_vehicle.py -v ArduCopter -f gazebo-iris --console



Fly drone through this command in another yerminal with this the drone will follow the waypoints as instructed in this mov.py code.

 
                                                 python mov.py
