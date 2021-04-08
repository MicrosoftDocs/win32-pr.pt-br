---
description: Um programa de configuração de serviço usa a função OpenService para obter um identificador para um objeto de serviço instalado. O programa pode usar o identificador de objeto de serviço na função DeleteService para excluir o serviço do banco de dados SCM.
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: Excluindo um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b1e0e95e0ea943487a0d3fa513afa2c0563d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922423"
---
# <a name="deleting-a-service"></a><span data-ttu-id="70efa-104">Excluindo um serviço</span><span class="sxs-lookup"><span data-stu-id="70efa-104">Deleting a Service</span></span>

<span data-ttu-id="70efa-105">Um [programa de configuração de serviço](service-configuration-programs.md) usa a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) para obter um identificador para um objeto de serviço instalado.</span><span class="sxs-lookup"><span data-stu-id="70efa-105">A [service configuration program](service-configuration-programs.md) uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function to get a handle to an installed service object.</span></span> <span data-ttu-id="70efa-106">O programa pode usar o identificador de objeto de serviço na função [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para excluir o serviço do banco de dados SCM.</span><span class="sxs-lookup"><span data-stu-id="70efa-106">The program can then use the service object handle in the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service from the SCM database.</span></span>

<span data-ttu-id="70efa-107">A função DoDeleteSvc no exemplo a seguir mostra como excluir um serviço do banco de dados SCM.</span><span class="sxs-lookup"><span data-stu-id="70efa-107">The DoDeleteSvc function in the following example shows how to delete a service from the SCM database.</span></span> <span data-ttu-id="70efa-108">A variável szSvcName é uma variável global que contém o nome do serviço a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="70efa-108">The szSvcName variable is a global variable that contains the name of the service to be deleted.</span></span> <span data-ttu-id="70efa-109">Para obter o exemplo completo que define essa variável, consulte [SvcConfig. cpp](svcconfig-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="70efa-109">For the complete example that sets this variable, see [SvcConfig.cpp](svcconfig-cpp.md).</span></span>


```C++
//
// Purpose: 
//   Deletes a service from the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID __stdcall DoDeleteSvc()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    SERVICE_STATUS ssStatus; 

    // Get a handle to the SCM database. 
 
    schSCManager = OpenSCManager( 
        NULL,                    // local computer
        NULL,                    // ServicesActive database 
        SC_MANAGER_ALL_ACCESS);  // full access rights 
 
    if (NULL == schSCManager) 
    {
        printf("OpenSCManager failed (%d)\n", GetLastError());
        return;
    }

    // Get a handle to the service.

    schService = OpenService( 
        schSCManager,       // SCM database 
        szSvcName,          // name of service 
        DELETE);            // need delete access 
 
    if (schService == NULL)
    { 
        printf("OpenService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }

    // Delete the service.
 
    if (! DeleteService(schService) ) 
    {
        printf("DeleteService failed (%d)\n", GetLastError()); 
    }
    else printf("Service deleted successfully\n"); 
 
    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a><span data-ttu-id="70efa-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70efa-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70efa-111">Instalação, remoção e enumeração de serviço</span><span class="sxs-lookup"><span data-stu-id="70efa-111">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> <dt>

[<span data-ttu-id="70efa-112">O exemplo de serviço completo</span><span class="sxs-lookup"><span data-stu-id="70efa-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



