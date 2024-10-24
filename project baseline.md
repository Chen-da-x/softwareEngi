## Requirement baseline
The requirement baseline defines the core functions and requirements of the project, ensuring that project development revolves around these requirements, and any changes require approval

1. API documentation generation

  - The tool can automatically extract API information from comments or code structures and generate documentation that complies with OpenAPI standards (supporting JSON and YAML formats).
  - The generated document should include:
    API endpoint description
    Request parameters (including type, mandatory, default values, etc.)
    Response format and status code
    Error messages and examples
  - Support document version management and historical archiving of different API versions.
  - Capable of generating local HTML documents for developers to browse, and also supports integration into CI/CD to generate online documents.

2. Automatic testing

  - Support automated testing functionality for API interfaces, capable of generating test cases automatically based on API documentation.
  - Provide the following testing functions:
    Verification of normal response
    Boundary condition testing
    Error handling testing
  - Support writing custom test scripts, allowing users to expand test cases according to their needs.
  - Automatically generate test reports, which should include information such as test coverage, pass rate, and details of failed cases.

3. CI/CD integration

  - The tool can seamlessly integrate into existing CI/CD pipelines, supporting automatic triggering of API document generation and automated testing.
  - Automatically generate documentation and run tests when there are updates or API changes in the code repository.

4. User interface
    -Provide a simple and intuitive user interface that allows users to manage API document generation, view test results, and customize test configurations.

5. Acceptance criteria

  - The generated API documentation complies with OpenAPI standards and can be correctly parsed by third-party tools.
    The testing tool can automatically generate at least 80% of test cases, with a testing coverage rate of over 90%.
  - CI/CD integration has passed testing, and documents and test reports can be automatically generated and accurate.

## Progress baseline
The progress baseline specifies the schedule and milestones of the project at each stage, helping the team track progress and promptly identify potential delays.

Project duration: 12 weeks

- week 1:

  - Complete project requirement analysis and technology selection.

  - Determine the technical solution for generating API documentation (such as whether to use Swagger or other tools).
  - Complete project prototype design, clarify tool interface and workflow.

- week 2-5: Sprint1

  - Development of API documentation generation module:
    - Implement API annotation parsing and document generation logic.
    - Supports OpenAPI standard JSON and YAML format output.
    - Complete local document generation and version control functions.
  - Preliminary integration of CI/CD. Implement automated document generation process.

- week 6-9: Sprint2

  - Integration and optimization:
    - Seamless integration of API documentation generation and automated testing modules.
    - Support the complete document generation and testing execution process in the CI/CD pipeline.
    - Optimize the performance of the tool to improve processing speed and response time.

- week 10-12:

  - Testing and Release:
    - Complete functional and performance testing of the project.
    - Fix all bugs and prepare to release the version.
    - Submit documents and ultimately release deliverables.

- Key milestones:

  - End of week 1: Requirement analysis and technical selection completed, prototype design passed review.
  - End of week 5: API documentation generation function development completed, preliminary CI/CD integration testing passed.
  - End of week 10: Integration completed, generation and testing performance passed.
  - End of week 12: Project delivery, final release completed.

## Performance baseline

The performance baseline defines the minimum performance requirements of the project and serves as a reference for subsequent optimization. 

1. Performance baseline for document generation
   - Document generation time: In large API projects (with over 100 endpoints), the tool can generate complete API documents (in JSON and YAML formats) within 5 seconds.
   - Concurrent processing capability: In the case of generating 10 API document requests concurrently, the response time of the tool should be less than 10 seconds and should not cause a significant decrease in system performance.
   - Document size optimization: The generated API documentation should be as concise as possible, but complete. Compared to the size of the document, the generated document should be within 5MB and support compressed storage.
     Automated testing performance baseline
2. CI/CD performance baseline
   - Integration efficiency: In the CI/CD pipeline, the completion time for API documentation generation and automated testing after each code submission should not exceed 10 minutes, even with 100 API endpoints.
   - System resource utilization: When generating documents and executing tests, the CPU usage of the tool should be below 50%, and the memory usage should be controlled within 1GB.