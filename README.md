# Data-Empresas-Luz-IIS 🔌

## Overview 📋
This SQL Server Integration Services (SSIS) project processes electrical company data from monthly Excel files and loads it into SQL Server databases. The project handles data migration for electrical consumption metrics across different regions.

## Project Structure 📂
```
Data-Empresas-Luz-IIS/
├── [Package.dtsx](Data-Empresas-Luz-IIS/Package.dtsx)       # Main SSIS package
├── [Package1.dtsx](Data-Empresas-Luz-IIS/Package1.dtsx)     # Data migration package
└── [Project.params](Data-Empresas-Luz-IIS/Project.params)   # Project parameters
```

## Data Sources 📊
The project processes Excel files containing monthly electrical data:
- February 2024 (`DatosCompartido202402.xlsx`)
- March 2024 (`DatosCompartidos202403.xlsx`)
- April 2024 (`DatosCompartido202404.xlsx`)
- May 2024 (`DatosCompartido202405.xlsx`)
- June 2024 (`DatosCompartido202406.xlsx`)

## Database Architecture 💾
The solution uses three databases:
- 

DB_Datos

 - Primary data storage

DB_DatosElectronorte

 - Electronorte specific data

DM_ConsumoEnergetico

 - Energy consumption data mart

## Data Model 🗃️
Key fields include:
- `NOMBRE_EMPRESA` (Company Name)
- `DEPARTAMENTO` (Department)
- `PROVINCIA` (Province)
- `DISTRITO` (District)
- `CARTERA` (Portfolio)
- `TARIFA` (Tariff)
- `FECHA_CONSUMO_DESDE` (Consumption Start Date)

## Technical Requirements 🛠️
- SQL Server 2019+
- SQL Server Integration Services
- Microsoft Excel ACE.OLEDB.12.0 Provider
- Visual Studio with SSIS Tools

## Connection Details 🔌
- Server: AN5-DS
- Connection Type: OLEDB
- Excel Source: Microsoft.ACE.OLEDB.12.0

## Development Team 👥
- Created by: AN5-DS\Sando
- Creation Date: 2024

## Version Information 📌
- Product Version: 16.0.5685.0
- Schema Version: 9.0.1.0

## Notes 📝
- All Excel files must have headers (HDR=YES)
- Data is processed with XML handling (EXCEL 12.0 XML)
- Package uses retry logic for robust data loading
