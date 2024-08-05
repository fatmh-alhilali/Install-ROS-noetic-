concise guide to install ROS on Ubuntu using VirtualBox:

![Uploading Install ROS noetic .png…]()

1. Install VirtualBox: [official website](https://www.virtualbox.org/).

2. Download Ubuntu ISO: file from the [Ubuntu website](https://ubuntu.com/download/desktop).

3. Create a New Virtual Machine:
- Open VirtualBox and click "New".
  ![Oracle VM VirtualBox Manager ](https://github.com/user-attachments/assets/0db60ac6-9934-4aed-8a98-074a469d7c8c)

- Name the VM, select "Linux" as the type and "Ubuntu (64-bit)" as the version.
  ![Oracle VM VirtualBox Manager 01_02_46 06_57_21 م](https://github.com/user-attachments/assets/e3ea251e-ff98-41db-afb9-7d01fd052fd9)

- Allocate memory (at least 4GB).
  ![Oracle VM VirtualBox Manager 01_02_46 07_01_05 م](https://github.com/user-attachments/assets/b0f845b1-038e-4900-8368-aa25a9080e13)

- Insert the Ubuntu ISO disk you downloaded.
  
  ![f  Running  - Oracle VM VirtualBox ](https://github.com/user-attachments/assets/e3078d80-5508-47f3-8182-6a5dc2b74483)


4. Install Ubuntu:
- Start the VM and select the Ubuntu ISO as the startup disk.
- Follow the installation prompts to install Ubuntu on the virtual machine.

5. Setup ROS Sources:
   bash
   sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    

6. Add ROS Keys:
   bash
   sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
   

7. Update Package Index:
   bash
   sudo apt update
   

8. Install ROS:
   bash
   sudo apt install ros-noetic-desktop-full
   

9. Initialize rosdep:
    bash
    sudo rosdep init
    rosdep update
    

10. Setup ROS Environment:
    bash
    echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
11. Install Dependencies for Building Packages:
    bash
    sudo apt install python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
    

