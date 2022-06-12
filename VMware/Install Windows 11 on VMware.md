## Installing Windows 11 as a guest OS on VMware Workstation Pro/Player and Fusion

**Purpose**            

This article provides steps to install Windows 11 as a guest Operating System on Workstation Pro/Player and Fusion.

**Workaround**            

While the fix is being worked on, you can resolve the issue through a workaround.

**Note:** Minimum Requirement by Microsoft to run Windows 11 requires TPM support.

### **Process to Install Windows 11 in a virtual machine using Windows 11 ISO image:**

1. While installing a new Guest OS, Select the OS type as "Windows 10 and later x64".
2. Before starting the installation, Configure default settings of Virtual  Machine to be created in-order to match the minimum system  requirements for Windows 11, Check here https://www.microsoft.com/en-in/windows/windows-11-specifications

- To configure Processor and RAM requirements : Go to Guest VM settings -> Processors & Memory.
- For Storage memory: Go to Guest VM Settings -> Hard Disk -> Increase the Disk Size as per minimum requirement.
- Enable UEFI, Secure Boot capable: Go to Guest VM settings -> Advanced                     

1. With regards to Microsoft’s minimum requirement of TPM, there are three ways to install Windows 11.

  A. Use the Software feature by updating the vmx file:

- Before starting the installation process. Edit the vmx file for the newly created VM and add managedVM.autoAddVTPM = "software"

Source: https://kb.vmware.com/s/article/86207