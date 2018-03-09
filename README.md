# dlib-face-landmark-compression

Dlib中的人脸landmark检测的模型压缩

具体介绍见博客：[http://www.miaoerduo.com/c/dlib人脸关键点检测的模型分析与压缩.html]( http://www.miaoerduo.com/c/dlib人脸关键点检测的模型分析与压缩.html)

使用前，需要修改dlib的源码：
DLIB_PATH/include/dlib/image_processing/image_processing/shape_predictor.h

修改 shape_predictor 类的成员变量的属性为public。

```
git clone https://github.com/miaoerduo/dlib-face-landmark-compression.git
cd dlib-face-landmark-compression
g++ main.cpp -o main.bin -I ./ -I DLIB_PATH/include -L DLIB_PATH/lib -ldlib -std=c++11
./main.bin src_dlib_shape_predictor_model dest_model
```

为了方便大家的调试，这里上传一个dlib的68点landmark的原模型和使用main.cpp的代码压缩之后的模型。

链接: https://pan.baidu.com/s/1OnT45TUHkQnqkN2h2zCc9g 密码: 22ju

