# 指令
这里列出了机器人支持的所有指令。

手册正在完善，这里可能没有列出所有支持的命令。开发阶段，命令可能遭遇破坏性更改。

[[toc]]

::: tip 解释
<br />
 带有 <Badge text="仅管理员" type="warning"/> 的指令表示只有机器人管理员执行此指令才会生效。

**机器人管理员并非群管理员。** 管理员列表保存在 `admins.list` 中；而被封禁用户列表保存在 `blockusers.list` 中。
:::
::: tip 提示
下文使用以下格式编写  
`<command> <args>` *description*
:::

---
## &test
- **`&test`** 存活测试

## &manual
- **`&manual`** 引导用户在用户手册中找到问题答案

## &faq
- **`&faq`** 引导用户看常见问题解答

## &ot
- **`&ot`** 提示用户正在水群，并将其引导至咖啡馆

## &csl 
- **`&csl <player_name>`** 获取 `<player_name>` 的角色信息，同时返回材质预览
- 对角色名回复 **`$csl`** 使用被回复的消息中的文本作为角色名进行查询，同时返回材质预览
- **`&csl.log`** 引导用户上传 CustomSkinLoader 日志至 <https://pastebin.aosc.io/>
- **`&csl.config`** 引导用户手动修改 CustomSkinLoader 的配置文件

::: tip 申必功能
当用户在群内发出 CustomSkinLoader 的日志在 <https://pastebin.aosc.io/> 的链接后，机器人将自动解析日志，提取关键信息并提供问题报告。

需要注意的是，由于没有使用 `aiohttp` 这个异步库，解析日志时将会阻塞其他指令运行 ~~（便秘）~~
:::

## &ygg
- **`&ygg <player_name>`**  获取 `<player_name>` 的角色信息（含 UUID），同时返回 `provider` 为 LittleSkin 的材质预览
- 对角色名回复 **`$ygg`** 使用被回复的消息中的文本作为角色名进行查询，同时返回 `provider` 为 LittleSkin 的材质预览
- **`&ygg.nsis`**  *No Skin in Server*，提示用户需正确配置服务端

## &view
- **`&view <texture_hash>`**  获取材质预览，`<texture_hash>` 应为长度为 64 位的哈希值

## &browser
- **`&browser`** 引导用户更换浏览器

## &ygg.server.jvm
- **`&ygg.server.jvm`** 引导用户添加参数并将产生的日志上传至群

## &domain
- **`&domain`** 引导用户更换域名访问 LittleSkin 主站

## &ban
- **`&ban add <@somebody>`** <Badge text="仅管理员" type="warning"/>  
    封禁 *被 @ 者*，被封禁的用户将不能操作机器人。执行者必须有管理员权限，管理员不能被封禁
- **`&ban remove <@somebody>`** <Badge text="仅管理员" type="warning"/>  
    解封 *被 @ 者*，被解封的用户现在可以操作机器人。执行者必须有管理员权限

## &help
- **`&help`** 指令帮助，引导用户查看此页面
