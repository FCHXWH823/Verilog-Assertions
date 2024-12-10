# Verilog-Assertions

## Concurrent Assertions
 
property identifier [argument_list]; 
          [clocking_event] [disable iff (reset)] property; 
endproperty[:identifier] 

Here, the square brackets are not part of the syntax, they show that the corresponding constructs are optional. 

Example: 
assert property (@(posedge clk) disable iff (rst) a |-> nexttime[2] b); 

### Overlapped/Non-overlapped Implication
Overlapped implication (|->): If there is a match on the antecedent, then the consequent expression is evaluated in the same clock cycle. 
Non-overlapped implication (|=>): If there is a match on the antecedent, then the consequent expression is evaluated in the next clock cycle. 

 