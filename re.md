#匹配所有的字母
str='abcdefg1234567890hijklmnopqrstuvwxyz'

ex = re.compile('[^0-9]')
t = re.findall(ex,str)
print(t)


