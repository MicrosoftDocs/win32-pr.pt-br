---
title: Obtendo a tabela de interfaces MIB II
description: O código a seguir usa MprAdminMIBEntryGet para obter a tabela de interfaces MIB II do computador local.
ms.assetid: 76152cd8-f285-42b3-8ee5-bbab1d14b99f
keywords:
- MIB, obtendo as interfaces
- Obtendo as interfaces MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05eb1bb10822ce7dc770e58c5aed36167340a9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917605"
---
# <a name="obtaining-the-mib-ii-interfaces-table"></a><span data-ttu-id="7519a-105">Obtendo a tabela de interfaces MIB II</span><span class="sxs-lookup"><span data-stu-id="7519a-105">Obtaining the MIB II Interfaces Table</span></span>

<span data-ttu-id="7519a-106">O código a seguir usa [**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget) para obter a tabela de interfaces MIB II do computador local.</span><span class="sxs-lookup"><span data-stu-id="7519a-106">The following code uses [**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget) to obtain the MIB II interfaces table from the local machine.</span></span>


```C++
#include <windows.h>
#include <mprapi.h>
#include <iprtrmib.h>

#pragma comment(lib, "mprapi.lib")

void main()
{
    HANDLE            _hMibSrv = INVALID_HANDLE_VALUE;  
    MIB_OPAQUE_QUERY  MibOpaqueQuery; 
    PMIB_OPAQUE_INFO  pMibOpaqueInfo = NULL; 
    DWORD             dwInSize, dwOutSize, dwResult; 
    PMIB_IFTABLE      pIntfTable; 
    
    MibOpaqueQuery.dwVarId = IF_TABLE; 
    dwInSize = sizeof( MIB_OPAQUE_QUERY ); 
    dwOutSize = 0; 
    
    dwResult = MprAdminMIBEntryGet ( _hMibSrv, 
                                    PID_IP, 
                                    IPRTRMGR_PID, 
                                    (PVOID)&MibOpaqueQuery, 
                                    dwInSize, 
                                    (PVOID *)&pMibOpaqueInfo, 
                                    &dwOutSize );

    if ( dwResult != NO_ERROR )
        return;
    
    if ( pMibOpaqueInfo == NULL ) 
        return; 
    
    pIntfTable = ( PMIB_IFTABLE ) pMibOpaqueInfo -> rgbyData;
}


#include <windows.h>
#include <stdio.h>
#include &quot;Iphlpapi.h&quot;

int __cdecl main(){

    MIB_SERVER_HANDLE hMibSrv = NULL;  
    MIB_OPAQUE_QUERY MibOpaqueQuery; 
    PMIB_OPAQUE_INFO pMibOpaqueInfo = NULL; 
    DWORD dwInSize, dwOutSize, dwRes; 
    PMIB_IFTABLE pIntfTable; 
    
    MibOpaqueQuery.dwVarId = IF_TABLE; 
    dwInSize = sizeof(MIB_OPAQUE_QUERY); 
    dwOutSize = 0; 
    
    // Connect to the MIB server to obtain the hMibSrv handle
    dwRes = MprAdminMIBServerConnect(NULL, &hMibSrv);    
    if (dwRes != NO_ERROR){
        wprintf(L&quot;ERROR: Unable to connect to the MIB server specified.\n&quot;);
        return ERROR_SUCCESS;
    }

    // Retrieve the MIB interfaces table. The local RRAS service MUST be running or this call will fail.
    dwRes = MprAdminMIBEntryGet(hMibSrv, PID_IP, IPRTRMGR_PID, (PVOID)&MibOpaqueQuery, dwInSize, (PVOID*)&pMibOpaqueInfo, &dwOutSize);
    if (dwRes != NO_ERROR){
        wprintf(L&quot;ERROR: Unable to retrieve the MIB interface table.\n&quot;);
        return ERROR_SUCCESS;
    }

    // Disconnect from the MIB server to release the hMibSrv handle
    MprAdminMIBServerDisconnect(hMibSrv);

    if (dwRes != NO_ERROR)
        return ERROR_SUCCESS;
    
    if (pMibOpaqueInfo == NULL) 
        return ERROR_SUCCESS; 
    
    pIntfTable = (PMIB_IFTABLE)pMibOpaqueInfo->rgbyData;

    // Print out the name and description of each MIB interface in the table
    wprintf(L&quot;There were %d MIB table records found:\n&quot;, pIntfTable->dwNumEntries);
    for(UINT i=0; i < pIntfTable->dwNumEntries; i++){
        wprintf(L&quot;%d\t%s\t&quot;, i, pIntfTable->table[i].wszName, pIntfTable->table[i].bDescr);
        printf(&quot;%s\n&quot;, pIntfTable->table[i].bDescr);
    }

    return ERROR_SUCCESS;
}
```





## <a name="related-topics"></a><span data-ttu-id="7519a-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7519a-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7519a-108">**\_informações opacas de MIB \_**</span><span class="sxs-lookup"><span data-stu-id="7519a-108">**MIB\_OPAQUE\_INFO**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_opaque_info)
</dt> <dt>

[<span data-ttu-id="7519a-109">**\_consulta opaca por MIB \_**</span><span class="sxs-lookup"><span data-stu-id="7519a-109">**MIB\_OPAQUE\_QUERY**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_opaque_query)
</dt> <dt>

[<span data-ttu-id="7519a-110">**MprAdminMIBEntryGet**</span><span class="sxs-lookup"><span data-stu-id="7519a-110">**MprAdminMIBEntryGet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget)
</dt> </dl>

 

 