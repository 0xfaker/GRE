# auto-green

[![Build Status](https://github.com/justjavac/auto-green/workflows/ci/badge.svg?branch=master)](https://github.com/justjavac/auto-green/actions)

自动保持 GitHub 提交状态常绿。

> a commit a day keeps your girlfriend away.

## 原理

使用 GitHub Actions 的定时任务功能，每隔一段时间自动执行 `git commit`，提交信息为 "a commit a day keeps your girlfriend away"，灵感来自知乎问题[在 GitHub 上保持 365 天全绿是怎样一种体验？](https://www.zhihu.com/question/34043434/answer/57826281)下某匿名用户的回答：

> 曾经保持了 200 多天全绿，但是冷落了女朋友，一直绿到现在。

有关 Github Action 的原理，可查看官方文档 [Github Action 简介](https://docs.github.com/cn/actions/learn-github-actions/introduction-to-github-actions)

## 使用

- 点右上角 **Use this template** 按钮复制本 GitHub 仓库，**:warning: 千万不要 Fork，因为 fork 项目的动态并不会让你变绿 :warning:**
- 修改 [ci.yml 文件的第 7、8 行](https://github.com/justjavac/auto-green/blob/master/.github/workflows/ci.yml#L7-L8) 去掉前面的 `#` 号
- 修改 [ci.yml 文件的第 23 行](https://github.com/justjavac/auto-green/blob/master/.github/workflows/ci.yml#L23) 为自己的 GitHub 邮箱账号
- (可选) 你可以通过修改 [ci.yml 文件的第 8 行](https://github.com/justjavac/auto-green/blob/master/.github/workflows/ci.yml#L8)来调整频率

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

**注**：由于 GitHub Actions 的限制，如果设置为 `* * * * *` 实际的执行频率为每 5 分执行一次。

## License

[auto-green](https://github.com/justjavac/auto-green) is released under the MIT License. See the bundled [LICENSE](./LICENSE) file for details.
Update timestamp: Mon Sep 16 01:39:28 UTC 2024
Update timestamp: Thu Sep 19 01:35:36 UTC 2024
Update timestamp: Sun Sep 22 01:42:54 UTC 2024
Update timestamp: Wed Sep 25 01:39:19 UTC 2024
Update timestamp: Fri Oct  4 01:38:27 UTC 2024
Update timestamp: Thu Oct 10 01:37:55 UTC 2024
Update timestamp: Sat Oct 19 01:37:07 UTC 2024
Update timestamp: Tue Oct 22 01:39:35 UTC 2024
Update timestamp: Thu Oct 31 01:40:38 UTC 2024
Update timestamp: Fri Nov  1 01:46:05 UTC 2024
Update timestamp: Mon Nov  4 01:41:07 UTC 2024
Update timestamp: Sun Nov 10 01:41:43 UTC 2024
Update timestamp: Tue Nov 19 01:43:47 UTC 2024
Update timestamp: Fri Nov 22 01:43:42 UTC 2024
Update timestamp: Mon Nov 25 01:45:40 UTC 2024
Update timestamp: Sun Dec  1 02:00:32 UTC 2024
Update timestamp: Wed Dec  4 01:47:45 UTC 2024
Update timestamp: Sat Dec  7 01:45:33 UTC 2024
Update timestamp: Fri Dec 13 01:48:38 UTC 2024
Update timestamp: Mon Dec 16 01:50:54 UTC 2024
Update timestamp: Thu Dec 19 01:44:25 UTC 2024
Update timestamp: Wed Dec 25 01:37:20 UTC 2024
Update timestamp: Tue Dec 31 01:38:06 UTC 2024
Update timestamp: Wed Jan  1 01:45:51 UTC 2025
Update timestamp: Sat Jan  4 01:36:37 UTC 2025
Update timestamp: Tue Jan  7 01:39:43 UTC 2025
Update timestamp: Sat Jan 25 01:25:09 UTC 2025
Update timestamp: Fri Jan 31 01:36:38 UTC 2025
Update timestamp: Sat Feb  1 01:40:59 UTC 2025
Update timestamp: Tue Feb  4 01:36:44 UTC 2025
Update timestamp: Fri Feb  7 01:38:20 UTC 2025
Update timestamp: Mon Feb 10 01:39:19 UTC 2025
Update timestamp: Thu Feb 13 01:38:45 UTC 2025
Update timestamp: Sun Feb 16 01:44:48 UTC 2025
Update timestamp: Wed Feb 19 01:38:49 UTC 2025
Update timestamp: Sat Feb 22 01:36:12 UTC 2025
Update timestamp: Tue Feb 25 01:41:17 UTC 2025
Update timestamp: Fri Feb 28 01:41:29 UTC 2025
Update timestamp: Tue Mar  4 01:42:52 UTC 2025
Update timestamp: Fri Mar  7 01:43:33 UTC 2025
Update timestamp: Tue Mar 25 01:46:16 UTC 2025
Update timestamp: Fri Mar 28 01:45:37 UTC 2025
Update timestamp: Mon Mar 31 01:51:31 UTC 2025
Update timestamp: Thu Apr 10 01:47:04 UTC 2025
Update timestamp: Wed Apr 16 01:49:54 UTC 2025
Update timestamp: Fri Apr 25 01:50:36 UTC 2025
Update timestamp: Wed May  7 01:52:58 UTC 2025
Update timestamp: Sat May 10 01:48:10 UTC 2025
Update timestamp: Tue May 13 01:54:10 UTC 2025
Update timestamp: Mon May 19 01:58:58 UTC 2025
Update timestamp: Sun May 25 02:02:52 UTC 2025
Update timestamp: Wed Jun  4 01:56:43 UTC 2025
Update timestamp: Tue Jun 10 01:58:31 UTC 2025
Update timestamp: Fri Jun 13 01:57:25 UTC 2025
Update timestamp: Thu Jun 19 01:57:57 UTC 2025
Update timestamp: Tue Jul  1 02:09:41 UTC 2025
Update timestamp: Sun Jul 13 02:18:19 UTC 2025
Update timestamp: Sat Jul 19 02:00:25 UTC 2025
Update timestamp: Tue Jul 22 02:05:33 UTC 2025
Update timestamp: Fri Jul 25 02:05:15 UTC 2025
