# Git Commit Message

> Git 提交规范

- [Git 指令](./docs/git-command.md)
- [清理Github仓库中敏感信息](./docs/clean_sensitive_file.md)

## Git commit

Commit message 包括三个部分：Header，Body 和 Footer。

```text
<type>(<scope>): <subject>
// <BLANK LINE>
<body>
// <BLANK LINE>
<footer>
```

> Header 是必需的，Body 和 Footer 可以省略。
> Header 部分只有一行，包括三个字段：type（必需）、scope（可选）和subject（必需）。

```text
<type>(<scope>): <subject>
  │       │             │
  │       │             └─⫸ 主要描述，尽量简短
  │       │
  │       └─⫸ Commit Scope(可选): common | 业务模块[挂号 就诊人 用户子系统] 等等
  │
  └─⫸ Commit Type: build|ci|docs|feat|fix|perf|refactor|test
```

> git commit - m 'feat(common): util 中加入节流函数'  
> `-m` 参数 : 指定 commit message

### type

|字符|文案|备注|颜色|颜色文案|
|:---:|:---|:---|:---:|:---:|
|`feat`|功能|增加新的业务功能|#4CAF50|明亮绿色|
|`fix`|修复|修复业务问题/BUG|#2196F3|蓝色|
|`perf`|性能|优化性能|#FFEB3B|黄色|
|`style`|样式|改代码风格, 不影响运行结果|#5c879d|暗蓝色|
|`refactor`|重构|重构代码|#A52A2A|棕色|
|`revert`|撤销|撤消更改|#E91E63|粉色|
|`test`|测试|测试相关，不涉及业务代码的修改|#00BCD4|浅蓝色|
|`docs`|文档注释|文档和注释|#9C27B0|紫色|
|`chore`|琐事|依赖项/修改脚手架配置等|#424242|深灰色|
|`workflow`|工作流|工作流程改进|#8BC34A|浅绿色|
|`ci`|持续集成|持续集成相关|#F44336|浅红色|
|`wip`|开发中|开发中|#9E9E9E|灰色|
|`types`|类型定义|类型定义|#CE93D8|浅紫色|
|`release`|发布|发布版本|#2ECC71|鲜艳绿色|

### scope

可选: 没有统一的约定，一般提交时填写涉及的范围即可（公共模块 | 业务模块 ）

### subject

是 commit 目的的简短描述，不超过50个字符。

```md
- 以动词开头，使用第一人称现在时，比如change，而不是changed或changes
- 第一个字母小写
- 结尾不加句号（.）
```

### body

是对本次 commit 的详细描述，可以分成多行。

### footer

- 不兼容变动: `BREAKING CHANGE: something.`
- 关闭 Issue: `Closes #100, #101, #102`

## Git emoji

> git commit -m ":tada: initialize Repo"

|               emoji                |           emoji 代码            |    commit 说明    |
| ---------------------------------- | ----------------------------- | --------------- |
|            :tada: (庆祝)             |           `:tada:`            |      初次提交       |
|             :new: (全新)             |            `:new:`            |      引入新功能      |
|          :bookmark: (书签)           |         `:bookmark:`          |     发行/版本标签     |
|            :bug: (bug)             |            `:bug:`            |     修复 bug      |
|         :ambulance: (急救车)          |         `:ambulance:`         |      重要补丁       |
|    :globe_with_meridians: (地球)     |   `:globe_with_meridians:`    |     国际化与本地化     |
|          :lipstick: (口红)           |         `:lipstick:`          |   更新 UI 和样式文件   |
|          :clapper: (场记板)           |          `:clapper:`          |     更新演示/示例     |
|       :rotating_light: (警车灯)       |      `:rotating_light:`       |  移除 linter 警告   |
|           :wrench: (扳手)            |          `:wrench:`           |     修改配置文件      |
|       :heavy_plus_sign: (加号)       |      `:heavy_plus_sign:`      |     增加一个依赖      |
|      :heavy_minus_sign: (减号)       |     `:heavy_minus_sign:`      |     减少一个依赖      |
|         :arrow_up: (上升箭头)          |         `:arrow_up:`          |      升级依赖       |
|        :arrow_down: (下降箭头)         |        `:arrow_down:`         |      降级依赖       |
|   :zap: (闪电)<br>:racehorse: (赛马)   |   `:zap:`<br>`:racehorse:`    |      提升性能       |
| :chart_with_upwards_trend: (上升趋势图) | `:chart_with_upwards_trend:`  |    添加分析或跟踪代码    |
|           :rocket: (火箭)            |          `:rocket:`           |      部署功能       |
|     :white_check_mark: (白色复选框)     |     `:white_check_mark:`      |      增加测试       |
|     :memo: (备忘录)<br>:book: (书)     |     `:memo:`<br>`:book:`      |      撰写文档       |
|           :hammer: (锤子)            |          `:hammer:`           |      重大重构       |
|            :art: (调色板)             |            `:art:`            |   改进代码结构/代码格式   |
|            :fire: (火焰)             |           `:fire:`            |     移除代码或文件     |
|           :pencil2: (铅笔)           |          `:pencil2:`          |     修复 typo     |
|        :construction: (施工)         |       `:construction:`        |      工作进行中      |
|        :wastebasket: (垃圾桶)         |        `:wastebasket:`        |      废弃或删除      |
|         :wheelchair: (轮椅)          |        `:wheelchair:`         |      可访问性       |
|     :construction_worker: (工人)     |    `:construction_worker:`    |   添加 CI 构建系统    |
|         :green_heart: (绿心)         |        `:green_heart:`        |   修复 CI 构建问题    |
|             :lock: (锁)             |           `:lock:`            |     修复安全问题      |
|            :whale: (鲸鱼)            |           `:whale:`           |   Docker 相关工作   |
|            :apple: (苹果)            |           `:apple:`           |  修复 macOS 下的问题  |
|           :penguin: (企鹅)           |          `:penguin:`          |  修复 Linux 下的问题  |
|       :checkered_flag: (旗帜)        |      `:checkered_flag:`       | 修复 Windows 下的问题 |
| :twisted_rightwards_arrows: (交叉箭头) | `:twisted_rightwards_arrows:` |      分支合并       |