# DevOps - Configuration Management
- "Configuration management (CM) is a system engineering process for establishing and maintaining consistency of a product's performance, functional, and physical attributes with its requirements, design, and operational information throughout its life." https://www.upguard.com/blog/5-configuration-management-boss

# Ansible
- Allows us to write code to install and deploy multiple servers consistently.
  - Instructions to automate IT setup
  - Configuration Management: consistency of all systems in the infrastructure is maintained 
  - Automatic Deployment: applications are deployed automatically on a variety of environments
  
## Push Configuration Tool:
  - Ansible is installed in the local machine server and it pushes configurations to the nodes (servers connected to the main local machine) through an SSH client
  - Local machines hold:
   - Modules: collections of configuration code files (also known as playbooks)
   - Inventory: document that groups the nodes under specific labels
    
## Playbook:
  - The core where the architecture is defined, where instructions for configure nodes are written in YAML files
  - YAML files define the specific tasks for each node to configure the desired state
    
## Inventory: 
  - Maintains the structure of the nodes' environment by classifying nodes into groups (manages physical hardware)
  - Hostnames of the nodes are specified under the group name

  
# AWS CloudFormation
- AWS CloudFormation provides users with a simple way to create and manage a collection of Amazon Web Services (AWS) resources by provisioning and updating them in a predictable way
- It enables you to specify and manage the complete infrastructure or AWS resources in a reusable text file (YAML or JASON), without having to perform manual actions
- To make templates reusable, we use parameters, mapping, and conditions sections in the template to customize stacks

## How CloudFormation Works:
  - Create or use existing CloudFormation template using JSON/YAML file
  - Save your code template locally or in S3 bucket
  - Use CloudFormation to create a stack on your template
  - AWS CloudFormation constructs and configures your stack resources that you have specified in your template
  
## Two Major Components: Template and Stack
 ### Templates:
  - Formatted text file in JSON or YAML language that describes your AWS infrastructure
  - Use AWS CloudFormation Designer to create
  - Consists of nine main objects:
   - 1. Format Version: defines the capability of a template 
   - 2. Description: any comments about the template is specified in the description
   - 3. Metadata: used to provide further information using JSON or YAML objects
   - 4. Parameters: customized, so each time you create or update your stack, parameter gives custom template runtime
   - 5. Mapping: enables you to map keys to corresponding named value that you specify in conditional parameter
   - 6. Conditions: used when you want to reuse the templates by creating resources in different context 
   - 7. Transform: build simple declarative language for AWS CloudFormation and enables reuse of template components
   - 8. Resource: declare the AWS resource that you want to create and specify in the stack (EC2, S3, etc)
                : logical IF and name specified + optional additional information
   - 9. Output: describes the output values that you can import into other stacks or the values that are returned when users view their own stack property
   - Template Resource Attributes:
    - Create Policy: used when you want to delay on resource configuration actions before proceeding with stack creation      
    - Deletion Policy: preserving and backing up of resource is possible when its stack is deleted
    - Depends On: any user can define the creation of a specific resource followed by another resource 
    - Metadata: helps you associate a resource with structured data
    - Update Policy: can manage and replace the updates of the instances in the Auto Scaling group
    
  ###  Stack:
   - Collection of AWS resources and can be managed in a single unit
   - CloudFormation's template defines a stack in which the resources can be created, deleted, or updated in a predictable way
   - Nested Stack: hierarchy of stacks, can create nested stack within another stack
   - Windows Stack: can run windows instances (pre-configured template)
   - Stack sets: lets you create stack in AWS accounts across the globe by using single template
    
             
# Terraform
