# financial_management_system
practice project to increase your java skills using lambdas
### Financial Management System Ticket Breakdown

**Ticket 1: Create Employee Model**

**Description:** Define the `Employee` class with fields for `id`, `name`, `salary`, `position`, `department`, and `hourly_rate`.

**Tasks:**
1. Create the `Employee` class.
2. Add fields for `id`, `name`, `salary`, `position`, `department`, and `hourly_rate`.
   - **Hint:** Use `int` for `id`, `String` for `name`, `position`, and `department`, `double` for `salary` and `hourly_rate`.
3. Implement getter methods for each field.
4. Implement a `toString` method to display employee details.

**Ticket 2: Implement CSV Reader**

**Description:** Implement the `CSVReader` class to read employee data from a CSV file and populate a list of `Employee` objects.

**Tasks:**
1. Create the `CSVReader` class.
2. Implement the `readEmployeesFromCSV` method using `BufferedReader` to read from the CSV file.
   - **Hint:** Example method signature: `public static List<Employee> readEmployeesFromCSV(String file)`.
3. Parse the CSV file and create `Employee` objects.
   - **Hint:** Use `String.split(",")` to split each line into values.
4. Return a list of `Employee` objects.
   - **Hint:** Use `ArrayList<Employee>` to store the employees.
5. Handle any necessary exceptions.
   - **Hint:** Use `try-with-resources` for `BufferedReader`.

**Ticket 3: Implement CSV Writer**

**Description:** Implement the `CSVWriter` class to write employee data to a CSV file from a list of `Employee` objects.

**Tasks:**
1. Create the `CSVWriter` class.
2. Implement the `writeEmployeesToCSV` method using `BufferedWriter` to write to the CSV file.
   - **Hint:** Example method signature: `public static void writeEmployeesToCSV(List<Employee> employees, String file)`.
3. Format the employee data for CSV output.
   - **Hint:** Use `String.format` to create CSV lines.
4. Handle any necessary exceptions.
   - **Hint:** Use `try-with-resources` for `BufferedWriter`.

**Ticket 4: Implement Financial Operations**

**Description:** Implement `FinancialOperations` class with methods for financial operations using both traditional and streams-based approaches.

**Tasks:**
1. Create the `FinancialOperations` class.
2. Implement `getHourlyRateSum` method using streams.
   - **Hint:** Example method signature: `public static double getHourlyRateSum(List<Employee> employees)`.
   - **Hint:** Use `mapToDouble` and `sum` methods.
3. Implement additional operations using streams:
   - **Hint:** `public static double sumDepartmentSalary(List<Employee> employees, String department)`.
     - Use `filter` and `mapToDouble`.
   - **Hint:** `public static double getAverageSalaryByDepartment(List<Employee> employees, String department)`.
     - Use `filter` and `mapToDouble`.
   - **Hint:** `public static double sumDepartmentHourlyRate(List<Employee> employees, String department)`.
     - Use `filter` and `mapToDouble`.
   - **Hint:** `public static double getAverageHourlyRateByDepartment(List<Employee> employees, String department)`.
     - Use `filter` and `mapToDouble`.
   - **Hint:** `public static Map<String, Double> getTotalSalaryByDepartment(List<Employee> employees)`.
     - Use `Collectors.groupingBy` and `Collectors.summingDouble`.
   - **Hint:** `public static Map<String, Double> getAverageSalaryByDepartment(List<Employee> employees)`.
     - Use `Collectors.groupingBy` and `Collectors.averagingDouble`.
   - **Hint:** `public static Map<String, Double> getTotalHourlyRateByDepartment(List<Employee> employees)`.
     - Use `Collectors.groupingBy` and `Collectors.summingDouble`.
   - **Hint:** `public static Map<String, Double> getAverageHourlyRateByDepartment(List<Employee> employees)`.
     - Use `Collectors.groupingBy` and `Collectors.averagingDouble`.
     - **Hint:** `public static int getNumSum(int number)`.
     - Use `Helper method for getSumOfEmployeeIdDigits (no lambda needed) `.
     -  **Hint:** `public static int getSumOfEmployeeIdDigits(List<Employee> employees)`.
     - Use `mapToInt` and `map(use helper function here) and sum`.

**Ticket 5: Create Main Class**

**Description:** Implement the `Main` class to demonstrate the functionality of both traditional and streams-based financial operations.

**Tasks:**
1. Create the `Main` class.
2. Load employees from the CSV file using `CSVReader`.
   - **Hint:** Example method call: `List<Employee> employees = CSVReader.readEmployeesFromCSV("financial_management_system.csv")`.
3. Demonstrate the functionality of `FinancialOperations` methods using traditional approach.
   - **Hint:** Call the methods and print the results.
4. Demonstrate the functionality of `FinancialOperations` methods using streams.
   - **Hint:** Call the methods and print the results.
5. Write results to new CSV files using `CSVWriter`.
   - **Hint:** Example method call: `CSVWriter.writeEmployeesToCSV(employees, "output.csv")`.
   - **Hint:** Create a file for each department that includes all employees from that department: ` CSVWriter.writeEmployeesToCSV(hrEmployees, "output_hr_employees.csv");`.
