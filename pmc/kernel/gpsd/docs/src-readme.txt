这个程序支持NEMA协议
NEMA的Sentence有多种，这里使用GPRMC来获取时间，如果你们用的设备不同，修改GetRefDiff这个函数即可。
原来的程序本来还可以调整时钟的快慢（模仿NTP），后来因为串口本身没有实时性，这个功能没有意义，被禁止，
但源程序没有删除，所以看上去有点复杂。其实程序的功能很简单，每秒收到一个对时数据包，和本地时间比较，
如果不同就调整本地时间，只能达到秒级的精度。