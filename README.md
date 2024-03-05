# Connecting Clients Across Subnets: Adding a New Domain Client

## Introduction
I'm excited to share a step-by-step guide on how to add a client in another subnet to your domain. As we expand our network or set up remote offices, it's crucial to ensure seamless connectivity and integration with our existing domain infrastructure.
 
### Procedure / Process

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

## Conclusion
By following these steps, you can easily add a client in another subnet to your domain, enabling seamless integration and centralized management. Remember to pay attention to network connectivity, DNS resolution, authentication, and group policy settings to ensure a smooth transition. With proper configuration and attention to detail, your new client will be up and running on the domain in no time.

Happy networking!
