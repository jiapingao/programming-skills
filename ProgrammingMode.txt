问题：优雅的优化掉多余的if/else
① 提前return
② 策略模式：多态、枚举
③ 学会用Optional（jdk8）
④ 数组小技巧：一种编程模式：表驱动法
    一般实现：
    int getDays(int month) {
        if(month == 1) return 31;
        if(month == 5) return 31;
        if(month == 7) return 31;
        if(month == 8) return 31;
        if(month == 10) return 31;
    }

    优化实现：
    int monthDays[12] = {31, 31, 31, 31, 31};
    int getDays(int month) {
        return monthDays[--month];
    }