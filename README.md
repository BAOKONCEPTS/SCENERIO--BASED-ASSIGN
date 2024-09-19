Maintaining a simple web application in Microsoft Azure involves several steps, and focusing on cost, scalability, and security is critical to effective management. Below is a detailed scenario of how you can do this:

1. Choose the right service
Web Application Service (Application Service):

Cost: Start with a basic or free pricing tier for development and testing. When you scale, you can switch to the Standard or Premium level depending on your needs.
Scalable: App Service allows you to scale vertically (upgrade to a higher level) and horizontally (number of instances added) easily.
Security: Built-in features include managed SSL certificates, authentication/authorization, and integration with Azure Active Directory.
Azure Virtual Machines (more control):

Cost: Ongoing pricing based on virtual machine size and usage. Consider boxes or reserved seats to save costs.
Scalability: Requires manual scaling or automatic scaling using virtual machine scale sets.
Security: You're in full control, but you have to manage updates, firewalls, and other security measures yourself.
2. Deployment strategy
Development: Use Azure DevOps or GitHub Actions to automate your CI/CD pipeline. This ensures that your web application is tested and deployed effectively.
Deployment: For simple web applications, Azure App Service is often the easiest way to deploy. Deploy Git, FTP, or Azure DevOps.
3. Cost control
Estimated costs: Use the Azure pricing calculator to estimate costs based on the services and resources you want to use.
Budget alerts: Set up cost management and budget alerts in Azure Cost Management + Billing to track and manage expenses.
Scaling: Use automatic scaling to control costs by adjusting the number of instances based on traffic or load.


4. Scalability
Horizontal scaling: Configure automatic scaling settings in Azure Application Services. You can scale based on parameters such as CPU usage, memory, or request queue length.
Vertical scaling: Increase your App Service plan level if you need more resources (CPU, memory).
Load balancing: Azure App Services includes a built-in load balancer. For virtual machines, use Azure Load Balancer or Application Gateway to distribute traffic.
5. Security
Network security:

Application services: Use IP blocking, virtual network integration, and private endpoints.
VMs: Configure a network security group (NSG) with Azure Firewall to control inbound and outbound traffic.
Data protection: 

Application services: Use a managed SSL certificate to protect data in transit.
VMs: Use encryption for data when using Azure Disk Encryption.
Identity and access management:

Application services: Use Azure Active Directory for user authentication and role-based access control.
VMs: Manage user access with Azure role-based access control (RBAC) and Azure Active Directory.
Regular updates: Keep your application and all key VMs or infrastructure components up to date with security patches.

6. Care and maintenance
Monitoring: Use Azure Monitor and Application Insights to track application performance, detect issues, and gain insights into usage patterns.
Maintenance: Regularly check logs, set up anomaly alerts, and perform regular health checks and updates.
Generally speaking, to host simple web applications on Microsoft Azure, start with Azure Application Service for a cost-effective, scalable, and secure solution. Use Azure's built-in scalability and security capabilities, and use Azure Cost Management to keep costs in check. For more control and customization, consider using virtual machine, but be prepared to handle additional management. Regular maintenance and upkeep will keep your application running smoothly and safely.

