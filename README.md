# auto-green

[![Build Status](https://github.com/ShuangRen/auto-green/workflows/ci/badge.svg?branch=master)](https://github.com/ShuangRen/auto-green/actions)

自动保持 GitHub 提交状态常绿。

> a commit every day, keep your girlfriend far away.

## 使用

- [新建](https://github.com/new) GitHub 仓库
- 复制 `.github/workflows/ci.yml` 和 `keepchange.txt` 文件到你的仓库
- 修改 `email`、`name` 和 `url`，在 [ci.yml 文件的第 19-21 行](https://github.com/ShuangRen/auto-green/blob/master/.github/workflows/ci.yml#L19-L21)
- (可选) 你可以通过修改 [ci.yml 文件的第 8 行](https://github.com/ShuangRen/auto-green/blob/master/.github/workflows/ci.yml#L8)来调整频率

计划任务语法有 5 个字段，中间用空格分隔，每个字段代表一个时间单位。

```plain
┌───────────── 分钟 (0 - 59)
│ ┌───────────── 小时 (0 - 23)
│ │ ┌───────────── 日 (1 - 31)
│ │ │ ┌───────────── 月 (1 - 12 或 JAN-DEC)
│ │ │ │ ┌───────────── 星期 (0 - 6 或 SUN-SAT)
│ │ │ │ │                                   
│ │ │ │ │
│ │ │ │ │
* * * * *
```

每个时间字段的含义：

|符号   | 描述        | 举例                                        |
| ----- | -----------| -------------------------------------------|
| `*`   | 任意值      | `* * * * *` 每天每小时每分钟                  |
| `,`   | 值分隔符    | `1,3,4,7 * * * *` 每小时的 1 3 4 7 分钟       |
| `-`   | 范围       | `1-6 * * * *` 每小时的 1-6 分钟               |
| `/`   | 每         | `*/15 * * * *` 每隔 15 分钟                  |

## License

[auto-green](https://github.com/ShuangRen/auto-green) is released under the MIT License. See the bundled [LICENSE](./LICENSE) file for details.

<img align="right" src="https://github-readme-stats.vercel.app/api?username=yourname&show_icons=true&icon_color=805AD5&text_color=718096&bg_color=ffffff&hide_title=true" />

#### Hello 👏
> I'm YourName  
> java coder💻   
> football player⚽️
