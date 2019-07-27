# VulkanTutorialCN
Vulkan中文教程v0.9

原文地址：https://vulkan-tutorial.com/

译文PDF地址：https://github.com/fangcun010/VulkanTutorialCN/blob/master/Vulkan%E7%BC%96%E7%A8%8B%E6%8C%87%E5%8D%97.pdf

由于本人才疏学浅，翻译难免有误，望各位不吝惜指正。

从OpenGL升级到Vulkan可以引用一个形象的比喻：API这个中间商从以往的小超市摇身一变成为“某东”，造就价低量又足。（没有中间商，自己赚差价）

Vulkan是Khronos Group(OpenGL标准的维护组织)开发的一个新API，它提供了对现代显卡的一个更好的抽象，与OpenGL和Direct3D等现有api相比，Vulkan可以更详细的向显卡描述你的应用程序打算做什么，从而可以获得更好的性能和更小的驱动开销。Vulkan的设计理念与Direct3D 12和Metal基本类似，但Vulkan作为OpenGL的替代者，它设计之初就是为了跨平台实现的，可以同时在Windows、Linux和Android开发。甚至在Mac OS系统上，Khronos也提供了Vulkan的SDK，虽然这个SDK底层其实是使用MoltenVK实现的。

MoltenVK实际上是一个将Vulkan API映射到Metal API的一个框架，Vulkan这里只是相当于一个抽象层。
然而，为了得到一个更好的性能，Vulkan引入了一个非常冗余的API。相比于OpenGL驱动帮我们做了大量的工作，Vulkan与图像api相关的每一个细节，都需要从头设置，包括初始帧缓冲区的创建与缓冲、纹理内存的管理等等。因此，哪怕只画一个三角形，我们都要写数倍于OpenGL的代码。

而Google在Android 7.0后提供了对Vulkan的支持，并且提供了一系列工具链与Validation Layers（后面会进行说明）。在Android Studio中，只要将Shader代码放在src/main/shaders文件夹下面，项目编译时会自动被编译成.spv字节码，可以作为assets使用。
由于Vulkan的使用非常冗长，

