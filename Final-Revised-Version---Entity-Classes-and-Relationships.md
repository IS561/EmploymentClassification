# Entity Classes

**1. Employment Type**

Class description:
* A classification of employment one falls under, based on HR policy, like a regular, temporary, intern, etc. 

Attribute
* Employment Type ID
* Employment Type Name

**2. Employment Position**

Class description: 
* This relates to the position the employee holds like for eg. Manager, Professor, Accountant etc.

Attribute
* Employment Position ID
* Employment Position Name 

**3. Appointment**

Class description: 

The act of an employee holding a specific position. This is different than employment position as an instance of position will continue to exist as long as the department offers it. An instance of appointment exists only as long as an employee occupies a position. 

Attributes:

* EmployeeName
* PositionName
* Salary
* TimeLength
* TimeUnit (hours,months, years)

**4. Department**

Class description

* The Department that an employee works for
* There are a variety of Departments that are under Harvard University.

Attribute

* Department ID
* Department Name

**5. Employee**

Class description

* An individual who works regularly or temporarily under a contract of Harvard University.
* An individual who provides labor to the University.
* An individual get paid and benefits by Harvard University based on different positions.

Attribute

* Working hours per week
* Position duration
* Title

**6. Time Employed**

Class description

* Amount of time an employee has been employed by the university in the prior fiscal year. For example, John has been employed by the university in 9 months out of the prior fiscal year. 

Attributes

* TimeLength
* Unit (hours, months, years)

**7. Student**

Class description

* An individual who is taking classes and progressing towards a degree at the university. 

Attributes

* Name
* Age
* University name 

**8. Cooperative & Intern program**

Class description

* An on-job training program that must be fulfilled for successful completion of certain degrees. 

Attributes

* Program Name

**9. Policy**  

Class description

* The policy is a non-contractual and legal document designed to provide guidance to Harvard University employees. 
* The policy communicate expectations of Staff and Temporary employees and support its compliance with laws and 
  regulations.  
* The policy specified the maximum working hours for student employees.

Attribute

*  Maximum working hours
*  Working position
*  Type of employment

# Relationships

**1.Holds**

Scope Note: Participation of employees in different employment positions. 

Domain: Employee. 

Codomain: Employment Position. 

Arity:2. 

Cardinality: many-to-many

**2.Managed by**

Scope Note: To determine concurrent employment. 

Domain: Employee. 

Codomain: Department. 

Arity: 2. 

Cardinality: many to many

**3.Has**

Scope Note: An employee has a type of employment at the university. 

Domain: Employee. 

Codomain: Employment 

Type. Arity: 2. 

Cardinality: many-to-1

Remarks:

* Many employees can have one employment type
* One employee can have only one employment type

**4. Filled by**

Scope Note: When an employment position has been assigned an appointment. 

Domain: Employment Position. 

Codomain: Appointment. 

Arity: 2. 

Cardinality: 1-to-many

Remarks:

* An instance of position can have many appointments over time
* An instance of appointment can only be made to one position

**5. Is replacing**

Scope Note: Whether an employee is replacing a regular employee on temporary leave. 

Domain: Employee. 

Codomain: Employee. 

Arity: 2. 

Cardinality: 1-to-1

Remarks:

* One employee is temporarily replacing another employee

**6.Employed for in prior fiscal year**

Scope Note: Amount of time an employee is employed by the university in the prior fiscal year. 

Domain: Employee. 

Codomain: Time Employed. 

Arity: 2. 

Cardinality: many-to-1

Remarks:

* Many employees can be employed for the same amount of time
* One employee can only be employed for one amount of time

**7.Is also**

Scope Note: When an employee is also a student at the university. 

Domain: Employee. 

Codomain: Student. 

Arity: 2. 

Cardinality: 1-to-1

Remarks:

* An employee can be a student
* A student can be an employee

**8. Is a part of**

Scope Note: Student is a part of a program that would make him/her a co-op or an intern student. 

Domain: Student. 

Codomain: Cooperative & Intern program. 

Arity: 2. 

Cardinality: many-to-1

Remarks:

* Many employees can be part of a co-op program
* An employee can only belong to one co-op program

**9. Impacts**

Scope Note: The duration of Appointment changed impacts employment type.  

Domain: Appointment. 

Codomain: Employment Type. 

Arity: 2. 

Cardinality: many-to-1

Remarks:

* An appointment can belong to one employment type
* An employment type can have many appointments 

**10. Determines**

Scope Note: If a student is a Harvard student, then his/her employment type is student employment. 

Domain: Student. 

Codomain: Employment type. 

Arity:2. 

Cardinality: 1-to-many

**11. Adheres to**

Scope Note: Policy associated with an Employee. 

Domain: Employee. 

Codomain: Policy. 

Arity: 2. 

Cardinality: many-to-1

Remarks: Many employees adhere to one policy.