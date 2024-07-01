<p align="center">
<img alt="1" src="https://private-user-images.githubusercontent.com/163789590/314762211-9ea02092-b450-472d-bceb-ae612bcb07e4.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyMjExLTllYTAyMDkyLWI0NTAtNDcyZC1iY2ViLWFlNjEyYmNiMDdlNC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05NWFlOWM4OGUyY2E3ZmJjN2E0YzgzZjIwZDY3ZWE3M2Q3N2Q1ZjA5ZjMxOTY3YmFkYTk4M2EyZDY5NmY5MDcwJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.6ccQzOJ0HJckx0ru5qddIh6RvGN7txaV3-1YfPDyuc4"/>

</p>

<h1> Active Directory Deployed in the Cloud (Azure)  </h1>


<p>Starting from where the first part of this tutorial ended, that produced our simulated Active Directory environment, in this second part we will explore the details of deploying and refining an Active Directory system. This part is designed to give a basic understanding of Active Directory services, emphasizing essential aspects such as installation, forest creation, user account administration, domain integration, and customized Remote Desktop Connection access.

</p>

<h2>Prerequisites</h2>

- <a href= </a>

<h2>Key Objectives</h2>
<h3>Active Directory Installation</h3>

-  Set up and install Active Directory services on the chosen Domain Controller virtual machine.

<h3>Forest Creation</h3>

- Create a new Active Directory forest.

<h3>Administrator Account Creation</h3>

- Produce and administer user accounts with administrative privileges to deal efectively with the Active Directory environment.

<h3>Domain Joining</h3>

- Introduce the Client-01 virtual machine into the established domain, ensuring uninterrupted communication with the Active Directory infrastructure.

<h3>Remote Desktop Setup</h3>

- Configure Remote Desktop Connection access specifically designed for non-administrative users, improving user accessibility while keeping security protocols.




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)


<h2>Configuration Steps</h2>

<h3>&#9312; Install Active Directory in DC-01</h3>

- In the Server Manager dashboard, click Add roles and features and continue the setup <img width="736" alt="2" src="https://private-user-images.githubusercontent.com/163789590/314762456-e6004d64-09cf-4472-b00a-08f2689b489b.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyNDU2LWU2MDA0ZDY0LTA5Y2YtNDQ3Mi1iMDBhLTA4ZjI2ODliNDg5Yi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT00ODE0ZDZlODIxMGU0OTJkODExZmMxZDA2OWZmMzc5N2NlNzQ3ZGQ0NGU1Yjg3NzU4ZjNmMDg3NTcxMGJjOGZmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.gX220uQPHuOb31pHgVBuHDPlgA4jTURJM-nGWbNP24s">


<p>

</p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<p><strong> Select Active Directory Domain Services and finish the installation </strong> </p>
<p>
</p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#9313; Promote DC-01 to Domain Controller </h3>

- Once the installation is done, notice the flag on the top left of the Server Manager
- Click on the flag and promote DC-01 to Domain Controller.

<img width="242" alt="3" src="https://private-user-images.githubusercontent.com/163789590/314762776-6020727b-0778-475a-8181-2ad597fe8137.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyNzc2LTYwMjA3MjdiLTA3NzgtNDc1YS04MTgxLTJhZDU5N2ZlODEzNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01YTZhMjk3ZGM5ZGVlYzBlNGQzOTJlNDk1MDJmZGMyOGIwZDkzMmE1ZDcwNzEyODg2N2JjMzliNTNkNjQxYzQ0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.d7R27HINl4Siai-yajkj3xLZYJBKP4AZI3BRZ2eNB6s">




<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

- Now add a new Forest and set the Root domain name to “mydomain.com”
<p>
<img width="565" alt="4" src="https://private-user-images.githubusercontent.com/163789590/314762815-c4ce5731-0b82-4a8a-bf41-1e2c75beeafa.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyODE1LWM0Y2U1NzMxLTBiODItNGE4YS1iZjQxLTFlMmM3NWJlZWFmYS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0zODI1NWMxOTlkZWNkZjdiOTFjOWE4ZWIwNTYxMWUyNWYzYWE4MTJiMDE3NDAxZDFhOGU0OTNmMzA4NThkNTFmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9._i316gzqsfwdVJyFv-8Lp2jlWcVJZWRdsBwIFPn5iC0">
 </p>
  
