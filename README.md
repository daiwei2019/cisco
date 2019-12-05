grep -E "((25[0-5]|2[0-4][0-9]|[0-1]?[0-9][0-9]?)\.){3}(25[0-5]|2[0-4][0-9]|[0-1]?[0-9][0-9]?)" //查询IPv4地址明细
awk -v count=0 '{if ($2 ~/(([0-9]+)\.){3}[0-9]+/) {counnt++}} {print "IP地址总数："couunt}' //查询IPv4地址总
awk -v count1=0,count2=0 '{if ($5 ~/^u/) {count1++} if ($5 ~/^a/) {count2++}}{print "UP接口数量：\t"count1 "\nDown接口数量：\t"count2}' //统计up、down接口数量
