---
trigger: model_decision
description: 进行嵌入式代码开发的时候需要引入此规则
---

# 嵌入式MCU开发规则

## 1. 语言与编码标准
- 使用纯C99标准
- 禁止使用goto和continue语句
- 符合MISRA C 2012规范
- 禁止动态内存分配和递归调用

## 2. 命名规范
- 寄存器宏：XXX_REG_ADDR、XXX_BIT_MASK、XXX_BIT_POS
- 枚举类型：xxx_reg_t、xxx_state_t（小写下划线）
- 函数命名：xxx_init()、xxx_read()、xxx_write()
- 注释格式：Doxygen风格

## 3. 代码格式
- 缩进4个空格
- 每行不超过80字符
- 禁止魔法数，全部使用宏定义

## 4. 错误处理
- 必须进行参数校验
- 实现超时判断机制
- 提供明确的错误返回值

## 5. 项目架构
- 应用层(APP) -> 组件层(CDD) -> 驱动层(DRV) -> 实时驱动(RTD) -> 硬件(HW)
- 目录结构清晰，模块划分明确
trigger: model_decision
description: 进行嵌入式代码开发的时候需要引入此规则
---