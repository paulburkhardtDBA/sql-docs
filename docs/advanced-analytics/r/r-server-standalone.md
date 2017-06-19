---
title: "R Server (Standalone) | Microsoft Docs"
ms.custom: 
  - "SQL2016_New_Updated"
ms.date: "04/14/2017"
ms.prod: "r-server"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "r-services"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "R"
ms.assetid: ca9e48f1-67b8-4905-9b78-56752d7a4e81
caps.latest.revision: 21
author: "jeannt"
ms.author: "jeannt"
manager: "jhubbard"
---
# R Server (Standalone)
 
In SQL Server 2016, Microsoft released **R Server (Standalone)**, as part of its platform for supporting enterprise-class analytics.  Microsoft R Server provided scalability and security to the R language, and addressed the in-memory limitations of open source R. Like SQL Server R Services, Microsoft R Server (Standalone) provides parallel and chunked processing of data, enabling R users to use data much bigger than can fit in memory.

In SQL Server 2017, support has been added for the Python language, which is another popular choice for advanced machine learning and text processing tasks.  To reflect support for this broader set of languages, we've also renamed it to **Microsoft Machine Learning Server (Standalone)**.

## What's Included in Microsoft R Server
 
You can use Microsoft R Server for distributed computing on multiple platforms. When you install from SQL Server setup, you get the Windows-based server and all the required tools for publishing and deploying models. For more information about other platforms, see these resources in the MSDN library:

+ [Introducing Microsoft R Server](https://msdn.microsoft.com/microsoft-r/rserver)
+ [R Server for Windows](https://msdn.microsoft.com/microsoft-r/rserver-install-windows)

You can also install Microsoft R Server to use as a development client, to get the RevoScaleR libraries and tools needed to create R solutions that can be deployed to SQL Server.
  
## What's New in Microsoft Machine Learning Server

If you install Machine Learning Services (Standalone) using SQL Server 2017 setup, you now have the option to add the Python language. Naturally, the R language is still a supported option, and you can even install both languages if desired.
 
In SQL Server 2017 CTP 2.0, the server installation also includes the mrsdeploy package and other utilities used for operationalizing models. For more information, see [Operationalization with mrsdeploy](../../advanced-analytics/operationalization-with-mrsdeploy.md).

## How to Get Microsoft R Server or Machine Learning Server (Standalone) 
 
 There are multiple options for installing Microsoft R Server:

### Use the SQL Server setup wizard

[Create a Standalone R Server](../r/create-a-standalone-r-server.md)

+ Run SQL Server 2016 setup to install **Microsoft R Server (Standalone)**. The R language is added by default.
+ Run SQL Server 2017 setup to install **Machine Learning Server (Standalone)** and select either R or Python, or both.

> [!IMPORTANT]
> The option to install the server is in the **Shared Features** section of setup. Do not install any other commponents.
>
> Preferably, do not install the server on a computer where SQL Server R Services or SQL Server Machine Learning Services has been installed. 

### Use command-line options for SQL Server setup

[Install Microsoft R Server from the Command Line](../r/install-microsoft-r-server-from-the-command-line.md)

SQL Server setup supports unattended installs via a rich set of command-line arguments. 

### Use the standalone installer

You can now use a new Windows installer to set up a new instance of Microsoft R Server or Microsoft Machine Learning Server.

Both Microsoft R Server and Microsoft Machine Learning Server require a SQL Server Enterprise agreement. 
However, after you run the standalone installer, the support policy for an existing intallation is updated, to use the new Modern Lifecycle policy. This support option ensures that updates to machine learning components are applied more frequently than they would be when using the SQL Server service releases. 

+ [Run Microsoft R Server for Windows](https://msdn.microsoft.com/microsoft-r/rserver-install-windows).

+ Upgrade a SQL Server instance

  You can use the standalone installer to upgrade an instance of SQL Server 2016 R Services to use the latest version of R. When you run the installer, the instance you specify will use the Modern Lifecycle support policy instead, and thus get more frequent updates. This update can only be performed on an existing installation of SQL Server 2016. For more information, see [Using SqlBindR to Upgrade an Instance of R Services](./use-sqlbindr-exe-to-upgrade-an-instance-of-sql-server.md).


## Related Machine Learning Products

+ **Azure virtual machines with R Server**: The Azure marketplace includes multiple virtual machine images that include R Server. Creating a new Azure virtual machine is the fastest way to set up a server for operationalizing predictive models. Some images come with scaling and sharing features (formerly known as DeployR) already configured, which makes it easier to embed R analytics inside applications and integrate R with backend systems. For more information, see [Provision an R Server Virtual Machine](../../advanced-analytics/r-services/provision-the-r-server-only-sql-server-2016-enterprise-vm-on-azure.md)
  
## Resources

For samples, tutorials, and more information about Microsoft R, see [Microsoft R Products](https://msdn.microsoft.com/microsoft-r/microsoft-r-getting-started).   

## See Also

 [SQL Server R Services](../../advanced-analytics/r/sql-server-r-services.md)   

  
  