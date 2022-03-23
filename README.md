HOW TO INTERACT EXCEL DATA WITH ARDUINO

1/ Enable data streamer in excel: go to file->options->select Add-ins-> Under Manage select Com Add-ins item, click Go->Select Microsoft data streamer for excel->Click OK



2/Plug Arduino into laptop



3/ Click the new Data streamer that appears on the excel menu-> Click Connect a device-> Select the port corresponding to the new arduino plugged into the laptop



4/Select Advanced in excel->Select Settings->Select baud rate



5/Go to the Settings sheet->Select the data rows size, that is, the number of orders scanned in the working day to check, for example 10000 rows need to scan the code



6/ Go to the Data In sheet in excel, click Start Data, the code scanned data on the arduino will automatically stream to excel



7/ Enter the entire barcode content in column M of the Data In sheet (for example, you can choose any), then enter the command =COUNTIF($B$8:$B$10007,M8) (refer to https://www.w3schools.com/excel/excel_countif.php) into the cell in column N corresponding to each barcode, when each scan orders in the warehouse to export or import goods, if there are goods that match the barcode in the file, then cell N will automatically add 1, and so on, it will automatically add up when there is a duplicate barcode.

