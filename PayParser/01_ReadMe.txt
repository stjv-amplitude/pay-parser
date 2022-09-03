# Pay Parser
Licence : GPL3  
Author : Don't want to be named  

A tool for parsing a folder of pay sheets in pdf  
This tool rely pdftotext.exe in order to work (http://www.xpdfreader.com/)  

Simple use : Drag a folder containing the invoices pdf on PaieParser.exe

To add support for more invoice format :
 - add regular expression to config.json
 - make sure you are saving it in UTF-8
 - use pdftotext.exe and a regex evaluator to find the correct formula (for instance : https://regex101.com/ with the .NET flavor setting)


CLI options :  
PaieParser.exe [--Status] [--Export \<file-name>] [--pdftotext \<path>] [--no-pad-zero] [--start-date \<yyyy/MM>] [--separator (comma|colon|semicolon|space|tabulation)] FolderName  
--config : Config file path, default : "config.json"
--status : Display info on which file has been succesfully parsed  
--export : The exported csv name, default : "Pay.csv"  
--pdftotext : Path to pdftotext.exe, default : "pdftotext.exe"  
--no-pad-zero : Don't add zero entries between non found months  
--start-date : Prefix the file at date "yyyy/MM"  
--separator : Specify the separator type, can be either comma|colon|semicolon|space|tabulation, default : "semicolon"  