- Finish setup and restart DC-01
- Log back in with “your username"@mydomain.com



<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#9314; Creating an Admin in Active Directory </h3>

- Once DC-01 has rebooted, click on tools and select Active Directory Users and Computers
- Right-click on mydomain.com and select new and click on Organizational Unit
<img width="438" alt="5" src="https://private-user-images.githubusercontent.com/163789590/314762854-bef564b6-0393-488a-8094-e907f092a3a1.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyODU0LWJlZjU2NGI2LTAzOTMtNDg4YS04MDk0LWU5MDdmMDkyYTNhMS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1iMDRkZmJlNDljZTNkNWQ1MTk2ZDMwYTI4MzAxZTI3ZDk2ZjUxNGNlNTg0NWMyOWIyZTZkM2VkZTRiNDM1OTE5JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.7PS4gobM2oN0iYE_0ZCqyk6YECX4kLUT56Jiva0hhP4">



<br>
<br>
<br>
<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<p><strong> Create an OU named _EMPLOYEES and _ADMINS </strong></p>

<img width="450" alt="6" src="https://private-user-images.githubusercontent.com/163789590/314762922-bf4d2c90-6753-4179-8304-93831f29f81e.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyOTIyLWJmNGQyYzkwLTY3NTMtNDE3OS04MzA0LTkzODMxZjI5ZjgxZS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03OTYwZmZlYzYzM2M5ZjU4ZjE2NTMzMzg3MTdiNGE3YmJlZWFiZGYyZjg1MjA2YzM4YjExOTBmYmMwZjQ0MzlmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.O2R4go5Yu2fV3ephMiHUiUZzDEFCjC2a0w1_FGeXbqs">



<p><strong>.</strong></p>
<p><strong>.</strong></p>

<p><strong> Right-click on Users and produce a new user named Jane Doe with the username jane_admin</strong></p>

<img width="323" alt="7" src="https://private-user-images.githubusercontent.com/163789590/314762953-d1fe5899-daad-4589-9d03-6367f5fbc145.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyOTUzLWQxZmU1ODk5LWRhYWQtNDU4OS05ZDAzLTYzNjdmNWZiYzE0NS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT04OGFhYTg3YzZkYWIwZjQ4ODA2YTExMjFjNDdiZDhlNWY5ZjIxNDZlOGI1NzMxNzgwNTAxYzA1OGFkN2YwZTg3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.aroJ4JDDBHzi_Udbi_k-UZHUrdWZGwrRb4giI6sU6zI">


<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<p><strong>Turn Jane Doe into an admin by right-clicking her name and adding her to the “Domain Admins” Security Group</strong></p>

<img width="412" alt="8" src="https://private-user-images.githubusercontent.com/163789590/314762985-bc7ac07c-1ae5-45d7-9f60-3188ad683769.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYyOTg1LWJjN2FjMDdjLTFhZTUtNDVkNy05ZjYwLTMxODhhZDY4Mzc2OS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1jNDRhNzcyZGEzMGE5N2IzZWZhMzkzNmNhYTM1NmIzNmE5NGE1ZTdkM2Q5NTkyNDFjMjJlNmU3YzA0NTMzNmQxJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.O5JQmE58qC_AOgv1d37ojQcXkcsG0X6q0stEpnEZ_48">



<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<p><strong>Logout of DC-01 and log back in with Jane Doe’s credentials</strong></p>

<img width="337" alt="9" src="https://private-user-images.githubusercontent.com/163789590/314763012-b71e7b29-550c-4e61-a8d1-359f14235f85.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYzMDEyLWI3MWU3YjI5LTU1MGMtNGU2MS1hOGQxLTM1OWYxNDIzNWY4NS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xNmVlZDViYWVlNDBiYzA1ZDZiNmMzMjZmYmJkNDI1MTJjNWYxNTcyNDQ2ZTNiMzkxZGU4ZWNkNjRmMmNjYjA2JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.0y9_xW89uGbwM6ByfTagoAUO2PYf7mNyoWvWUwhjYPo">


<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>


<h3>&#9315; Integrate Client-01 to domain </h3>

