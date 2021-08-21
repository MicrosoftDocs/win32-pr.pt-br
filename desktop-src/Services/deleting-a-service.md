---
description: Um programa de configuração de serviço usa a função OpenService para obter um identificador para um objeto de serviço instalado. O programa pode usar o identificador de objeto de serviço na função DeleteService para excluir o serviço do banco de dados SCM.
ms.assetid: 3bfe4d42-a8a0-4613-9b0f-a80eef54b622
title: Excluindo um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5f4f79b17de2e3726fcd8bc4ada8b34cc10c404789200ffa5eaa71373ff823
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968193"
---
# <a name="deleting-a-service"></a>Excluindo um serviço

Um [programa de configuração de](service-configuration-programs.md) serviço usa a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) para obter um identificador para um objeto de serviço instalado. O programa pode usar o identificador de objeto de serviço na [**função DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para excluir o serviço do banco de dados SCM.

A função DoDeleteSvc no exemplo a seguir mostra como excluir um serviço do banco de dados SCM. A variável szSvcName é uma variável global que contém o nome do serviço a ser excluído. Para ver o exemplo completo que define essa variável, consulte [SvcConfig.cpp](svcconfig-cpp.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instalação, remoção e enumeração do serviço](service-installation-removal-and-enumeration.md)
</dt> <dt>

[O exemplo de serviço completo](the-complete-service-sample.md)
</dt> </dl>

 

 



