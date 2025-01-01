# **Module 14: Completing BREAD for Calculations and Final Project**

## **Module Overview**

In **Module 14**, you will finalize your **BREAD (Browse, Read, Edit, Add, Delete)** functionality for calculations on the front end—tying it together with your JWT-secured back end. Additionally, you will implement a **final project feature** that extends beyond basic login and calculations. This feature will require **unit, integration, and end-to-end (E2E) testing** and be deployed to Docker Hub through your existing CI/CD pipeline. Optionally, you may incorporate **Alembic** for database migrations if your final feature modifies the schema.

By the end of this module, you will submit a **fully functional, secure, tested, and containerized** Python web application as your final deliverable.

### **Relevant Course Learning Outcomes (CLOs)**

- **CLO 3:** Create Python applications with automated testing.  
- **CLO 4:** Set up GitHub Actions for Continuous Integration (CI), automating tests and Docker builds to demonstrate DevOps principles.  
- **CLO 10:** Apply containerization techniques to containerize applications using Docker.  
- **CLO 11:** Create, consume, and test REST APIs using Python.  
- **CLO 12:** Integrate Python programs with SQL databases to create and manipulate data.  
- **CLO 13:** Serialize, deserialize, and validate JSON using Python with Pydantic.  
- **CLO 14:** Utilize best practices for software development security by implementing secure authentication and authorization techniques, including encryption, hashing, and encoding.

---

## **Why Complete BREAD and Add a New Feature Now?**

1. **Comprehensive Scope**: Ensuring full BREAD for calculations completes your core application functions, while the new feature showcases your ability to extend and innovate.  
2. **Mastery Demonstration**: Combining final touches on existing features with something entirely new (including all levels of testing) cements your skill set.  
3. **Optional Alembic**: Implementing migrations with Alembic (if needed) demonstrates professional DB update handling—useful if your new feature alters the data model.

---

## **Hands-On Assignment**

### **Part 1: Completing BREAD for Calculations**

- **Browse**: Display all calculations belonging to the logged-in user.  
- **Read**: (Optional) Provide a detailed view of a single calculation’s data.  
- **Edit**: Let users update calculation fields (operands, operation type) on the front end.  
- **Add**: Allow creation of a new calculation (choose operation, input operands, etc.).  
- **Delete**: Provide a straightforward way to remove a calculation.  

**Implementation Tips**:
- Continue using **JWT** for route protection.  
- Keep or refine your front-end validation (numeric checks).  
- Extend your Playwright E2E tests to cover these new BREAD interactions, focusing on **positive** and **negative** scenarios (e.g., invalid numeric input).

### **Part 2: Final Project Feature**

Beyond the BREAD functionality, add **one new feature** (or propose a similar scope). This feature must be tested at **unit**, **integration**, and **E2E** levels:

1. **User Profile & Password Change**  
   - Add a page or form to let users update profile info (username, email) or change passwords (hash new passwords).  
   - Test with unit (change logic), integration (DB updates), E2E (flow from login -> profile -> password change -> re-login).

2. **Additional Calculation Type**  
   - Introduce an advanced operation (exponentiation, modulus, or something custom).  
   - Update routes, Pydantic schemas, and the front-end UI.  
   - Write tests confirming correct logic (unit), route handling (integration), and front-end usage (E2E).

3. **Report/History Feature**  
   - Provide usage stats or summaries (e.g., total calculations, average operands).  
   - Implement routes/data storage, and show a small UI section with these metrics.  
   - Thoroughly test logic (unit), route (integration), and UI flow (E2E).

**(Alternative)**: If you have a different idea of comparable complexity (DB changes, new logic, UI integration), clear it with your instructor first.

### **Optional Alembic (Bonus)**

- If your final feature requires changes to the database schema (new columns/tables), consider using **Alembic** to generate and apply migrations.  
- Include instructions in your README on how to run these migrations (e.g., `alembic upgrade head`).

---

## **Testing Requirements**

All features must be tested at three levels:

1. **Unit Tests**  
   - Small, focused tests for your new logic or changed data model functions (e.g., new calculation method, user profile logic).

2. **Integration Tests**  
   - Confirm that your routes (FastAPI) interact correctly with the DB, ensuring any new or updated endpoints work as expected.

3. **E2E Tests (Playwright)**  
   - Extend or add new scenarios:  
     - Positive: Valid usage of the new feature plus the new BREAD interactions.  
     - Negative: Invalid inputs, unauthorized access, or erroneous states.  
   - All E2E tests should pass in your CI pipeline.

---

## **Deployment to Docker Hub**

- Maintain your **GitHub Actions** pipeline from previous modules.  
- On each commit or pull request, your pipeline will:
  1. Spin up DB + server, run all tests (unit, integration, E2E).  
  2. If green, push your final image to Docker Hub.  
  3. If using Alembic, consider adding a step to run migrations in your test environment.

---

## **Submission Requirements**

1. **GitHub Repository Link**  
   - Must include final BREAD code for calculations, your new feature, all relevant tests, and optional Alembic migrations.  
   - In **README**: 
     - Summarize how to run the full app, the tests, and (if applicable) the migration commands.  
     - Provide a link to your Docker Hub repository.

2. **Module 14 Reflection** (300–500 words)  
   1. **Front-End Integration**: How did finishing the BREAD UI + final feature shape your complete full-stack perspective?  
   2. **DevOps & Testing**: Discuss how you balanced unit, integration, and E2E tests for your final project.  
   3. **Security & Best Practices**: Note final approaches to JWT usage, user data protection, and advanced checks for your new feature.  
   4. **Challenges & Solutions**: Summarize any last hurdles (migrations, advanced feature logic, front-end complexities) and how you addressed them.

3. **Quiz** (on Canvas)  
   - **Multiple-Choice** and **Short-Answer** questions about finalizing your project, BREAD patterns, advanced features, potential Alembic usage, and comprehensive testing strategies.

---

## **Tips for Success**

1. **Design First**: Outline your new feature’s data model, routes, and front-end changes before coding.  
2. **Code Iteratively**: Complete BREAD, then build the new feature, adding tests at each level (unit -> integration -> E2E).  
3. **Consider Alembic**: If DB schema changes, demonstrate professional migrations.  
4. **Document Thoroughly**: This final version is your portfolio piece—be sure it’s well-structured, secure, and tested.

---

## **Submission Deadline**

All final deliverables (GitHub repo link, Docker Hub link, Reflection) are due by **[Insert Deadline Here]**. Late submissions may be subject to course policy.

---

**Congratulations!** You have built and enhanced a robust full-stack application, culminating in a final project feature that showcases advanced testing, security, and DevOps expertise. This end-to-end solution forms a powerful demonstration of your newly acquired Python web development skills.