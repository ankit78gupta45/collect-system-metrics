**Steps to perform and collect System metrics:

1. Download elasticsearch from --> https://www.elastic.co/downloads/elasticsearch 

2.After downloading extract the files into C: drive.

3.Open elasticsearch in c drive goto bin folder and run this elasticsearch.bat (node will start automatically).

4.Download Topbeat Windows zip file from --> https://www.elastic.co/downloads/beats/topbeat 

5.Extract the contents of the zip file into C:\Program Files.

6.Rename the topbeat-<version>-windows directory to Topbeat.

7.Open a PowerShell prompt as an Administrator (right-click the PowerShell icon and select Run As Administrator). 
  If you are running Windows XP, you may need to download and install PowerShell.

8.Run the following commands to install Topbeat as a Windows service:

PS > cd 'C:\Program Files\Topbeat'
PS C:\Program Files\Topbeat> .\install-service-topbeat.ps1

In case of error run

	PS > Set-ExecutionPolicy RemoteSigned

then again try to run  
	
	PS C:\Program Files\Topbeat> .\install-service-topbeat.ps1

9. Configure topbeat.yml file --> https://www.elastic.co/guide/en/beats/topbeat/current/topbeat-configuration.html

10.Loading the Index Template in Elasticsearch.

11.In powershell run this --> PS C:\Program Files\Topbeat> Start-Service topbeat (topbeat starting...)

12.then finally open this url --> http://localhost:9200/topbeat-*/_search?pretty (in browser).

              Output is shown that is details of system metrics.
