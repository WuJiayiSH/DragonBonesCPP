# DragonBones C++ 运行时
[README in English](./README.md)
## [DragonBones 公共库](./DragonBones/)
## 强烈建议使用 [DragonBones Pro](http://www.dragonbones.com/) 制作动画。

## 使用CMakes

    add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/frameworks/DragonBonesCPP)
    target_link_libraries(${APP_NAME} DragonBonesCPP)
    target_include_directories(${APP_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/frameworks/DragonBonesCPP/DragonBones/src)
    target_include_directories(${APP_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/frameworks/DragonBonesCPP/Cocos2DX_3.x/src)

## 支持的引擎
* [Cocos2d-x](http://cocos2d-x.org/) - [如何在 Cococs2d-x 中使用 DragonBones](./Cocos2DX_3.x/)
* [SFML](https://www.sfml-dev.org/) - 已移除! 请查看https://github.com/DragonBones/DragonBonesCPP

## 了解更多
* [DragonBones 官网](http://www.dragonbones.com/)

## 在线示例
[![PerformanceTest](https://dragonbones.github.io/demo/demos.jpg)](https://github.com/DragonBones/Demos)

Copyright (c) 2012-2018 The DragonBones team and other contributors.
