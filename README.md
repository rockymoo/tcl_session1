# VSD-TCL TASKS
#  A REPOSITRY FOR VSD-TCL WORKSHOP FILES
To create the command to pass .csv from UNIX shell to TCL script Scenarios: 

# DAY 1
# introduction to tcl 
sub tasks:

 1.1Create a command to pass the .csv(excel sheet) from Unix Shell to TCL script
 
  1.2Convert all inputs to format[1] and SDC format and pass it to synthesis tool yosys
 
  1.3Convert format[1] 0r from yosys and SDC to format[2] and passing into timing tool OpenTimer
  
  1.4Generate the output timing report

  To create the command to pass .csv from UNIX shell to TCL script Scenarios:

no .csv provided

$argv[1]           // gives the first argument 
$argv[2]           // gives the second argument and so on....
$#argv             // gives the number of arguments passed in the command
