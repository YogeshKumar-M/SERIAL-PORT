
# Serial Transfer of Single Byte / Character using 8051 (Keil)

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in Keil.

## APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

## PROGRAM

### (i) Serial Port Transfer a Single Character

```
#include<reg51.h>
void main(void)
{
TMOD=0X20; //TIMER 1, MODE 2
TH1=0XFA;
SCON=0X50;
TR1=1;
while(1)
{
SBUF='A';
while(TI==0);
T1=0;
}
}


```
### (ii) Serial Port to Transfer a Message

```
#include<reg51.h>
void main(void)
{
unsigned char msg[]="PROGRAME 8051";
unsigned char i;
TMOD=0X20;//TIMER 1,MODE 2
TH1=0XFC;
SCON=0X40;
TR1=1;
for (i=0; i<17;i++)
{
SBUF= msg[i];
while(TI==0);
TI=0;
}
while(1);
}


```

### OUTPUT:

(i)
<img width="1673" height="611" alt="Screenshot 2025-11-11 193355" src="https://github.com/user-attachments/assets/1a7ffd94-4769-43b1-acaf-040df89b2936" />

# MANUAL
![WhatsApp Image 2025-11-11 at 18 53 56_684302d5](https://github.com/user-attachments/assets/2746de30-10b4-4d7a-bd92-c50d05c082fc)


(ii)
<img width="1666" height="606" alt="Screenshot 2025-11-11 192547" src="https://github.com/user-attachments/assets/871debd8-94aa-42f8-a36d-c7924880ceea" />

# MANUAL
![WhatsApp Image 2025-11-11 at 18 53 56_c90960ad](https://github.com/user-attachments/assets/5671fced-f17f-40bc-9323-17bfcddfea70)


### RESULT:
Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
