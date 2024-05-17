# VLSI-EXPT-2
# SIMULATE AND SYNTHESIS ENCODER,DECODER, MULTIPLEXER, DEMULTIPLEXER, MAGNITUDE COMPARATOR USING VIVADO
## AIM :
       To simulate and synthesis ENCODER, DECODER, MULTIPLEXER, DEMULTIPLEXER, MAGNITUDE COMPARATOR using VIVADO
## APPARATUS REQUIRED : VIVADO 2023.2
## PROCEDURE :
STEP:1 Start the Vivado, Select and Name the New project.<br>
STEP:2 Select the device family, device, package and speed.<br>
STEP:3 Select new source in the New Project and select Verilog Module as the Source type.<br>
STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it.<br>
STEP:5 Select the Behavioural Simulation in the Source Window and click the check syntax.<br>
STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table

8:3 ENCODER :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/2d430198-a1a5-4207-8d78-ad02b2163490)
## PROGRAM :
module encoder83df(i, a, b, c);<br>input [7:0]i;<br> output a,b,c; <br>assign a=i[4] | i[5] | i[6] | i[7];<br> assign b=i[2] | i[3] | i[6] | i[7];<br> assign c=i[1] | i[3] | i[5] | i[7];<br> endmodule
## output :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/25298fc8-fd37-4995-a9c2-8c4fcaf08034)

DECODER 3:8 :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/bfd7d197-fed1-4a04-aff0-942c5071c203)

## PROGRAM:
module decoder_3_8(s,y);<br>input [2:0]s;<br> output [7:0]y;<br> assign y[0]=~s[2]&~s[1]&~s[0];<br> assign y[1]=~s[2]&~s[1]&s[0];<br> assign y[2]=~s[2]&s[1]&~s[0];<br> assign y[3]=~s[2]&s[1]&s[0];<br> assign y[4]=s[2]&~s[1]&~s[0];<br> assign y[5]=s[2]&~s[1]&s[0];<br> assign y[6]=s[2]&s[1]&~s[0]; <br>assign y[7]=s[2]&s[1]&s[0]; <br>endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/e4f151bb-0c26-4816-b21d-c78af598da0f)
## MULTIPLEXER 8:1 :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/b25f3bef-a576-4bf0-9c94-40ce09f27bc5)
## PROGRAM :
module Mux 8 1 (s0,s1,s2, i,y);<br> input [7:0]i;<br> input 50, s1,s2;<br> output y; <br>wire [7:0]w;<br> assign w[0]=(~s2) & (~sl) & (~50)&i[0];<br> assign w[1]=(~32)&(~51) & (50) &i [1];<br> assign w[2]=(~52) & (sl) & (~50)&i [2];<br> assign w[3]=(~52) & (51) & (50) &i [3];<br> assign w[4]=(s2) & (sl) & (~50)&i [4];<br> assign w[5]=(s2) & (sl) & (s0) &i [5];<br> assign w[6]=(52) & (51)&(~50)&i [6];<br> assign w[7]=(s2) & (51) & (s0)&i [7];<br> assign y=w[0][w[1] w[2] w[3] w[4] w[5] w[6] w[7];<br> endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/4ad7865e-31ff-4594-b833-fbb735214c93)

## DEMULTIPLEXER 1:8 :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/f473e6d7-ee46-41f2-bde1-7e6f5acd4bcf)
## PROGRAM :
module fa (a,b,c,sum, carry);<br> input a,b,c;<br> output sum, carry; <br>wire w1,w2,w3;<br> xor gl(wl,a,b);<br> xor g2 (w2,a,b);<br> xor g3 (sum, w1,c);<br> and (w3,c,w1);<br> or g5 (carry, w3,w2); <br>endmodule
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/d454e935-7cf4-47e8-9093-e5549219b9c7)

## MAGNITUDE COMPARATOR :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/3d4dc9b2-6b04-4daa-857a-a1189a8eb962)
## PROGRAM :
module comparator(a,b,l,g,e);<br> input [3:0]a,b;<br> output reg l,g,e;<br> always@(*) begin if(a>b) begin l=1'b0;<br> g=1'b1;<br> e=1'b0;<br> end<br>
else if(a<b)<br> begin l=1'b1<br>; g=1'b0;<br> e=1'b0;end <br>endmodule <br>
## OUTPUT :
![image](https://github.com/JAYASHREEER/VLSI-EXPT-2/assets/166278992/eef93e9a-a651-4bb0-b66f-0db1f6343d05)

## RESULT :
The simulate and sythesis ENCODER, DECODER, MULTIPLEXER, DEMULTIPLEXER, MAGNITUDE COMPARATOR using VIVADO is successfully verified














