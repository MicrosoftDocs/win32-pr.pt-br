---
description: Ao enumerar nuvens, um aplicativo deve fornecer o escopo da pesquisa de nuvens. Depois que o escopo é identificado, o aplicativo pode iniciar o processo de enumeração.
ms.assetid: efd16cca-ac63-4bfa-bc6c-d7465cc374ee
title: Enumerando nuvens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c651fcfd003e4cafdf9b0f04c7cfc993a1e677b03630a61556523eed8c3aaece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011554"
---
# <a name="enumerating-clouds"></a>Enumerando nuvens

Ao enumerar nuvens, um aplicativo deve fornecer o escopo da pesquisa de nuvens. Depois que o escopo é identificado, o aplicativo pode iniciar o processo de enumeração.

O procedimento a seguir identifica as chamadas que precisam ser feitas para enumerar nuvens.

**Para enumerar nuvens**

1.  Chame [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) para iniciar o processo e retornar um handle.
2.  Chame [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) para recuperar um conjunto de nuvens e, em seguida, chame essa função até que o aplicativo tenha recuperado todas as nuvens.
3.  Chame [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) para concluir a enumeração.

## <a name="example-enumerating-and-printing-the-names-of-available-link-local-clouds"></a>Exemplo: enumerando e imprimindo os nomes de nuvens locais de link disponíveis


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "ws2_32.lib")

DWORD PrintLinkLocalClouds()
{

    WSAQUERYSETW    qset;
    BLOB            Blob;
    PNRPCLOUDINFO   CloudInfo;
    HANDLE          hLookup = NULL;
    int             err;
    DWORD           dwErr = NO_ERROR;
    DWORD           dwSize;
    WSAQUERYSETW    *pResults = NULL;

    ZeroMemory(&qset, sizeof(qset));
    ZeroMemory(&CloudInfo, sizeof(CloudInfo));

    CloudInfo.dwSize = sizeof(PNRPCLOUDINFO);
    CloudInfo.Cloud.Scope = PNRP_LINK_LOCAL_SCOPE;

    Blob.cbSize = sizeof(PNRPCLOUDINFO);
    Blob.pBlobData = (LPBYTE)&CloudInfo;

    qset.dwSize = sizeof(WSAQUERYSET);
    qset.dwNameSpace = NS_PNRPCLOUD;
    qset.lpServiceClassId = (LPGUID)&SVCID_PNRPCLOUD;
    qset.lpBlob = &Blob;

    //
    // Start enumeration
    //
    err = WSALookupServiceBegin(
            &qset,
            LUP_RETURN_NAME,
            &hLookup);
                
    if(err !=0)
    {
        return WSAGetLastError();
    }

    // getting results
    while(TRUE)
    {

        //
        // Get size
        //
        ZeroMemory(&qset, sizeof(qset));
        dwSize = sizeof(qset);

        pResults = &qset;

        err = WSALookupServiceNext(
                hLookup,
                0,
                &dwSize,
                pResults
                );
        if(err != 0)
        {
            dwErr = WSAGetLastError();
        }

        if(dwErr != NO_ERROR)
        {
            if(dwErr == WSA_E_NO_MORE)
            {
                //
                // No more entries
                //
                dwErr = ERROR_SUCCESS;
                break;
            }
            else if (dwErr == WSAEFAULT)
            {
                //
                // This usually means result buffer too small. Allocate space
                //
                pResults = (WSAQUERYSET *)malloc(dwSize);
                if(pResults == NULL)
                {
                    dwErr = ERROR_OUTOFMEMORY;
                    break;
                }

                //
                // Get cloud name
                //
                err = WSALookupServiceNext(
                        hLookup,
                        0,
                        &dwSize,
                        pResults
                        );
                if(err == 0)
                {
                    wprintf(L"%s\n", pResults->lpszServiceInstanceName);

                    dwErr = NO_ERROR;
                }
                else
                {
                    dwErr = WSAGetLastError();
                }

                free(pResults);

                if(dwErr != NO_ERROR)
                {
                    break;
                }
            }
            else
            {
                //
                // Some other unexpected error
                //
                break;
            }
        }
        else
        {
            //
            // Should never happen
            //
            dwErr = ERROR_GEN_FAILURE;
            break;
        }
    }

    //
    // Close the enumeration
    //
    WSALookupServiceEnd(hLookup);
                
    return dwErr;
}
```



 

 



