# Using-cinema
第13組
B10409035 戴文諺
B10409009 陳威力
B10409008 吳宏毅
電影輸入器：
建了電影院系統，會先列出全台威秀電影院
依照你所輸入的電影院，給你這一星期的電影時刻表
你就可以開心地查詢威秀電影了！！

程式碼：
# coding: utf-8

# In[ ]:

import requests
from bs4 import BeautifulSoup
print("---------歡迎光臨威秀影城查詢系統---------\n" +      "1  = 台北信義威秀影城\n"+      "2  = 台北京站威秀影城\n" +      "3  = 台北日新威秀影城\n"+      "4  = 板橋大遠百威秀影城\n"+      "5  = 新竹大遠百威秀影城\n"+      "6  = 新竹大遠百威秀影城(Gold Class)\n"+      "7  = 新竹巨城威秀影城 \n"+      "8  = 頭份尚順威秀影城 \n"+      "9  = 台中大遠百威秀影城 \n"+      "10 = 台中Tiger City威秀影城 \n"+      "11 = 台中Tiger City威秀影城(Gold Class) \n"+      "12 = 台中新時代威秀影城 \n"+      "13 = 台南南紡夢時代威秀影城\n"+      "14 = 台南南紡夢時代威秀影城 (Gold Class)\n"+      "15 = 台南大遠百威秀影城 \n"+      "16 = 高雄大遠百威秀影城\n"+      "17 = 高雄大遠百威秀影城 (Gold Class)\n")
while True:
    x = int(input("請輸入店名編號:"))
    if 1<=x<=17:
        if x == 1:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0006|TP&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 2:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0009|QS&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 3:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0008|XM&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 4:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0010|BQ&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 5:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0005|HS&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="    
        elif x == 6:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0005|HSGC&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 7:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0012|BC&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="    
        elif x == 8:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0014|TF&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="    
        elif x == 9:   
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0011|TZ&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="    
        elif x == 10:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0002|TT01&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="    
        elif x == 11:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0002|TT02&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 12:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0003|TD&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 13:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0013|NF&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 14:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0013|NFGC&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 15:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0004|TN&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 16:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0001|KS&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        elif x == 17:
            web = "http://sales.vscinemas.com.tw/ticketing/visPrintShowTimes.aspx?visCinemaID=0001|KSGC&visMultiCinema=Y&visLang=2&ReturnURL=&visEventCode="
        
        res = requests.get(web)
        res.encoding = 'utf-8'
        soup = BeautifulSoup(res.text,'lxml')
        for item in soup.select('#ddlCinema'):
            print("\n" +                  item.select('option')[x-1].text)
        a = soup.get_text()
        print(a[299:328] +              a[338:-5])
        print("----------------到底囉!----------------")
    else:
        print("-----------請輸入正確數字喔~!-----------")


# In[ ]:


