# What is this?

This is a spring cloud config server for the [limits service found here](https://github.com/Step-henC/limits-service-spring-cloud-client). Config servers provide external [configuration in a distributed system](https://docs.spring.io/spring-cloud-config/docs/current/reference/html/).
This spring config server is for tutorial learning purposes.

## Cool, so How do I run this?

A spring cloud config **requires** external, configuration `.properties` file committed to git.  

Once you clone this repository, on your local machine, create a separate folder *outside* of the project's folder directory. So if in spring-cloud-config-server-limits do the following command line args:

  1. `cd ..`
  2. `mkdir git-cloud-profile`
  3. `touch limits-service.properties`
  4. Open limits-config folder in the code editor of your choice. If VS Code type: `code .`
  5. In the code editor, add the following properties:
       - `limits-service.minimum=4`
       - `limits-service.maximum=996`
  6. In the folder directory type in command line:
       - `git init`
       - `git add .`
       - `git commit -m "added external config to git"`
  7. Initialize this cloud config server as well with the same commands
  8. This will allow this cloud config server to read the properties in the properties file.
  ### Bonus : 
    to have fun with different environments, ie. dev and qa, you can repeat steps 3-5 by changing the file name to limits-service-dev.properties and limits-service-qa.properties

  ## Key Takeaways
    - The properties file has the same name as the client service
    - The properties themselves are the same name as the client with dot properties (minimum and maximum) that are serialized as POJO object properties in the client
    - The properties file must be initialized in git
    
