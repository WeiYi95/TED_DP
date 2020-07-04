# 介绍
基于动态规划，对四库全书数据进行的文字定位。
# 配置
pip install numpy==1.17.3  
pip install cv2==3.4.3.18  
# 运行
```
main.py
```
💾首次使用：LOAD = False  
🚨随后若中途出现问题需要从新运行时，需先运行get_processed_books_name.py以避免重复处理。随后将LOAD置为True
🚨运行速度较慢，且对结果置信度的要求较高。
# 说明
模型对每张图片会按列切割和按单字切割。
📌列根据书名存到对应的文件夹中。每本书中切出的列都存在同一文件夹中。命名方式为：书名-对应的文字
📌单字根据书名存到对应的文件夹中。每本书中所有的字都存在同一文件夹中。命名方式为：书名-字-序号
📌具体切割的结果（用红线在原始图片中标出）会保留在 Res 文件夹中。