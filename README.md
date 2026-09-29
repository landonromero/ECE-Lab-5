# Lab 05 - Combinatorial Logic

In this lab, you’ve learned real world applications of digital logic, as well
as how to assemble your own Verilog modules. In addition, you’ve learned how
the constraints file maps your inputs and outputs to real pins on the FPGA.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Name: Evan Walther and Landon Romero

#We used minimized functions in the files for readability, but here are the minterms and maxterms
MINTERMS: (~A&~B&~C&~D)|(~C&~D&~A&B)|(~C&~D&A&B)+(~C&~D&A&~B)+(~C&D&A&B)+(C&D&A&B)+(C&~D&A&B)+(C&~D&~A&B)
MAXTERMS: (A+B+C+D)&(A+B+~C+D)&(A+~B+C+D)&(A+~B+~C+D)&(~A+~B+C+D)&(~A+~B+C+~D)&(~A+~B+~C+~D)&(~A+~B+~C+D)&(~A+B+C+D)&(~A+B+C+~D)&(~A+B+~C+~D)&(~A+B+~C+D)


## Lab Summary
In this lab we programmed 2 circuits and assigned the output of one of them to the input of the other. We assigned 6 switches in total and the output of circuit A to led 0 and a wire that was connected to circuit B. We programmed the logic of each circuit using maxterms and min terms with a truth table. Finally we added constraints to the project and wrote it to the board. 

## Lab Questions

###1 - Explain the role of the Top Level file.
The top.v file is kind of the "main" function in other programming languages. It is used to connect different gates and circuit together, 
for example we use the output of circuit_a to assign to a wire and then use that for the A input in circuit_b.


### 2 - Explain the function of the Constraints file.
The constraints file is what maps the pins to functions and was decided by hardware engineers ahead of time. We have to uncomment certain led's and sw's so that they are available for us on the board to use.

### 3 - Was the selection of Minterm and Maxterm correct for each circuit? What would you have chosen?
Yes the selection for both min term and maxterm was correct for each circuit. I would have chosen min terms for circuit A due there being less ones than zeros which makes it easier to extract the function.
