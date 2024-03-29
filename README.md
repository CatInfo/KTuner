# WHAT IS KTUNER

&ensp;&ensp;KTuner is an expert-level Oracle & MS SQL Server diagnostic and optimization platform that is comprehensive in functionality, lightweight, driverless, proxyless, and requires no installation. It directly connects to the database with a single click, accurately identifies sources of issues and performance bottlenecks, automatically diagnoses and generates analysis reports along with optimization scripts. KTuner serves as a productivity tool exclusively designed for database administrators (DBAs) and operations experts.

# KEY FEATURES

- Focused on problem diagnosis and performance optimization
- Comprehensive historical tracing
- Automatic diagnosis and performance optimization
- No need for agent
- No need for client driver
- No need for ODBC driver
- Run directly without installation
- The Swiss Army Knife for DBA Experts
- An efficient assistant for APP O&M specialist's tool
- Widely used in core database management for industries such as banking, telecommunications, securities, healthcare, government, and higher education.

# SCREENSHOTS  
## Bright Or Dark    
![image](https://github.com/CatInfo/KTuner/blob/main/images/Style.jpg)
## Intuitive And Efficient
![image](https://github.com/CatInfo/KTuner/blob/main/images/UI.jpg)  
## Highlight Issues  
![image](https://github.com/CatInfo/KTuner/blob/main/images/OraSql.jpg)  
## Graphical Presentation  
![image](https://github.com/CatInfo/KTuner/blob/main/images/MsSql.jpg)

# CONFIGURATION

&ensp;&ensp;No configuration required. You can directly run the KTuner.exe file to use KTuner. For more detailed instructions, please refer to the KTuner User Manual.

# COMPATIBILITY

&ensp;&ensp;To run KTuner, the following configurations are required:

- **Operating System**

&ensp;&ensp;&ensp;&ensp;All versions of Windows, both 32-bit and 64-bit, are supported.

- **Memory and Disk Space Capacity**

&ensp;&ensp;&ensp;&ensp;No specific requirements.

- **Display Resolution**

&ensp;&ensp;&ensp;&ensp;A resolution higher than 1024 x 768 (pixels) is recommended for optimal performance; lower resolutions may result in suboptimal display quality.

- **Target Database**

| Version               | Compatibility     |
| ----------------------| ----------------- |
| Oracle 11g            | ✅                |
| Oracle 12c            | ✅                |
| Oracle 18c            | ✅                |
| Oracle 19c            | ✅                |
| Oracle 21c            | ✅                |
| MS SQL Server 2008    | ✅                |
| MS SQL Server 2008 R2 | ✅                |
| MS SQL Server 2012    | ✅                |
| MS SQL Server 2014    | ✅                |
| MS SQL Server 2016    | ✅                |
| MS SQL Server 2017    | ✅                |
| MS SQL Server 2019    | ✅                |

> Note: Some functions within the PDB might be restricted.
- **Database Account Permissions**

&ensp;&ensp;KTuner utilizes existing database accounts to connect to the database and query its performance status. The simplest method is usually by using the 'system' account(in Oracle) or 'sa' account(in MS SQL Server), or alternatively, you may opt for another account (let's assume the account name is 'ktuner') with the following necessary permissions:

| DB Type       | Minimum Permissions                                   | Optimal Permissions                                                        |
| ------------- | ----------------------------------------------------- | -------------------------------------------------------------------------- |
| Oracle        | CONNECT, SELECT ANY DICTIONARY                        | CONNECT, SELECT ANY DICTIONARY, ALL PRIVILEGES                             |
| MS SQL Server | CONNECT, VIEW SERVER STATE, CONTROL(in msdb database) | CONNECT, VIEW SERVER STATE, CONTROL(in msdb database), VIEW ANY DEFINITION | 

&ensp;&ensp;If you prefer to log in to KTUNER using a newly created database account instead of an existing one, the following are example scripts:
 
    -- Oracle
    create user ktuner identified by <yourpassword> default tablespace users;
    grant CONNECT to ktuner;
    grant SELECT ANY DICTIONARY to ktuner;
    grant ALL PRIVILEGES to ktuner;

    -- MS SQL Server
    create login ktuner with password = <yourpassword>;
    use master;
    grant VIEW SERVER STATE to ktuner;
    grant VIEW ANY DEFINITION to ktuner;
    use msdb;
    create user ktuner for login ktuner;
    grant control to ktuner;
    
# License Statement

&ensp;&ensp;This software operates on a subscription basis. New users can apply for a free trial for a specific number of days. Within the valid licensing period, users are eligible to upgrade to the latest version. For more details, please refer to the license document.

# Further Explanation

1. KTuner utilizes the most efficient direct connection method to communicate with the database and does not undergo any additional encryption or translation processes.
2. KTuner does not engage in any invasive actions towards the database. All information is sourced from the data dictionary, which refers to the metadata describing the database itself.
3. Once initiated, KTuner establishes five persistent sessions to connect with the database. However, KTuner strictly controls its impact on the database load, keeping it nearly negligible.
4. KTuner software is restricted for use outside of  Chinese mainland.

# Contact Us

&ensp;&ensp;We eagerly welcome your feedback. If you have any questions or concerns, please contact us through the following channels:

- ☎️: +86-25-52442441
- 📮: support@catinfo.com.cn
- 📮: sales@catinfo.com.cn

# Copyright Information

&ensp;&ensp;Copyright @ 2016-2024 Catinfo Technologies. 

&ensp;&ensp;All rights reserved, including but not limited to the copying, modification, development of derivative products, distribution, and sale of any part of this software. Without explicit written permission from the copyright owner, it may not be used for any commercial purposes.
