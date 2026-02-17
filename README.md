
Course: PL/SQL
--
Assignment 2: Database Creation, Deletion & OEM
--
Name: MUHIMPUNDU Anne Marie
-
ID: 29398
-
Group: D
-
Introduction
 -
This assignment was completed to demonstrate practical understanding of Oracle Multitenant Architecture using Oracle Database   

The objective was to:
- Create and manage Pluggable Databases (PDBs)
- Create a dedicated user inside a PDB
- Create and completely remove a temporary PDB
- Access and verify configuration using Oracle Enterprise Manager (OEM)
- Document all work professionally and publish it on GitHub

Task1:Create a New Pluggable Database
-
The following are commands i used to get connected to my oracle as SYSDBA and Creat a new pluggable database named "mu_pdb_29398" and save it as it was asked.

sqlplus / as sysdba
-
CREATE PLUGGABLE DATABASE pdb_name
ADMIN USER pdb_admin IDENTIFIED BY password
FILE_NAME_CONVERT = ('pdbseed', 'pdb_name');
-
![Image Alt](https://github.com/muhimpunduanne/oracle_pdb_ass_II_29398_MUHIMPUNDU/blob/383181e9e216693b9ad384a2bbaddf30a7b4f861/PL_SQL_PDB/PL_PDB_CREATED_0.png)

 PDB open state

ALTER PLUGGABLE DATABASE pdb_name OPEN;
-
![Image Alt](https://github.com/muhimpunduanne/oracle_pdb_ass_II_29398_MUHIMPUNDU/blob/ab55fd2ef4bf6f16ccecea398101002bc4e74186/PL_SQL_PDB/PL_PDB_OPENED_1.png)

User created inside the PDB Your username must be clearly visible
    
![Image Alt](https://github.com/muhimpunduanne/oracle_pdb_ass_II_29398_MUHIMPUNDU/blob/1cd2b95d3d5d8529b1a037371be7d3e9d40cd6c4/PL_SQL_PDB/PL_PDB_THE_CREATED_USER_7.png)

Task 2: Create and Delete a PDB
-
Before creating another pdb i switched to root container in order to avoid error because oracle only allows you to create or drop PDBs from the CDB root container not from inside another one as it follows here:
 ![Image Alt](https://github.com/muhimpunduanne/oracle_pdb_ass_II_29398_MUHIMPUNDU/blob/d3d740b05880ee4fae6b5d738a86376c93a2d919/PL_SQL_PDB/PL_PDB_SWITCH_TO_PDB_ROOT_9.png)
 
       PDB creation
       
![Image Alt](https://github.com/muhimpunduanne/oracle_pdb_ass_II_29398_MUHIMPUNDU/blob/caaeb6d1f7489c94bbb77b68d22fecace076d67d/PL_SQL_PDB/PL_PBD_CREATION_OF_THE_DELETE_PDB_10.png)
     
      PDB deletion Commands and results must be visible
     
![Image Alt](https://github.com/muhimpunduanne/oracle_pdb_ass_II_29398_MUHIMPUNDU/blob/0cc6276d3a698c03e7734cb08b00ffe1544ccfe4/PL_SQL_PDB/PL_PDB_DELETION_OF_THE_PDB_TO_DELETE_14.png)

Task 3: Oracle Enterprise
-
in this task 3 i opened and open the OEM(Oracle Enterprise Manager) as the localhost and i logged in using the "System" as Username and "Password" and i entered the name of my container as "mu_pdb_29398"



