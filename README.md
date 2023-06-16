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

$argv[1]           // gives the 1st argument 
$argv[2]           // gives the 2nd argument
$#argv             // gives the number of arguments passed  


code for task  following:

if(! -f $argv[1] || $argv[1] == "-help") then

	if($argv[1] != "-help") then
 
		echo "Error: Cannot find csv file $argv[1]. Exiting..."
  
		exit 1
  
	else
 
		echo "USAGE: ./rakesh <csv file> , where the <csv file> consists of 2 columns  -->  1st column is being case sensitive."
  
		echo "Note if the file is not in the same directory, ensure to include the path along with the <csv file>"
  
		echo 
  
		echo "<Design Name> is the name of the top module"

  endif
  
else

		tclsh rakesh.tcl $argv[1]
  
endif
![WhatsApp Image 2023-06-16 at 17 47 38](https://github.com/RAKESHRAKIHR/tcl_session1/assets/126293037/8ae056b0-31d7-47f2-b8f2-d11f590b02d5)

![WhatsApp Image 2023-06-16 at 17 29 43](https://github.com/RAKESHRAKIHR/tcl_session1/assets/126293037/eaae8d07-bcbf-45aa-a575-b29d822be9af)


# DAY 2


