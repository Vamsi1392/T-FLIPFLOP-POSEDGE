# T-FLIPFLOP-POSEDGE

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

![Screenshot 2025-05-06 094114](https://github.com/user-attachments/assets/0aca1749-7127-4957-a513-50ff81567478)


## **PROGRAM**
Developed by:Pugazhalenthi V

Register No:212224100047

```
module pugal9(t, clk, rst, q);
  input t, clk, rst;
  output reg q;

  always @(posedge clk or posedge rst) 
begin
    if (rst)
      q <= 0; 
    else if (t==0)
      q <= q; 
     else
        q<=~q;
  end
endmodule

Developed by: M.V.Vamsidhar Reddy
RegisterNumber: 212224040205



```


**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/user-attachments/assets/115c8aec-7de0-4541-80ff-c0f3950a5b1e)


**TIMING DIGRAMS FOR FLIP FLOPS**

![image](https://github.com/user-attachments/assets/ae289843-61d0-44a7-bd0c-4993d104b81e)


**RESULTS**

implementation of T flipflop using verilog and validating their functionality using their functional tables
