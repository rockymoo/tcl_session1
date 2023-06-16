# VSD-TCL TASKS
#  A REPOSITRY FOR VSD-TCL WORKSHOP FILES
To create the command to pass .csv from UNIX shell to TCL script Scenarios: 

no .csv provided 

$argv[1]           // gives the first argument  
$argv[2]           // gives the second argument and so on.... 
$#argv             // gives the number of arguments passed in the command 
 

 
to display an error message the following code snip can be used: 

if($#argv != 1) then 
echo "Please provide the .csv file only" 
exit 1  
endif 
 

save the file with the name rakesh and make it executable by executing the following command in the terminal: 

sudo chmod -R 777 rakesh
 

to execute the file use the following command: 

./vsdsynth 
 

non-existent .csv provided and -help The following code snip can be used: 

if(! -f $argv[1] || $argv[1] == "-help") then; 
	if($argv[1] != "-help") then ;
		echo "Error: Cannot find csv file $argv[1]. Exiting..." ;
		exit 1 
	else 
		echo "USAGE: ./vsdsynth <csv file> , where the <csv file> consists of 2 columns  -->  1st column is being case sensitive." 
		echo "Note if the file is not in the same directory, ensure to include the path along with the <csv file>" 
		echo  
		echo "<Design Name> is the name of the top module" 
		echo  
		echo "<Output Directory> is the name of the output directory where you want to dump synthesis script, synthesized netlist and timing report"  
		echo  ;
		echo "<Netlist Directory> is the name of the directory where all RTL netlist are present" ;
		echo 
		echo "<Early Library Path> is the file path of the early cell library to be used for STA" ;
		echo ;
		echo "<Late Library Path> is the file path of the late cell library to be used for STA" ;
		echo 
		echo "<Constratints file> is the csv file path of constraints to be used for STA" 
		echo 
		exit 1 
	endif 
else 
		tclsh vsdsynth.tcl $argv[1] 
endif 

 
