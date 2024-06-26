
--------------------------
版本修改
--------------------------
 - 3.0.3
    - 加入了groupName 方便处理双行表头问题
    - ExcelEntity 也支持双行设置
    - 加入和导入列顺序校验
    - 修复图片导出bug
    - 修复默认值问题
    - ali规范修复版本
    - 修复double默认值问题
    - 其他小问题
 - 3.0.2 版本 新包名版本,看自己需求跟新
     - word 遍历样式复制
     - 导入校验返回增强
     - 导入校验,校验组参数
     - Excel--html图标不在单独生成
     - Excel模板导出加入了图片支持
     - 修复了dubbo处理问题

 - 3.0.1 版本 新包名版本,看自己需求跟新
    - 加了一个numformat 属性,方便格式化数字
    - 修复view 再特定情况无法找到的bug
    - 加强了缓存发现路径,加了绝对路径,相对路径,包路径三种规则
    - 提供可全新的key-value 读取规则,方便特殊字段读取
    - 加强了HtmlXorExcel 之间的转换,可以互相转换
    - 加强了时间这个类型的处理
    - 以及其他的小bug


 - 2.4.0 修复bug,推荐更新
 	- 支持使用html模板处理Excel  HtmlToExcelUtil
 - 2.3.1 修复bug,推荐更新
 	- 支持三目运算嵌套
 	- 提供大量导出功能,分批插入数据
 	- 勉强支持模板统计了
 	- 把最大值设置成参数
 - 2.3.0.1 修复bug,推荐更新
 	- 提供的PDF基础的Excel导出支持
 	- 提供了Excel Charts的导出支持
 	- 升级了ＰＯＩ
 	- 提供了Word换行支持
 	- 图片提供统一缓存
 	- 增加Cell取值工具，自动分辨合并单元格和独立单元格
 	- 修复合并单元格,获取cell改为递归,之前判断有问题
 	- 修改了下,el表达式的==判断,给fe加上了样式自定义方法
 	- 修复if(),单字段的判断
 	- 修复其他一些bug
 - 2.1.6 校验规则不向下兼容,升级请自行考虑
 	- 其实不想升的,不过有必要的bug要修复,所以就先生上来吧
 	- 升级交易为hibernate校验,hibernate的maven自己配置可选
 	- WORD的Excel遍历 的Row,改为Insert Row
 	- 修复了font的数组越界
 	- 修复targetId的数组越界
 	- 修复多行模板导出的bug
 	- 增加了验证Excel的功能

 - 2.1.5 bug修复,建议升级
 	- fix指定sheetNum导入的bug
 	- add导入时候setIndex(null) 可以防止识别为集合的问题
 	- fix导入excel列数量判断有bug，导致有些列数漏掉校验
 	- update修改了getValue的方式,减少导入cell value识别错误
 - 2.1.4
 	- 模板输出自动合并单元格功能
 	- 多行模板数据导出
 	- 导出链接功能
 	- 把反射加入了缓存
 	- word和Excel语法保持了统一
 	- Excel to Html 增加了图片显示和缓存功能
 	- 导入增加一个参数startSheetIndex 用以指定sheet位置

 - 2.1.3
 	- 屏蔽了科学计数法的问题
 	- 修复了多模版记得清空记录信息
 	- 加入了map setValue的接口,用以自定义setValue,主要是可以自定义key
 	- 把合并单元格的数据提起出来,让大家都可以复用
 	- 多个sheet导出问题

 - 2.1.2
 	- groupId 改成org.jeecg,为了以后可以直接提交到中央库了
 	- 把test 那个模块删除了
 	- 提供了Excel 预览的功能
 	- type 新增一个 4类型,用于Excel是数字,但是java 是String,防止科学计数法
 	- 修复一些bug
 - 2.1.1-release -小更新/防止下一个预览功能太久不能发布更新
 	- $fe标签
 	- 几个可能影响使用的bug
 	- 导入Map的支持
 - 2.0.9-release--模板功能更新
 	- 修复了中文路径,float类型导入等bug
 	- 增加了根据CellStyler判断cell类型的功能
 	- 优化了一下代码,sort 的compare 改为类实现接口,getValue统一由public处理
 	- height和width 都改成double 可能更加准确的调整
 	- 升级到common-lang3
 	- 可以循环解析多个模板
 	- !!模板增加了多个标签功能
 - 2.0.8-release--小版本更新
 	- 分开了基础注解和base包,编译maven多模块集成
 	- 加强了Excel导入的校验功能,可以追加错误信息,过滤不合格数据
 	- 修复了spring mvc下的07版本不支持的问题
 	- 添加了@  Controller 注解,扫描org.jeecgframework.poi.excel.view路径就可以了,不用写bean了
 	- 加强了styler的自定义功能,参数改为entity,自由控制
 	- test包下面增加了几个demo
 	- 导出添加了一个冰冻列属性,可以简单执行
 	- PS: 经过这段时间项目中的测试,模板导出Excel复杂报表可以省5倍以上的时间,特别是样式复杂的完全可以在Excel中完成,不是在代码中完成了
 - 2.0.7-release--推荐更新
 	- 增加了合计的参数,便于统计合计信息
 	- 修改了样式设置,使用默认设置,提供其他设置,和样式接口
 	- 模板导出增加了插入导出的功能
 	- 模板导出重用了Excel导出的代码功能更加强劲
 	- 新增了Sax导入方式,大数据导入提供接口操作
 	- Word修改了页眉页脚不替换的bug
 	- 修改了捕获异常日志的bug
 	- 修复了模板导出,Spring View没识别版本的bug
 	- 修复了其他一些小bug
 - 2.0.6-release
 	- 修复导入的自定义格式异常
 	- 修复导入的BigDecimal不识别
 	- 导出大数据替换为SXSSFWorkbook,提高07版本Excel导出效率
 	- 根据sonar的提示,修复编码格式问题
 	- 做了更加丰富的测试
 	- word 导出的优化
 		
 - 2.0.6-SNAPSHOT
	 - 增加map的导出
	 - 增加index 列

