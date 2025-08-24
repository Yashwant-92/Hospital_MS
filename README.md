**project:**

  title: "🏥 Hospital Management System (HMS) with ICD-10 Integration"
  
  **description**: >
    A Java-based hospital management system that integrates ICD-10 (International Classification
    of Diseases) coding to standardize patient diagnoses and medical records.
    This project provides a structured approach to managing hospital data such as patients,
    doctors, appointments, and billing, while ensuring compliance with ICD-10 standards.

**summary:**
 **features:**
    - "👨‍⚕️ Manage patients, doctors, and staff records"
    - "📅 Book, update, and cancel appointments"
    - "🧾 Generate medical bills & reports"
    - "📊 Maintain patient medical history with ICD-10 diagnosis codes"
    - "🌐 Scalable design for integration with EHR systems"

**tech_stack:**
  - "☕ Java – Core Java (JDK 17+)"
  - "🗄️ MySQL – Database for storing hospital data"
  - "🔗 JDBC / Hibernate – Database connectivity"
  - "⚙️ Maven – Build and dependency management"
  - "📖 ICD-10 Dataset – Standard disease/diagnosis classification"

**project_structure:** |
  HospitalManagementSystem/
  
  ├── src/main/java/com/hms/
  
  │   ├── dao/             # Data Access Objects
  
  │   ├── model/           # Entities (Patient, Doctor, Appointment, ICDCode, Bill)
  
  │   ├── service/         # Business logic
  
  │   ├── util/            # Database utility, ICD-10 loader
  
  │   └── MainApp.java     # Entry point
  
  ├── resources/
  
  │   ├── application.properties
  
  │   └── icd10_codes.csv  # ICD-10 dataset
  
  ├── pom.xml
  
  └── README.md
  

**how_to_run:**
  prerequisites:
    - "JDK 17+"
    - "MySQL"
    - "Maven"
  
  **steps:**
    - "Clone the Project: git clone <repository-url>"
    - "Create Database:"
    - |
      ```sql
      CREATE DATABASE IF NOT EXISTS hospitalDB;
      USE hospitalDB;
      ```
    - "Import ICD-10 Dataset (CSV/SQL provided in resources/):"
    - |
      ```sql
      CREATE TABLE icd_codes (
          code VARCHAR(10) PRIMARY KEY,
          description VARCHAR(255) NOT NULL
      );
      -- Import ICD-10 codes here
      ```
    - "Update DB credentials in application.properties or HospitalUtility.java"
    - "Run MainApp.java from IDE"

**features:**
 ** core_hms:**
    - "➕ Add / Update / Delete patient records"
    - "🩺 Assign doctors & manage staff"
    - "📅 Appointment scheduling and cancellation"
    - "🧾 Bill generation with services & ICD-10 codes"
  
  **icd10_integration:**
    - "📖 Lookup disease codes while creating diagnosis"
    - "🔎 Search by code or description"
    - "🧩 Link patient medical history to ICD-10 codes"

**icd10_fields:**
  code: "String (e.g., A00.0) – ICD-10 Code"
  description: "String – Disease description (e.g., Cholera due to Vibrio cholerae 01)"
  patient_id: "Foreign key – Links diagnosis to patient"

**console_output**: |
  ========= HOSPITAL MANAGEMENT =========
  1. Add Patient
  2. View All Patients
  3. Search Patient by ID
  4. Book Appointment
  5. Add Diagnosis (ICD-10)
  6. Generate Bill
  7. Exit

  **Enter your choice:**

**learning_outcomes:**
  - "🏥 Understand healthcare informatics and ICD-10 usage"
  - "🗄️ Implement JDBC/Hibernate CRUD operations"
  - "🧩 Learn modular design with DAO, Service, Model layers"
  - "📖 Work with external datasets (ICD-10)"

**notes:**
  - "💻 Console-based project"
  - "🔄 Scalable to integrate with Spring Boot + REST APIs"
  - "📖 ICD-10 dataset can be updated with WHO releases"

**license:** "📜 This project is for educational purposes only."

**author**:
  name: "Your Name"
  role: "Java Developer | MCA Student | Enthusiastic Coder | Interested in Healthcare Tech"
