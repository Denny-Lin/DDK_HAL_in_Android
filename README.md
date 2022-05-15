# DDK_HAL_in_Android
A HAL defines a standard interface for hardware vendors to implement, which enables Android to be agnostic about lower-level driver implementations. &nbsp;

# From top to bottom
### Java Architecture
![Screen Shot 2022-04-24 at 6 09 08 AM](https://user-images.githubusercontent.com/67073582/164948344-eafad4b1-7b17-4c5e-978d-4e5d2423e5ba.png)

### C++ Architecture
![Screen Shot 2022-04-24 at 6 10 31 AM](https://user-images.githubusercontent.com/67073582/164948346-442bcf32-cb6e-49bc-808e-a03fe93aebcd.png)

# What is HAL?
https://source.android.google.cn/devices/architecture &nbsp;

# Why do we need HAL in Android?
Protect the source code of the vendor from open source licenses.<br/>

https://www.youtube.com/watch?v=gFOXM-CY8mQ &nbsp;

# Where can we find HAL?
https://android.googlesource.com/platform/hardware <br/>

### HAL Legacy
./hardware/libhardware_legacy/ &nbsp;

### HAL Stub
./hardware/libhardware/ &nbsp;

### HIDL 
./hardware/interfaces/ &nbsp;

### AIDL 
./hardware/interfaces/ &nbsp;

# HIDL for HALs
Because of Treble, use HIDL to define the interface(API) between system.img and vendor.img. <br/>

![image](https://user-images.githubusercontent.com/67073582/166171372-a8e305fc-1fae-49c6-8f55-a609f19689eb.png) <br/>

http://www.max-shu.com/blog/?p=1075 <br/>
https://www.796t.com/content/1544773146.html <br/>
https://ithelp.ithome.com.tw/articles/10221507 </br>
https://zhuanlan.zhihu.com/p/441227958 &nbsp;

## Steps
mkdir -p hardware/interfaces/DDK/1.0/default <br/>
Code the IDDK.hidl <br/>
Use update-makefiles.sh to generate Android.bp <br/>
Use hidl-gen .c and .h<br/>


# AIDL for HALs
https://source.android.google.cn/devices/architecture/aidl/aidl-hals <br/>
https://www.youtube.com/watch?v=M6extgmQQNw <br/>

![Screen Shot 2022-05-01 at 10 30 27 AM](https://user-images.githubusercontent.com/67073582/166129645-616ed552-120a-4142-8370-6dc03e52b78a.png) &nbsp;

# VNDK
https://www.cnblogs.com/blogs-of-lxl/p/11232754.html &nbsp;

# References
https://www.youtube.com/watch?v=UFaWqdxBW4E &nbsp;