<p><strong> For Client-01 to integrate into the domain, first set its DNS server as DC-01’s private address.</strong></p>

- In the Azure Portal, select Client-01 -> Networking -> Network interface and click on DNS servers

<img width="735" alt="10" src=https://private-user-images.githubusercontent.com/163789590/314763040-b47c3880-1e1c-4c95-8613-912b2374cd25.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYzMDQwLWI0N2MzODgwLTFlMWMtNGM5NS04NjEzLTkxMmIyMzc0Y2QyNS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT03YzEzZGIxY2EwMWJhODUzMDNjZWUyYmM5OTlmOGVjMDEzODBmYTg5OWQ5YTgzZDIzNGRhYjliZTU5YmJmYTRmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.VkdPZIXraDsJCV62ZWKU6IzG5yKMP4YonJ_7M3iYRxY"">




<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<p><strong>Choose a custom DNS server and type in the private ip address of DC-01 and restart Client-01</strong></p>

<img width="356" alt="11" src=https://private-user-images.githubusercontent.com/163789590/314763066-ee5fde66-59c9-4644-ad7a-931520473158.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYzMDY2LWVlNWZkZTY2LTU5YzktNDY0NC1hZDdhLTkzMTUyMDQ3MzE1OC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05YWNhNWZhNTA1ZjIzMjhmYjdjM2U3ZjlmM2JmYTk0YmU2MmEzNzJhY2RlZWM5NmViZTNhZjEyMjdlMWE5NTNjJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Gh2CPjAJlU121WwsePCf3aaymK5AWlB8NvfWSOvgbQk"">


<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<p><strong> Now log back in to Client-01 using your original admin credentials. Click start and go to Settings > Rename this PC (advanced) > Change and add “mydomain.com” and log in with the admin credentials previously created (jane_admin) </strong></p>

<img width="297" alt="12" src="https://private-user-images.githubusercontent.com/163789590/314763096-442138e1-caad-4d55-86e7-8d5ab0b38557.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYzMDk2LTQ0MjEzOGUxLWNhYWQtNGQ1NS04NmU3LThkNWFiMGIzODU1Ny5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1hODdiMzUzODE1NDY2ZmIyNjQ5YmM5MzY0N2FlZTg3ZmM0YTAwZmQ5YTE1ZmUxOGEwNDU2OTMxMjQzZjUzM2Q2JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.zTkLk01oHT3JchagzROw5yJ0iOrSuDdYgrVTHX-yiWA">

<br>

<p> <strong>Once Client-01 has been added, the VM will restart.</strong></p>


<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>

<h3>&#9316; Setup the Remote Desktop Connection for non-administrative users </h3>

- Log back into Client-01 using jane_admin, open Settings > Remote Desktop> User Accounts and click “Select users that can remotely access this PC”
- Add Domain Users

<br>

<img width="343" alt="13" src="https://private-user-images.githubusercontent.com/163789590/314763333-31475ba9-6628-41c1-8aef-a11f896cb0e6.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MTk4NzYwNDUsIm5iZiI6MTcxOTg3NTc0NSwicGF0aCI6Ii8xNjM3ODk1OTAvMzE0NzYzMzMzLTMxNDc1YmE5LTY2MjgtNDFjMS04YWVmLWExMWY4OTZjYjBlNi5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwNzAxJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDcwMVQyMzE1NDVaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT02MTcxOWZkNTkyZTJkMjdmM2E2ODYwNDkyYzk5NTQ4MTVhYzRmMDFhMWYwZDY3NGNjMDNlZmNiODI3NDQ2ZDQ0JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Tuw2OYqiMpSwwkTEudBU3SIxbdKhjaf-lJiAIKO-iHA">

<p><strong>This will allow normal users to login to Client-01</strong></p>

<br>

<p><strong>.</strong></p>
<p><strong>.</strong></p>
<p><strong>.</strong></p>



<h2> In Conclusion </h2>

<p>
We've successfully completed the second part of this tutorial. Through configuring Active Directory on the Domain Controller, we grounded our infrastructure by creating a forest, administrator account, and at the very end of it all, integrating Client-01 into the domain. In the third part of this tutorial, users will be generated and various Active Directory situations will be simulated. </p>
</p>


