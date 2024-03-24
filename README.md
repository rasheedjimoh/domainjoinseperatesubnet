# Connecting Clients Across Subnets: Adding a New Domain Client

![ad-joined-frontdesk1](https://github.com/rasheedjimoh/domainjoinseperatesubnet/assets/157264080/f6bf5950-354f-4d60-a53a-e2c4b827792e)


## Introduction
I'm excited to share a step-by-step guide on how to add a client in another subnet to your domain. As we expand our network or set up remote offices, it's crucial to ensure seamless connectivity and integration with our existing domain infrastructure.

## Why We Need It

Adding a client in another subnet to your domain is essential for several reasons:

1. **Network Expansion:**
   - As businesses grow and expand, the need to connect clients across different subnets arises. Adding new clients to the domain allows for seamless integration into the existing network infrastructure, facilitating collaboration and resource sharing.

2. **Remote Office Setup:**
   - In scenarios where remote offices or branch locations are established, joining clients to the domain enables centralized management and administration. This ensures consistency in security policies, software deployments, and user access permissions across geographically dispersed locations.

3. **Enhanced Connectivity:**
   - Connecting clients across subnets improves overall network connectivity and accessibility. Clients can securely access domain resources, such as shared drives, printers, and applications, regardless of their physical location within the network.

4. **Centralized Management:**
   - Joining clients to the domain centralizes management tasks, simplifying administration and troubleshooting. IT administrators can easily deploy software updates, enforce security policies, and monitor client activity from a centralized location, improving operational efficiency and productivity.

5. **Security and Compliance:**
   - Domain-joined clients benefit from enhanced security measures enforced through group policies. These policies help ensure compliance with security standards and regulatory requirements by implementing measures such as password policies, encryption settings, and access controls.

6. **Scalability and Flexibility:**
   - Adding clients to the domain supports scalability and flexibility in network design. As the organization grows or network requirements change, additional clients can be seamlessly integrated into the domain infrastructure, accommodating evolving business needs and technological advancements.

In summary, adding a client in another subnet to your domain is crucial for expanding network connectivity, enabling centralized management, and ensuring security and compliance across the organization.

---
 
## Procedure / Process

**Step 1: Network Configuration**

Before we dive into adding the new client, let's ensure that the network is properly configured. Make sure that both the client's subnet and the domain controller's subnet can communicate with each other. This often involves setting up appropriate routing or configuring VLANs if necessary.

**Step 2: DNS Configuration**

Next, we need to ensure that the new client can resolve DNS queries for the domain. Configure the client's DNS settings to point to the domain controller's IP address. This allows the client to locate the domain controller and join the domain.

**Step 3: Joining the Domain**

Now comes the exciting part – joining a new client to the domain. On the client machine, navigate to the Control Panel, then click on System and Security, followed by System. Here, you'll find the option to change the computer name and domain. Click on "Change settings" and then "Change" to join a domain.

**Step 4: Authentication**

You'll be prompted to enter the credentials of a domain user with sufficient privileges to join computers to the domain. Once authenticated, specify the domain name and click "OK." The client will communicate with the domain controller to complete the joining process.

**Step 5: Verification**

After joining the domain, restart the client machine to apply the changes fully. Upon reboot, log in using a domain account to verify that the client has successfully joined the domain. You can also check the Active Directory Users and Computers console on the domain controller to confirm that the client's computer account has been created.

**Step 6: Group Policy**

Finally, don't forget to apply any necessary group policies to the new client. Group policies help enforce security settings, software installations, and other configurations across domain-joined machines. Ensure that the client receives the appropriate policies to align with your organization's requirements.
  
## Technologies/Stacks
- VMware Workstation Pro as Hypervisor Type 2
- Windows Server 2019 (DC): Mydomain's Domain Controller/ Active Directory


![ad-joined-frontdesk1-poc](https://github.com/rasheedjimoh/domainjoinseperatesubnet/assets/157264080/c4243e25-76b4-48ff-97a1-80bfe5db1069)

## Conclusion
By following these steps, you can easily add a client in another subnet to your domain, enabling seamless integration and centralized management. Remember to pay attention to network connectivity, DNS resolution, authentication, and group policy settings to ensure a smooth transition. With proper configuration and attention to detail, your new client will be up and running on the domain in no time.

Happy networking!
