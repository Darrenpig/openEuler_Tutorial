# Nearlink EB25 SIG
#### **项目现状**  
- **初步维护状态**：项目整体分为三大部分：  
  1. **造车**：使用520编码电机作为动力模块。  
  2. **通讯模块**：基于EB25实现设备间通信。  
  3. **供电电源**：采用12V电池盒+稳压模块+5W×8太阳能板组合供电。  

---

#### **项目成员分工**  
- **@和尚**：负责ROS开发板配置、PWM控制及电机驱动封装。  
- **@徐逸凡**：负责硬件采购（如底板、喷涂材料）、底盘组装与调试。  
- **@徐欣晨**：负责文档维护、Matlab公式验证及竞赛交流。  
- **@DarrenPig**：仓库维护、环境搭建、进度推动及SDK编译烧录。  

---

#### **协作文档区**  
- **核心文档**：飞书知识库（[使用手册](https://lierda.feishu.cn/wiki/VBoPwV3oRiJRjWkb1ZkcgVMynmg )、[网址汇总](https://lierda.feishu.cn/wiki/X360wInOjihWzukypNzc0Df5nHf )）。  
- **ROS开发板资源**：Yahboom ROS驱动板[教程链接](https://www.yahboom.com/study/ROS-Driver-Board )。  

---

#### **项目目标与架构**  
- **核心目标**：在openEuler和RT-Thread上混合编译Nearlink接口，实现即插即用的Nearlink硬件支持。  
- **仓库管理**：  
  - 主仓库：[openeuler-nearlink](https://gitee.com/darrenpig/openeuler-nearlink )，通过更新Readme共享进度与文件。  
  - **Gitee功能**：支持代码托管、进度跟踪、PR提交及自动化构建检测（参考openEuler社区流程）。  

---

#### **关键进展与里程碑**  
- **2025年2月5日**：  
  - **@DarrenPig**需启动imx8的SDK编译烧录；**@徐逸凡**进行材料喷涂。  
- **历史进度**：  
  - 4.28：12V电池到位，ROS拓展板用于电机驱动。  
  - 5.4：建模完成，容器环境就绪。  

---

#### **技术实现与工具链**  
- **本地环境搭建**：  
  - 基于openEuler的容器化部署（参考[微信文章](https://mp.weixin.qq.com/s/rg3NYJRQcsNliDUJerOzuw )）。  
- **硬件选型**：  
  - 国信长天Cortex-M4开发板、太阳能供电系统。  

---

#### **开源协作流程**  
1. **代码提交**：通过Gitee仓库克隆、修改、提交PR，遵循openEuler社区的SIG（Special Interest Group）模式。  
2. **自动化构建**：提交代码后触发CI/CD流水线，自动编译检测（参考src-openeuler项目流程）。  
3. **文档维护**：Markdown文件渲染至社区官网，提升可读性（如飞书文档与Gitee联动）。  

---

#### **后续计划**  
- **硬件整合**：完成底盘固定与电机驱动函数封装。  
- **软件适配**：验证Nearlink接口在RT-Thread的兼容性。  
- **社区贡献**：将项目成果提交至openEuler第三方仓库（如src-oepkgs）。  

--- 

**注**：项目依赖Gitee的协作功能（如Issue跟踪、PR审核）及openEuler的自动化工具链。

## 项目现状
**初步维护状态**  
仓库基于[木兰宽松许可证第2版](http://license.coscl.org.cn/MulanPSL2)进行开源管理，当前处于基础功能开发阶段。

## 项目整体思路
### 1. 造车
- **核心驱动**  
  采用520编码电机作为动力源，实现精准控制与高效能输出

### 2. 通讯模块
- **关键组件**  
  EB25模块承担无线通信功能，确保设备间稳定数据传输

### 3. 供电系统
- **复合能源方案**  
  12V电池盒+稳压模块组成基础电源，搭配5W*8太阳能板实现可持续供电

## 项目成员分工
| 成员        | 职责领域             |
|-------------|----------------------|
| @和尚       | ROS系统开发/PWM控制  | 
| @徐逸凡     | 硬件设计与集成       |
| @徐欣晨     | 文档维护与版本管理   |

---



---
<table>
    <tr>
      <td ><img src="image/ROS%E5%B9%B3%E5%8F%B0.png" width=200/>
      <td ><img src="image/Tree.png" width=200/>
      <td ><img src="image/%E5%AE%98%E6%96%B9%E7%9A%84%E8%B5%84%E6%96%99%E5%8C%85%E6%88%AA%E5%9B%BE.png" width=200/>
      <td ><img src="image/FAQ%E6%88%AA%E5%9B%BE.png" width=200/>
    </tr>

   <tr>  
      <td ><img src="image/%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95.png" width=200/>
      <td ><img src="image/Nearlink.png" width=200/>
      <td ><img src="image/SegonUIScript%20%20aim.png" width=200/>
      <td ><img src="image/duibitu.png" width=200/>
   
    </tr>
</table>

# https://lierda.feishu.cn/wiki/VBoPwV3oRiJRjWkb1ZkcgVMynmg
### 以下是大家可以轻松编辑交流的文档区：（提交方法在Readme结尾~~~）

 @和尚 【ROS开发板】https://www.yahboom.com/study/ROS-Driver-Board


#### 介绍

常工院的一个[Nearlink](https://www.hisilicon.com/cn/techtalk/nearlink)兴趣小组，想在openEuler\Rt-Thread上混合编译Nearlink接口，达到有即插即用的Nearlink硬件目的


## 我们的主要利用[这个仓库](https://gitee.com/darrenpig/openeuler-nearlink)的方式：更新readme


#### 项目结构说明
我们能用Gitee做啥子？
共享文件、项目进度



#### 资料共享

##### 1.使用手册：https://lierda.feishu.cn/wiki/VBoPwV3oRiJRjWkb1ZkcgVMynmg


##### 2.网址：https://lierda.feishu.cn/wiki/X360wInOjihWzukypNzc0Df5nHf?utm_source=pocket_saves


#### 项目成员： @DarrenPig 、 @徐逸凡 、 @徐欣晨 ， @和尚 

### 个人进度

####  @DarrenPig 
3.24 建立[仓库](https://gitee.com/darrenpig/openeuler-nearlink)，维护Readme
3.25 队友组织，相关文档的推送。
4.17 我的本地环境https://mp.weixin.qq.com/s/rg3NYJRQcsNliDUJerOzuw这个方式装的
5.22 拉起容器


####  @徐逸凡 @徐欣晨 
3.25 拿板子 
3.24 预组会讨论
4.22 准备硬件
4.28 小车底盘到位，准备上电

---
## 维护记录：
#### 3.24 @DarrenPig 建仓Readme，传文档
## 项目进度：
#### 2.24 图书馆二楼
#### 4.17 @ DarrenPig 更新Readme,跟进进度
#### 4.18 @ DarrenPig 更新Readme,推动项目进度（底盘分工组会）、（步进电机）支架购买
#### 4.20 @ DarrenPig 图书馆二楼，检查电机，调整开发板环境； @ 徐逸凡 底板购买、喷涂购买
#### 4.21 @ 和尚 板子上电成功
#### 4.22 @ 和尚 换板子 国信长天Cortex-M4、@ 徐欣晨 Matlab 公式、竞赛交流
#### 4.28 @ 和尚 12V电池已到、ROS拓展板直接做电机驱动，记得封装好函数  @徐逸凡 @徐欣晨 底盘已到记得即使搞定固定与喷涂 
#### 5.2  @ DarrenPig 今天必须开始 imx 8 的SDK编译烧录了， @徐逸凡  有材料可以先涂
#### 5.4  @ DarrenPig 建模完成
---
###### @所有人 修改Readme方法：
>>> ![修改方式](image/%E7%99%BE%E5%BA%A6%E7%BD%91%E7%9B%98%E5%8A%A0%E9%80%9F.gif)

## 开源协议说明
根据[木兰宽松许可证第2版](http://license.coscl.org.cn/MulanPSL2)：
- 🛠️ **自由使用**：允许复制/修改/分发代码  
- ⚖️ **专利授权**：贡献者提供不可撤销的全球专利许可  
- ⚠️ **免责条款**：不承担使用导致的间接损失  
- 📜 **合规要求**：分发时必须包含完整许可证副本

> *注：所有贡献者需确保代码提交符合Mulan PSL v2规范*
