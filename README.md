# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
OUTPUT:
![WhatsApp Image 2025-11-02 at 21 01 10_8fd5f289](https://github.com/user-attachments/assets/92de9d1e-3ffb-44d5-bf80-c6089f9a1bcf)


![WhatsApp Image 2025-10-29 at 09 44 56_dd769193](https://github.com/user-attachments/assets/22ec4f44-741c-47bd-803f-afae634bce4d)

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
