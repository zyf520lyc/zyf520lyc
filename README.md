import requests
from lxml import etree
# import webbrowser
# webbrowser.open('https://www.shunvi.com/meitu/45825_5.html#p')
while True:
    for x in range(2,41):
        a='https://img.shunvi.com/id/2016/05/45825/{}.jpg'.format(x)
        asd=requests.get(a)
        # asq=etree.HTML(asd.text)
        f=open("{}.jpg".format(a[40:42]),"ab")
        f.write(asd.content)
        f.close()
