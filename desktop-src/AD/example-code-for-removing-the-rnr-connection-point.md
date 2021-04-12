---
title: Exemplo de código para remover o ponto de conexão do RnR
description: O exemplo de código a seguir é usado pelo exemplo de código de serviço do Winsock para cancelar o registro do ponto de conexão do RnR para o serviço.
ms.assetid: eee9b8b0-8566-442a-9a46-b6469e5bb1fc
ms.tgt_platform: multiple
keywords:
- Código de exemplo para remover o AD do ponto de conexão do RnR
- Registro do Windows Sockets, anúncio de resolução, código de exemplo, removendo o ponto de conexão do RnR
- Removendo o anúncio do ponto de conexão do RnR, código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1db126af451d8ecd3648ce04a93043df34b6a47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363668"
---
# <a name="example-code-for-removing-the-rnr-connection-point"></a><span data-ttu-id="8dbbd-106">Exemplo de código para remover o ponto de conexão do RnR</span><span class="sxs-lookup"><span data-stu-id="8dbbd-106">Example Code for Removing the RnR Connection Point</span></span>

<span data-ttu-id="8dbbd-107">O exemplo de código a seguir é usado pelo exemplo de código de serviço do Winsock para cancelar o registro do ponto de conexão do RnR para o serviço.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-107">The following code example is used by the Winsock service code example to unregister the RnR connection point for the service.</span></span>


```C++
#include <winsock2.h>
#include <stdio.h>
 
/***************************************************************************

    serverUnregister()

    Unregisters the RnR connection point for the specified service. 
    WSAStartup must be called before calling this function.

***************************************************************************/

INT serverUnregister(SOCKADDR *sa, 
                     GUID *pServiceID, 
                     LPTSTR pszServiceInstanceName, 
                     LPTSTR pszServiceInstanceComment)
{
    DWORD ret;
    WSAVERSION Version;
    WSAQUERYSET QuerySet;
    CSADDR_INFO CSAddrInfo[1];
    SOCKADDR sa_local;

    memset(&QuerySet, 0, sizeof(QuerySet));
    memset(&CSAddrInfo, 0, sizeof(CSAddrInfo));
    memset(&sa_local, 0, sizeof(SOCKADDR));
    sa_local.sa_family = AF_INET;

    // Build the CSAddrInfo structure to contain address
    // data. This is what clients use to create a connection.
    //
    // Be aware that the LocalAddr is set to zero because
    // dynamically assigned port numbers are used.
    //
    CSAddrInfo[0].LocalAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].LocalAddr.lpSockaddr = &sa_local;
    CSAddrInfo[0].RemoteAddr.iSockaddrLength = sizeof(SOCKADDR);
    CSAddrInfo[0].RemoteAddr.lpSockaddr = sa;
    CSAddrInfo[0].iSocketType = SOCK_STREAM;
    CSAddrInfo[0].iProtocol = PF_INET;

    QuerySet.dwSize = sizeof(WSAQUERYSET);
    QuerySet.lpServiceClassId = pServiceID;
    QuerySet.lpszServiceInstanceName = pszServiceInstanceName;
    QuerySet.lpszComment = pszServiceInstanceComment;
    QuerySet.lpVersion = &Version;
    QuerySet.lpVersion->dwVersion = 2;
    QuerySet.lpVersion->ecHow = COMP_NOTLESS;
    QuerySet.dwNameSpace = NS_NTDS;
    QuerySet.dwNumberOfCsAddrs = 1;
    QuerySet.lpcsaBuffer = CSAddrInfo;

    ret = WSASetService( &QuerySet,
                         RNRSERVICE_DEREGISTER,
                         SERVICE_MULTIPLE);

    return(ret);
}
```



 

 




