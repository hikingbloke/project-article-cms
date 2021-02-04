# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*

    - costs:
        - *Virtual Machine
            **more**: 
            https://azure.microsoft.com/pricing/details/virtual-machines/windows
            https://azure.microsoft.com/pricing/details/virtual-machines/linux
        - *App Service
            **more**: 
            https://azure.microsoft.com/pricing/details/app-service

    - calability:
        - *Virtual Machine scaling can be achieved by using Virtual machine scale sets(VMSS).
        - *App Service has Built-in service.        
        
        **more**: 
            https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree#scalability

    - availability:
        - Virtual Machine Connectivity to at least one instance is at least 99.95% of the time.
        - App Service is available 99.95% of the time.
        **more**: 
            https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree#availability

    - workflow:
   Upfront work on getting the webserver working, installing software and packages has been avoided by using App Service.
   Virtaul Machines and App Service deployments can both be automated.

- *Choose the appropriate solution (VM or App Service) for deploying the app*
My choice to implement the solution:  **App Service**:
https://flaskwebproject.azurewebsites.net/
	
- *Justify your choice*
I decided to implement the solution using App Service to leverage on its built in service capabilities like web hosting.
App Service is suitable for my solution because we do not have requirement for huge compute power needed by servers.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
- If I have to provide an availability of (3 9's) 99.9 then I would definitely go with Virtual Machine with Premium SSD
- If any of my services needed to be stateful then I would have gone with Virtual Machines
- Also If I need full control of the web server then I would have gone with Virtual Machines.