# 代码说明

1. 构造Brother类表示葫芦娃（name是名字，rank是年纪排名，pos是当前位置），定义了读写信息的一些方法、set_pos方法实现被指定前往某位置、exchange方法实现与某兄弟交换位置、yell方法实现报数
2. 构造Grandpa类表示爷爷
3. main函数首先实例化了葫芦娃七兄弟，并对其初始化，并且用pos[]来记录当前的队伍；然后分别调用orchestration方法和choreography方法，这两个方法的第一步都是让葫芦娃七兄弟随机站队，实现随机的方法是让每个葫芦娃都随机挑一个兄弟交换位置，互相交换位置（Brother类的exchange方法），结束后报数
4. orchestration方法中，选择冒泡排序，用Brother的exchange实现自行交换位置，然后自行报数
5. choreography方法中，实例化了爷爷，然后调用Grandpa的grandpa_sort方法来进行排序，该方法用Brother的set_pos方法来指定葫芦娃的位置，然后调用Grandpa的start_yell方法让葫芦娃开始报数