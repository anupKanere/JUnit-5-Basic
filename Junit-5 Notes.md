# Dependencies Required

- junit-jupiter-engine

  - APi for writing tests using Junit Jupiter

- junit-jupiter-api

  - Implementation of the testEngine API for JUnit Jupiter

- junit-vintage-api
  A thin layer on the top of Junit 4 to allow running vintage tests

# Annotations

- @Test

  - Marks the metthod as a test
  - Informs the Junit engine what methods need to run

- @TestInstance
  - In JUnit 5, the @TestInstance annotation is used to configure the lifecycle of test instances in a test class. By default, JUnit 5 creates a new instance of the test class for each test method. However, with the @TestInstance annotation, you can customize this behavior and control how test instances are managed.
    JUnit 5 provides three lifecycle modes for test instances:
    1) PER_CLASS:

        In this mode (TestInstance.Lifecycle.PER_CLASS), a single instance of the test class is created for all test methods in the class. This means that the same instance of the test class is reused for the entire test class, and setup and cleanup methods annotated with @BeforeAll and @AfterAll are executed only once.

    2) PER_METHOD:

        In this mode (TestInstance.Lifecycle.PER_METHOD, which is the default), a new instance of the test class is created for each test method. This ensures that the state of the test class is isolated between test methods.

    3) PER_CONSTRUCTION:

        This mode (TestInstance.Lifecycle.PER_CONSTRUCTION) is an experimental mode where a new instance is created for each test method but without invoking @BeforeEach and @AfterEach methods. It is not recommended for general use and is considered experimental.   

# Notes

    - if want to run the test cases using maven commands  then use surefire plugins.(add this dependencies in pom.xml)

# LifeCycle hooks:

- @BeforeAll
- @AfterAll
- @BeforeEach
- @AfterEach

-for using @BeforeAll and @AfterAll the methods must be static because these methods will run before creating the instance of our test class.
