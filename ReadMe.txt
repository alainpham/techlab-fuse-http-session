techlab-fuse-http-session
=========================================

This project shows how to deal with soap services call that requires a first authentication step.
The key element here is getting the Set-Cookie from the first call (for authentication)
and set the header "Cookie" for the next service call to the real service.
This allows to set the JSESSIONID so that the server knows whether the caller has an authenticated session running.

The server here is mocked to require a first authentication step before allowing the
caller to access the real data service.

To build this project use

    mvn install

To run the project you can execute the following Maven goal

    mvn camel:run

For more help see the Apache Camel documentation

    http://camel.apache.org/


Go to browser and access : 
	http://localhost:7125/ok       -> to see a working example where authentication is successful
	http://localhost:7125/ko       -> to see a working example where authentication fails and access is denied