Python scripts for Stock and Funds in 蚂蚁财富 

读取蚂蚁财富(Ant Fortune)的基金定投记录，并同步到随手记(sui.com)的转账记录和雪球(xueqiu.com/performance)的投资记录中。

随手记是金蝶开发的一个家庭账本工具，到2018年本人使用这个工具已经有六年了。另外，也在使用雪球记录投资股票和基金的操作记录。
去年开始做基金定投，大概投资了10支基金，选择的是每周四定投，所以每周四需要在随手记和雪球里各自记录十条数据，其中雪球里记录的时候还要手动输入净值、份额、手续费，且蚂蚁也不提供导出功能，需要一边在手机上看投资记录，一边手动抄写到雪球的界面里，相当繁琐。

是可忍孰不可忍，写了如下脚本：

XueqiuUtils.py：一些模拟post时用到的headers,cookie信息，理想状态是代码自己模拟登录并获取sessionId，后续再做。目前需要过一段时间自己更新一下，不过作为我自己基本每天都要登录的情况，这个sessionId是长期不变的，手工修改就可以了。

AntFundSui.py：读取支付宝导出的记录，并写入到随手记中。

AntFundXueqiu.py：读取支付宝导出的记录，并到新浪股票中查询当日基金净值，然后自行计算并填写投资记录。
