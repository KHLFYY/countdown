---
title: 2022年 高考倒计时
date: 2021-10-08 22:18:39
---

<body>
  <p><div align=center><h2 class="count"></h2>
  <script>
      window.onload = function () {
          countDown();
          function addZero(i) {
              return i < 10 ? "0" + i: i + "";
          }
          function countDown() {
              var nowtime = new Date();
              var endtime = new Date("2022/06/07,00:00:00");
              var lefttime = parseInt((endtime.getTime() - nowtime.getTime()) / 1000);
              var d = parseInt(lefttime / (24*60*60))
              var h = parseInt(lefttime / (60 * 60) % 24);
              var m = parseInt(lefttime / 60 % 60);
              var s = parseInt(lefttime % 60);
              d = addZero(d)
              h = addZero(h);
              m = addZero(m);
              s = addZero(s);
              document.querySelector(".count").innerHTML = `${d}天 ${h} 时 ${m} 分 ${s} 秒`;
              if (lefttime <= 0) {
                  document.querySelector(".count").innerHTML = "2022年高考已开始";
                  return;
              }
              setTimeout(countDown, 1000);
            }
        }
    </script>
</body>

> ☆此处采用终止时间为：2022/06/07 00:00:00

---

![emmm……](https://pic.imgdb.cn/item/616056592ab3f51d913823dd.png)

---

本项目Github仓库：[https://github.com/KHLFYY/countdown/](https://github.com/KHLFYY/countdown/)
