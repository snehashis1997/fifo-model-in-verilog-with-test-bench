
module fifo;
 parameter full=4;
 parameter empty=0;
 input da_sig;
 input [4:1] da_in;
 output reg [4:1] da_out;
 input push,pop;
 
 //coding starts
 
  counter cnt(da_cnt,push,pop);
  always @(da_cnt)
  case(da_cnt)
   1 : da_out=da_in[1];
   2 : da_out=da_in[2];
   3 : da_out=da_in[3];
   4 : da_out=da_in[4];
  endcase
 always@(*) 
 if (da_cnt==full)
  $display ("fifo full");
 
  
 else if (da_cnt==empty)
  $display ("fifo empty");
 
 else
  $display ("fifo not empty");
  
endmodule
 
 //counter code
 
module counter(da_cnt,push,pop);

  input push,pop;
  
  output reg da_cnt=0;
  
  always @(*)
  
  if (push) da_cnt=da_cnt+1;
   
  else if (pop)   da_cnt=da_cnt-1;
  
  else $display("error");
  
endmodule
