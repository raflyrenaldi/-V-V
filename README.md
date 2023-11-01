# -V-V
这是关于arc协议的一个代码
from apscheduler.schedulers.blocking import BlockingScheduler    # 引入模块


def task():
    '''定时任务'''
    os.system('python3 spider.py')


if __name__ == '__main__':
    scheduler = BlockingScheduler()

    # 添加任务
    scheduler.add_job(task, 'cron', hour=11, minute=30)

    scheduler.start()

作者：潘高
链接：https://juejin.cn/post/6844903823941730311
来源：稀土掘金
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
