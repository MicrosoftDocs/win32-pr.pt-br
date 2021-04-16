---
description: Um programa de configuração de serviço usa a função CreateService para instalar um serviço no banco de dados SCM.
ms.assetid: b94bf94e-1b07-4686-be5c-306e7cf13f39
title: Instalando um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e72953b2d3fc3ce549f614a035c9614c4d895a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751071"
---
# <a name="installing-a-service"></a>Instalando um serviço

Um [programa de configuração de serviço](service-configuration-programs.md) usa a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para instalar um serviço no banco de dados SCM.

A função SvcInstall no exemplo a seguir mostra como instalar um serviço do próprio programa de serviço. Para obter o exemplo completo, consulte [svc. cpp](svc-cpp.md).


```C++
//
// Purpose: 
//   Installs a service in the SCM database
//
// Parameters:
//   None
// 
// Return value:
//   None
//
VOID SvcInstall()
{
    SC_HANDLE schSCManager;
    SC_HANDLE schService;
    TCHAR szPath[MAX_PATH];

    if( !GetModuleFileName( "", szPath, MAX_PATH ) )
    {
        printf("Cannot install service (%d)\n", GetLastError());
        return;
    }

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

    // Create the service

    schService = CreateService( 
        schSCManager,              // SCM database 
        SVCNAME,                   // name of service 
        SVCNAME,                   // service name to display 
        SERVICE_ALL_ACCESS,        // desired access 
        SERVICE_WIN32_OWN_PROCESS, // service type 
        SERVICE_DEMAND_START,      // start type 
        SERVICE_ERROR_NORMAL,      // error control type 
        szPath,                    // path to service's binary 
        NULL,                      // no load ordering group 
        NULL,                      // no tag identifier 
        NULL,                      // no dependencies 
        NULL,                      // LocalSystem account 
        NULL);                     // no password 
 
    if (schService == NULL) 
    {
        printf("CreateService failed (%d)\n", GetLastError()); 
        CloseServiceHandle(schSCManager);
        return;
    }
    else printf("Service installed successfully\n"); 

    CloseServiceHandle(schService); 
    CloseServiceHandle(schSCManager);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instalação, remoção e enumeração de serviço](service-installation-removal-and-enumeration.md)
</dt> <dt>

[O exemplo de serviço completo](the-complete-service-sample.md)
</dt> </dl>

 

 



