# 非开发-配置

***
> 版本：3.2.0



``` yaml
pets:
  # 其它属性
  # 自带属性系统依然生效，包括升级后的公式数值，除非设置为0
  dependAttribute:
    # AttributePlus 属性插件
    ap:
      # 是否启用
      enable: false
      # 初始属性，同时会存储到YAML/MYSQL
      basis:
        - "生命力： 30"
      # 升级后属性的变化，同时会存储到YAML/MYSQL
      # 格式 公式|初始值
      # 公式可以使用JavaScriptMath，链接：https://www.runoob.com/jsref/jsref-obj-math.html
      # value_now 是该数值
      # min_now 是~前面的数值
      # max_now 是~后面的数值
      # 使用~要确保初始值含有~
      # | 是分割标志，初始值是在basis没有的时候为其加上该值
      levelUp:
        - "生命力： value_now+2|30"
        - "物理伤害： min_now+1~max_now+10|4~8"
```
