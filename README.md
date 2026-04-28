## Phase 2: JMeter Performance Testing

### Task 1: GUI Testing Results
Below are the screenshots of the JMeter GUI Summary Reports for each endpoint before optimization.

**Endpoint: `/all-student`**
![GUI All Student](src/assets/images/all-studentSummaryReport.jpeg)

**Endpoint: `/all-student-name`**
![GUI All Student Name](src/assets/images/all-student-nameSummaryReport.jpeg)

**Endpoint: `/highest-gpa`**
![GUI Highest GPA](src/assets/images/highest-gpaSummaryReport.jpeg)

### Task 2: CLI Testing Results
Below are the screenshots of the command-line interface execution for the JMeter test plans.

**Endpoint: `/all-student`**
![CLI All Student](src/assets/images/cli-all-student.jpeg)

**Endpoint: `/all-student-name`**
![CLI All Student Name](src/assets/images/cli-all-student-name.jpeg)

**Endpoint: `/highest-gpa`**
![CLI Highest GPA](src/assets/images/cli-highest-gpa.jpeg)

---

## Phase 3: Profiling & Optimization

### Task 3 & 4: Before and After Comparison

**1. `getAllStudentsWithCourses` (`/all-student`)**
* **Before Optimization:** 5,936 ms  
  ![Before Optimization](src/assets/images/getAllStudent-before-opt.jpeg)
* **After Optimization:** 806 ms  
  ![After Optimization](src/assets/images/getAllStudent-after-opt.jpeg)
* **Improvement:** Reduced CPU execution time by 5,130 ms, achieving an **86.42%** improvement.

**2. `/all-student-name`**
* **Before Optimization:** 593 ms  
  ![Before Optimization](src/assets/images/all-student-name-before-opt.jpeg)
* **After Optimization:** 182 ms  
  ![After Optimization](src/assets/images/all-student-name-after-opt.jpeg)
* **Improvement:** Reduced CPU execution time by 411 ms, achieving a **69.31%** improvement.

**3. `/highest-gpa`**
* **Before Optimization:** 182 ms  
  ![Before Optimization](src/assets/images/highest-gpa-before-opt.jpeg)
* **After Optimization:** 126 ms  
  ![After Optimization](src/assets/images/highest-gpa-after-opt.jpeg)
* **Improvement:** Reduced CPU execution time by 56 ms, achieving a **30.77%** improvement.

---

## Phase 4: Reflection

**1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?**
> JMeter is used to test how the system performs under load (response time, throughput), while IntelliJ Profiler is used to analyze the code and find which parts are slow.

**2. How does the profiling process help you in identifying the weak points of your application?**
> Profiling shows which methods or parts of the code take the most time or resources, so it helps find bottlenecks easily.

**3. Do you think the IntelliJ Profiler is effective in helping you find bottlenecks in your application's code?**
> Yes, it is effective because it clearly shows which methods are slow and helps focus optimization on those parts.

**4. What were the main challenges you faced when doing performance testing and profiling, and how did you overcome them?**
> Challenges include finding the real bottleneck and simulating real conditions. This can be solved by using both JMeter and profiler together and testing multiple times.

**5. What are the main benefits you get from using JMeter and IntelliJ Profiler in the software development process?**
> It helps analyze CPU and memory usage, find slow methods, and understand how the program runs internally.

**6. How do you handle situations where the results from profiling with IntelliJ Profiler are not
entirely consistent with findings from performance testing using JMeter?**
> If results are different, I re-run tests, check the environment, and compare both tools to understand the issue better.
 
**7. What strategies do you implement in optimizing application code after analyzing results
from performance testing and profiling? How do you ensure the changes you make do
not affect the application's functionality?**
> I optimize by reducing unnecessary queries, improving code efficiency, and using better data handling. To ensure functionality, I test the application and compare results before and after optimization.