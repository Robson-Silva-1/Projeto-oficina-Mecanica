# Projeto-oficina-Mecanica
Projeto do curso de Database Experience lecionado por juliana

##Criação do banco de dados para o cenario da oficina mecanica
  Create database Oficina_Mecanica;
  Use Oficina_mecanica;
  ## Criar Tabela Cliente
  Create Table Client(
       IdClient Int Auto_increment Primary Key,
       IdCar_repair Int,
       IdCar_review Int,
       Pname varchar(10),
       Minit Varchar(15),
       Lname Varchar(10),
       Adress Varchar(45),
       Contact_Phone Varchar(11),
       CPF Varchar(10) not null,
       Constraint UNique_CPF_Cliente unique(CPF),
       Birth_date Varchar(10)
);
## Criar Tabela Carro Revisão
Create Table Car_review(
       IdCar_review Int Auto_increment Primary Key,
       IdClient Int,
       Brand varchar(45),
       Model Varchar(45),
       Year Varchar(45)
);
## Criar Tabela Carro Conserto
Create Table Car_repair(
       IdCar_repair Int Auto_increment Primary Key,
       IdClient Int,
       Brand varchar(45),
       Model Varchar(45),
       Year Varchar(45)
);
## Criar Tabela Oficina mecanica
Create Table Mechanical_Workshop(
       IdMechanical_Workshop Int Auto_increment Primary Key,
	   IdClient Int,
       IdCar_repair Int,
       IdCar_review Int,
       IdMechanics_Team Int,
       Idservice_execution Int,
       Adress Varchar(45),
       CNPJ Varchar(10) not null,
       Contact_Phone Varchar(11),
       Charter Varchar(45),
       Corpoate_name vARCHAR(45)
);
## Criar Tabela Geração ordem de serviço
Create Table Mechanical_Workshop(
       IdMechanical_Workshop Int Auto_increment Primary Key,
       IdClient Int,
       IdCar_repair Int,
       IdCar_review Int,
       IdMechanics_Team Int,
       Idservice_execution Int,
       Adress Varchar(45),
       Contact_Phone Varchar(11),
       Kind_of_serive Varchar(45),
       Repair Varchar(45),
       Review varchar(45),
       Geometry Varchar(45),
       Balance Varchar(45)
);
## Criar Tabela equipe de mecanicos
Create Table Mechanics_Team(
       IdMechanics_Team Int Auto_increment Primary Key,
       IdMechanic_1 Int,
       IdMechanic_2 Int,
       IdMechanic_3 Int,
       Specialized_mechanics Varchar(45),
       Category Varchar(45)
);
## Criar Tabela Mecanico 1
Create Table Mechanic_1(
       IdMechanic_1 Int Auto_increment Primary Key,
       Pname varchar(10),
       Minit Varchar(15),
       Lname Varchar(10),
       Adress Varchar(45),
       Contact_Phone Varchar(11),
       CPF Varchar(10) not null,
       Constraint UNique_CPF_Cliente unique(CPF),
       Birth_date Varchar(10),
       Code Varchar(45),
       Specialty Varchar(45)       
       );
## Criar Tabela Mecanico 2
Create Table Mechanic_2(
       IdMechanic_2 Int Auto_increment Primary Key,
       Pname varchar(10),
       Minit Varchar(15),
       Lname Varchar(10),
       Adress Varchar(45),
       Contact_Phone Varchar(11),
       CPF Varchar(10) not null,
       Constraint UNique_CPF_Cliente unique(CPF),
       Birth_date Varchar(10),
       Code Varchar(45),
       Specialty Varchar(45)       
       );
## Criar Tabela Mecanico 3
Create Table Mechanic_3(
       IdMechanic_3 Int Auto_increment Primary Key,
       Pname varchar(10),
       Minit Varchar(15),
       Lname Varchar(10),
       Adress Varchar(45),
       Contact_Phone Varchar(11),
       CPF Varchar(10) not null,
       Constraint UNique_CPF_Cliente unique(CPF),
       Birth_date Varchar(10),
       Code Varchar(45),
       Specialty Varchar(45)       
       );
## Criar Tabela execução do serviço
Create Table service_execution(
       Idservice_execution Int Auto_increment Primary Key,
       Repair Varchar(45),
       Review varchar(45),
       Geometry Varchar(45),
       Balance Varchar(45)
);
## Criar Tabela Tabela de mão de obra
Create Table Labor_table(
       Idlabor_Table Int Auto_increment Primary Key,
       Value_repair Varchar(45),
       Value_review Varchar(45),
       Value_Geometry Varchar(45),
       Value_Balance varchar(45),
       Value_specialist Varchar(45),
       Value_Part Varchar(45)
);
    ## Criar Tabela Ordem de entrega
    Create Table Delivery_order(
       IdDelivery_order Int Auto_increment Primary Key,
       Total_repair Varchar(45),
       Total_review Varchar(45),
       Total_Geometry Varchar(45),
       Total_Balance varchar(45),
       Total_specialist Varchar(45),
       total_Part Varchar(45)
);

