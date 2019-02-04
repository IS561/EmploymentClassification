# Employment Classification
## Group 3: 
- Jiang Chang
- David Chanthabandith 
- Sayantan Dutta
- Pujeethaa Jakka
- Yi (Joy) Liang 
- Saxue Wang

## Entity Classes
- Employment Position
- Salary 
- Employer
- Employee
- Department
- Contract
- Policy

## Relationships
- Holds
- Determined by
- Pays
- Earns
- Equal or Greater Amount
- Hires
- Works For
- Has
- Issued By
- Hires For
- Seeks
- Is Agreed On 
- Includes
- Regulate

##  1. Employment Position

### Class description
* A relationship between two parties. Usually based on a contract where work is paid for, where one party is the employer 
  and the other is the employee. 
* Employment position refers to the type of employment. 
* In this case, we have 7 different employment types.

### Attribute
*  Employment Position ID
*  Employment Position Name 

##  2. Salary
### Class description
* A salary is a form of payment from an employer to an employee, which may be varied among different types of employment.

### Attribute
*  Salary Amount (Number)
*  Employment Position Name
*  Unit (per hour, per week, per month, per year)

##  3. Employer 

### Class description
* Harvard University is the employer of these employees.
* The employer employs an employee under a contract of employment and will pay an employee in salary or wages as 
  compensation for their work.
* The employer is responsible to practice safe employment practices, occupational safety, regulate wages, hours and 
  benefits.

### Attribute
*  Employer ID
*  Employer Name

##  4. Department  

### Class description
* The Department that an employee works for
* There are a variety of Departments that are under Harvard University.

### Attribute
*  Department ID
*  Department Name

##  5. Employee   

### Class description
* An individual who works regularly or temporarily under a contract of Harvard University. 
* An individual who provides labor to the University. 
* An individual get paid and benefits by Harvard University based on different positions. 

### Attribute
*  Working hours per week
*  Position duration
*  Title

##  6. Contract    

### Class description
* A contract is a legally-binding agreement which recognizes and governs the rights and duties of the employees and 
  Harvard University to the agreement.  
* An agreement typically involves the exchange of goods, services, money or promises of any of those. 
* A contract has a period which the employees are engaged to perform work from time to time.

### Attribute
*  Period
*  Form

##  7. Policy    

### Class description
* The policy is a non-contractual and legal document designed to provide guidance to Harvard University employees. 
* The policy communicate expectations of Staff and Temporary employees and support its compliance with laws and 
  regulations.  
* The policy specified the maximum working hours for student employees.

### Attribute
*  Maximum working hours
*  Working position
*  Type of employment

# Relationship
## 1.HOLDS
- Scope Note: Participation of an employee in an employment position
- Domain: Employee
- Codomain: Employment Position
- Arity:2
- Cardinality: 1-to-many 

## 2.DETERMINED BY
- Scope Note: Salary differs based on the employment position
- Domain: Salary		
- Codomain: Employment Position
- Arity: 2
- Cardinality:  1- to -1

## 3.PAYS
- Scope Note: Employer pays a certain amount of salary for someone who works for him.
- Domain:  Employer
- Codomain: Salary
- Arity: 2
- Cardinality:  many-to-many
- Remarks: Harvard University pays 20$ per hours for students who work for them.

## 4.EARNS
- Scope Note: Employee earns a certain amount of salary based on her/his working.
- Domain: Employee
- Codomain: Salary
- Arity: 2
- Cardinality:  1-to-1 
- Remarks: For example, Sam earns 50$ per hour as a regular employee.

## 5.EQUAL OR GREATER AMOUNT
- Scope Note: different amounts of salary have an asymmetric relationship
- Domain: Salary
- Codomain: Salary
- Arity: 2
- Cardinality:  many-to-many 
- Remarks: For example, 50$ per hour for regular employment is an equal or greater amount than 20$ per hour for student 
  employment.

## 6.HIRES
- Scope Note: Employee is recruited by an employer. 
- Domain: Employer
- Codomain: Employee
- Arity: 2
- Cardinality: many to many

## 7.WORKS FOR
- Scope Note: The department is the beneficiary of tasks performed by the employee. 
- Domain: Employee
- Codomain: Department
- Arity: 2
- Cardinality:  many to many

## 8.HAS
- Scope Note: Department has multiple employment positions
- Domain: Department
- Codomain: Employment Position
- Arity: 2
- Cardinality:  1 to many

## 9.ISSUED BY
- Scope Note: Salary is issued by the department
- Domain: Salary
- Codomain: Department
- Arity: 2
- Cardinality:  1 to 1

## 10.EMPLOYS
- Scope Note: A Department employs an employee for the Employer, which is Harvard University.
- Domain: Department
- Codomain: Employer 
- Arity: 2
- Cardinality:  1 to 1

## 11.SEEKS
- Scope Note: A Department seeks a qualified candidate to become an employee.
- Domain: Department
- Codomain: Employee 
- Arity: 2
- Cardinality:  1 to many

## 12.IS AGREED ON
- Scope Note: Contract states the amount of salary agreed upon. 
- Domain: Salary
- Codomain: Contract 
- Arity: 2
- Cardinality:  1 to 1

## 13.INCLUDES
- Scope Note: Employment position is stated in the contract.
- Domain: Contract
- Codomain: Employment Position
- Arity: 2
- Cardinality:  1-to-1

## 13.REGULATE
- Scope Note: Policy regulate and limit the working status of an employee
- Domain: Policy
- Codomain: employee
- Arity: 2
- Cardinality: 1-to-many

## 14.GUIDE
- Scope Note: Policy is to provide guidance for contract
- Domain: Policy
- Codomain: Contract
- Arity: 2
- Cardinality: 1-to-1  

 


