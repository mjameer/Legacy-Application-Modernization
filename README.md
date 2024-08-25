### Legacy Application Modernization 

Many critical applications within our projects are over a decade old and have no build, CI/CD, automated Unit testing, Sonar, and TRO integration implemented. Several such applications must be available round the clock for the customer's reference and from time to time, the application team ended up fixing performance and TRO issues caused by bad code or by using vulnerable libraries and there were several application outages, post deployments due to missing runtime components, configuration, and source code, which caused several production deployment failures. 

![image](https://github.com/user-attachments/assets/df256d98-9379-45c2-a450-5c622d8b14d2)


This idea aids in converting all legacy applications to Maven-based build projects which are committed in Git and created a reusable Jenkins build pipeline via which he implemented all of the CI/CD process that includes build, unit testing, Sonar scanning, TRO scanning(Nexus, Whitehat SATS & DATS) and effective deployment/rollback tracker with the help of Artifactory. 
Via this process, all such legacy applications have been adapted to modern standards and this process helped to slash down the time taken to build and deploy the application binary and bring down the number of post-deployment failures due to missing components/configurations, code defects, Duplicate code, and TRO issues.


### Solution Provided

I adopted a legacy application modernization approach that integrated various processes ranging from Mavenizing the application to implementing CI/CD process using Jenkins, Unit testing, TRO scanning(via Nexus, Whitehat DATS, and SATS), Sonar, Artifactory integration, established Git as a proper version control management tool via automated release process and provided an approval and Rollback step in Jenkins to deploy artifacts to production.
### Technologies Used

- Maven
- Jenkins - Declarative pipeline 
- Junit
- Sonar
- Nexus
- Whitehat
- Artifactory
- Git
- UCD - Urban code deployer
- WAS to Liberty Migration 

This process was created as a reusable asset that can be used across multiple applications in other projects. 

###  Why is it a problem worth solving?

There are lots of critical applications within our projects that are over a decade old and have no build, CI/CD, automated Unit testing, Sonar, and TRO integration implemented. Several such applications must be available round the clock for the customer's reference and from time to time, the application team ended up fixing performance and TRO issues caused by bad code or by using vulnerable libraries and there were several application outages, post deployments due to missing runtime components, configuration, and source code, which caused several production deployment failures. 

This process listed would eliminate all of the above problems. 

Also, this process pays way for migrating applications from IBM WAS to IBM Liberty 

### Why Migrate Application to Liberty

We tend to migrate applications to Liberty due to the following reasons.
- Even with the highest version of WAS, it only supports up to Java 8.
- For now, IBM has no plan to enhance it further. So, if Java 8 becomes out of complaint, then eventually you may need to choose another app server. Refer here on [IBM decommission plan](https://www.ibm.com/support/pages/verify-java-sdk-version-shipped-ibm-websphere-application-server-fix-packs).
- Just so you know, WAS is not supported in AKS architecture, it can be used only in traditional VM. Refer here for more info -> [Solutions to run WAS/Liberty in Azure](https://learn.microsoft.com/en-us/azure/developer/java/ee/websphere-family)

![image](https://github.com/mjameer/Legacy-Application-Modernization/assets/11364104/28c32edf-34d7-431f-84a6-4a94778ecde4)

Refer more on [Guide to Migrate Java application from WAS to Liberty](https://medium.com/@mj_ameer/guide-to-migrate-java-applications-from-was-to-liberty-129cfff9d31d)

### What are the benefits to the Customer if this idea is implemented?*

This process aids in keeping the application code in alignment with modern standards, this way it would be easier to upgrade the code during any migration such as the java/OS/app server’s version upgrade. 
Also, this process helps to slash down the time taken to build and deploy the application binary and bring down the number of post-deployment failures due to missing components/configurations, code defects, and Duplicate code and also brings down the number of vulnerabilities associated with bad library within the code.  

### How I came up with this idea*

The projects I worked for had lots of legacy applications, and we faced frequent deployment failures from time to time due to missing components/configurations, code defects, and sometimes we had performance issues post-deployment due to Duplicate code, numerous numbers of sonar defects, or bad code. During the vulnerability breaches such as Equifax, Log 4j 1.x issues, we faced multiple challenges upgrading our code immediately. 

With this process improvement, we modernized over 60+ applications, which slashed the post-deployment issues a lot, and the code became more standard due to sonar integration and the application became less vulnerable as we integrated sonar, whitehat, and nexus to monitor for vulnerable code and library. 





