# PlaneFly

[Flutter Matrix4矩阵 + 动画实现移动、缩放、旋转，让纸飞机沿着贝塞尔曲线轨迹飞起来](https://juejin.cn/post/6924591088040673294)

![image](./gif/Plane%20Fly.gif)

import 'package:flutter/material.dart';

/**
 * Transform矩阵转换示例
 */
void main(){
  runApp(new MaterialApp(
    title: 'Transform矩阵转换示例',
    home: new MyApp(),
  ));
}

class MyApp extends StatelessWidget{
  @override
  Widget build(BuildContext context) {
    // TODO: implement build
    return new Scaffold(
      appBar: AppBar(
        title: new Text('Transform矩阵转换示例'),
      ),
      body: new Center(
        child: Container(
          color: Colors.grey,
          child: Transform(
            alignment: Alignment.topRight,
            transform: Matrix4.rotationZ(0.3),
            child: Container(
              padding: const EdgeInsets.all(8.0),
              color: const Color(0xFFE8581C),
              child: const Text('Transform矩阵转换'),
            ),
          ),
        ),
      ),
    );
  }
}
