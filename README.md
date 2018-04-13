### wx.d.ts

typescript definition file for [weixin app](https://mp.weixin.qq.com/debug/wxadoc/dev/api/?t=1475052052547)

[下载wx.d.ts文件(右键另存为)](https://raw.githubusercontent.com/zxj5470/wx.d.ts/master/wx.d.ts)

## build

```bash
npm run build
```

## simple usage
copy wx.d.ts to your typing directory.


## update APIs every day
```bash
# first time
git clone https://github.com/zxj5470/wx.d.ts
cd wx.d.ts
```

```bash
$ cat everyday.sh
#!/bin/bash
npm run build
git add wx.d.ts
git commit -m "`date`"
git push
```

```bash
chmod u+x everyday.sh
```

```bash
$ crontab -e
# run at 6:00 AM EDT(UTC-4) (18:00 UTC+8) every day.
0 6 * * * ~/wx.d.ts/everyday.sh
```