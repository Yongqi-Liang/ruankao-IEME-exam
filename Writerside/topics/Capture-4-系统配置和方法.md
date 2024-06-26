# Capture 4:系统配置和方法

*根据考情分析，本章节知识仅在2013年考察过1题(占1分)*

## 系统配置技术
- 系统架构
- 系统配置方法（双机互备、双机热备、群集服务、容错服务器）
- 系统处理模式（集中式及分布式计算、批处理及实时处理、Web计算及云计算）
- 系统事务管理
事务4特性：原子性、一致性、隔离性、持续性
事务的并发控制：封锁、排他锁、共享锁

## 系统架构
- C/S结构
- B/S结构
客户端(浏览器)/应用服务器/数据库
- 多层分布式结构
瘦客户/业务服务/数据服务

## 可靠性、可维护性、可用性
### 可靠性度量
平均无故障时间(Mean Time To Failure)
平均失效间隔(Mean Time Between Failure)
### 可维护性度量
平均维修时间(Mean Time To Repair)
### 可用性
MTTF / ( MTTF + MTTR ) * 100%
### 可靠性(reliability) 可用性(availability) 区别

## 提高可靠性的方法
#### 提高元器件的质量
#### 发展容错技术
使用空闲备件、负载平衡、镜像、复现/延迟镜像、热可更换

> Q:任何信息系统都不可能避免天灾人祸，当事故发生时，要可以跟踪事故源、
> 收集证据、恢复系统、保护数据。通常来说高可用性的系统具有较强的容错能力，
> 使得系统在排除了某些类型的保障后继续正常运行。
> 请将正确的**容错途径**对应关系进行连线
> 
> A:直接展示对应答案
> 
> | 容错途径   | 说明                             |
> |--------|--------------------------------|
> | 使用空闲套件 | 配置一个备用部件，当原部件出现错误取代原部件的功能      |
> | 负载平衡   | 两个部件共同承担一项任务，一个出现故障，另外一个承担全部任务 |
> | 镜像     | 两个部件执行完全相同的工作，当一个出现故障时另外一个继续工作 |
> | 复现     | 原系统出现故障，辅助系统接替原系统的工作           |
> | 热可交换   | 某一部件出现故障，可以立即拆除该部件换上一个好的部件     |

## 串联、并联、混联系统
串联：R = R1 * R2 * ... * Rn
并联：R = 1 - (1 - R1) * (1 - R2) * ... * (1 - Rn)
混联系统：R * (1 - (1 - R)^3) * (1 - (1 - R)^2)

