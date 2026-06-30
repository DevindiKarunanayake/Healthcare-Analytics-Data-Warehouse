# 🏥 Healthcare Data Warehouse & Business Intelligence Solution

The **Healthcare Data Warehouse** is a SQL Server–based Business Intelligence solution developed to support analytical reporting and healthcare performance analysis. The project demonstrates how operational healthcare data can be integrated, transformed, and loaded into a dimensional data warehouse to enable OLAP analysis, reporting, and business intelligence applications.

The solution combines SQL Server databases, SSIS ETL processes, SSAS multidimensional cubes, Power BI dashboards, and Excel-based OLAP analysis to provide a complete end-to-end BI implementation.

---

# 🔗 Project Overview

The project models a complete data warehousing and business intelligence architecture for healthcare analytics and decision support.

Operational and external data sources are integrated through ETL processes and loaded into a dimensional data warehouse optimized for analytical workloads.

The solution includes:

- Source databases and external flat-file data sources
- Staging area for data integration and transformation
- Dimensional data warehouse using a star schema
- Slowly Changing Dimension (SCD Type 2) implementation
- SSIS ETL packages for data extraction and loading
- SSAS multidimensional cube for OLAP analysis
- Excel-based OLAP operations
- Interactive Power BI dashboards and reports

---

# 🏗 Architecture

The project follows a layered data warehousing architecture:

```
Data Sources
      ↓
MedicalCenter_DB + Insurance Flat File
      ↓
Staging Layer (MedicalCenter_Staging)
      ↓
Data Warehouse (MedicalCenter_DW)
      ↓
SSAS Cube
      ↓
Power BI & OLAP Analysis
```

---

# 📊 Data Sources

The solution integrates heterogeneous data sources including:

### SQL Server OLTP Database

- Patients
- Doctors
- Clinics
- Appointments
- Payments
- Treatments
- Prescriptions
- Staff

### External Flat File

Patient insurance information containing:

- Insurance Status
- Insurance Provider
- Coverage Level

---

# ⭐ Data Warehouse Design

The dimensional model follows a **Star Schema** design optimized for analytical workloads.

### Fact Table

- FactAppointments

### Dimension Tables

- DimPatient
- DimDoctor
- DimClinic
- DimDate
- DimStaff

The **DimPatient** dimension is implemented using **Slowly Changing Dimension Type 2 (SCD Type 2)** to preserve historical changes.

---

# 🔄 ETL Pipeline

The ETL process was implemented using SQL Server Integration Services (SSIS).

### Source → Staging

Data extraction from:

- SQL Server Database
- Flat File Sources

### Staging → Data Warehouse

Transformation using:

- Lookup Transformations
- OLE DB Commands
- Stored Procedures

Loading:

- Dimension tables
- Fact tables
- Historical records

---

# 🧊 SSAS Cube Implementation

SQL Server Analysis Services (SSAS) was used to create a multidimensional cube that supports fast aggregation and OLAP analysis.

Implemented features include:

- Measure groups
- Dimensions
- Hierarchies
- Cube processing
- Cube browsing

---

# 📈 OLAP Operations

OLAP analysis was performed through Excel connected to the SSAS Cube.

Supported operations include:

- Roll-Up
- Drill-Down
- Slice
- Dice
- Pivot

These operations enable users to analyze healthcare information from multiple perspectives.

---

# 📉 Power BI Reports

Interactive reports were developed using Power BI.

Implemented reports include:

### Matrix Visual

Compare appointment counts across doctors and years.

### Multiple Slicers with Cascading Filters

Dynamic filtering using:

- Clinic Type
- Doctor Name

### Drill-Down Analysis

Navigate from:

```
Year → Month
```

### Drill-Through Reports

Detailed information for individual doctors.

### DAX Measures

KPIs include:

- Total Appointments
- Total Patients
- Average Processing Time

---

# 🛠 Technologies Used

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)
- SQL Server Integration Services (SSIS)
- SQL Server Analysis Services (SSAS)
- SQL Server Data Tools (SSDT)
- Power BI
- Excel
- SQL
- DAX

---

# 📚 Concepts Demonstrated

- Data Warehousing
- ETL Development
- Star Schema Design
- Slowly Changing Dimension Type 2
- OLAP Operations
- SSAS Cubes
- Power BI Reporting
- Dimensional Modeling
- Business Intelligence
- Healthcare Analytics


