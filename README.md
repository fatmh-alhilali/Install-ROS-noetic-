خطوات تثبيت ROS على نظام Ubuntu:

1. إعداد VirtualBox وUbuntu


   ![Install ROS noetic ](https://github.com/user-attachments/assets/6bfa77b7-aa35-46dc-9183-0cd09a5a0a22)

1. تنزيل VirtualBox: (https://www.virtualbox.org/).
2. تنزيل Ubuntu ISO: (https://ubuntu.com/download/desktop).

2. إعداد الجهاز الوهمي في VirtualBox
1. إنشاء جهاز وهمي جديد:
   - افتح VirtualBox وانقر على "New".
   - اختر اسمًا للجهاز، نوع النظام "Linux"، والإصدار "Ubuntu (64-bit)".
2. تخصيص الذاكرة: حدد 4 جيجابايت على الأقل.
3. إنشاء قرص صلب وهمي: اختر "Create a virtual hard disk now"، نوع VDI، تخزين "Dynamically allocated"، حجم 25 جيجابايت على الأقل.
4. إضافة صورة Ubuntu ISO: في إعدادات الجهاز الوهمي، انتقل إلى "Storage" وأضف ملف ISO.

3. تثبيت Ubuntu
1. بدء الجهاز الوهمي: انقر على "Start" واختر تثبيت Ubuntu.
2. تثبيت Ubuntu: اتبع التعليمات على الشاشة لتثبيت النظام.

4. تثبيت ROS على Ubuntu
1. إعداد مصادر ROS:
   bash
   sudo apt update
   sudo apt install curl
   curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
   sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   
2. تثبيت ROS:
   bash
   sudo apt update
   sudo apt install ros-noetic-desktop-full
   
3. تهيئة ROS:
   bash
   echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
   sudo apt install python3-rosdep
   sudo rosdep init
   rosdep update
   

5. التحقق من التثبيت
1. *تشغيل ROS core*:
   bash
   roscore
   
   يجب أن تظهر رسالة تشير إلى أن ROS core يعمل بنجاح.

   
![image](https://github.com/user-attachments/assets/dc36cc6e-71f8-4b5f-bf89-34333aa0f4ac)
