concise guide to install ROS on Ubuntu using VirtualBox:


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
![11111](https://github.com/user-attachments/assets/c337e0bf-dd74-44c8-88f5-9fda654b32b3)


5. Setup ROS Sources:

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'    

6. Add ROS Keys: 
   sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
   

9. Update Package Index:
   sudo apt update
   

10. Install ROS:
   ![Uploading Install ROS noetic .png…]()
   

11. Initialize rosdep:
    sudo rosdep init
    rosdep update
    

12. Setup ROS Environment:
    echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
    
14. Install Dependencies for Building Packages:
    sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
    

