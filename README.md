# 批量下载知识星球的文件
knowledge-planet_v1.0.0  
用于批量下载知识星球中的文件  
  
knowledge-planet_v2.0.0  
增添更新文件功能  
运行exe文件时，不会再下载之前下载过的文件，以此达到更新文件的目的  
（若要将星球中的文件全部重新下载，只需要清空last_time.txt文件，再运行exe即可）  
  
knowledge-planet_v2.1.0  
修复knowledge-planet_v2.0.0存在的bug  
优化：  
下载的文件会存放在pdf的对应星球id的目录下（例如：从id为233333的星球下载的know.pdf文件存放在：./pdf/233333/know.pdf）  
日志信息存放log目录下  
目录结构介绍：  
pdf目录：存放从星球下载的文件  
cookie_and_url.txt：第一行为cookie，后面的每一行分别对应一个星球id  
knowledge-planet.py：主程序  
log目录：  
last_time.txt：存放本次下载的第一个文件其上传到星球的创建时间（例如：结构为233333=2018-01-11T11:20:20.400+0800，等号前面是星球id，等号后面是创建时间）。目的是为了下次下载星球文件时，检测到是已下载的文件就不再继续下载旧的文件，以此达到运行程序会同步最新文件的目的（若要重新下载星球，只需要删除星球相关的记录，重新运行程序即可）  
log.txt：存放日志信息，结构为时间+文件名+文件id+文件下载地址  
  
附加程序：  
catchid_v1.0.0  
用于自动获取已关注星球的id（id会写入cookie_and_url.txt文件中）  
配合knowledge-planet使用