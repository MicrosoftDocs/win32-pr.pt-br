---
description: Ao enumerar nuvens, um aplicativo deve fornecer o escopo da pesquisa para nuvens. Depois que o escopo é identificado, o aplicativo pode iniciar o processo de enumeração.
ms.assetid: efd16cca-ac63-4bfa-bc6c-d7465cc374ee
title: Enumerando nuvens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f958a2cc958c10bd85e674b43a3b41354fc344c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762924"
---
# <a name="enumerating-clouds"></a><span data-ttu-id="2d291-104">Enumerando nuvens</span><span class="sxs-lookup"><span data-stu-id="2d291-104">Enumerating Clouds</span></span>

<span data-ttu-id="2d291-105">Ao enumerar nuvens, um aplicativo deve fornecer o escopo da pesquisa para nuvens.</span><span class="sxs-lookup"><span data-stu-id="2d291-105">When enumerating clouds, an application must provide the scope of the search for clouds.</span></span> <span data-ttu-id="2d291-106">Depois que o escopo é identificado, o aplicativo pode iniciar o processo de enumeração.</span><span class="sxs-lookup"><span data-stu-id="2d291-106">After the scope is identified, the application can begin the enumeration process.</span></span>

<span data-ttu-id="2d291-107">O procedimento a seguir identifica as chamadas que precisam ser feitas para enumerar nuvens.</span><span class="sxs-lookup"><span data-stu-id="2d291-107">The following procedure identifies the calls that need to be made to enumerate clouds.</span></span>

<span data-ttu-id="2d291-108">**Para enumerar nuvens**</span><span class="sxs-lookup"><span data-stu-id="2d291-108">**To enumerate clouds**</span></span>

1.  <span data-ttu-id="2d291-109">Chame [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) para iniciar o processo e retornar um identificador.</span><span class="sxs-lookup"><span data-stu-id="2d291-109">Call [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) to begin the process and return a handle.</span></span>
2.  <span data-ttu-id="2d291-110">Chame [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) para recuperar um conjunto de nuvens e, em seguida, chame essa função até que o aplicativo tenha recuperado todas as nuvens.</span><span class="sxs-lookup"><span data-stu-id="2d291-110">Call [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) to retrieve a set of clouds, and then call this function until the application has retrieved all the clouds.</span></span>
3.  <span data-ttu-id="2d291-111">Chame [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) para concluir a enumeração.</span><span class="sxs-lookup"><span data-stu-id="2d291-111">Call [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) to finish the enumeration.</span></span>

## <a name="example-enumerating-and-printing-the-names-of-available-link-local-clouds"></a><span data-ttu-id="2d291-112">Exemplo: enumerando e imprimindo os nomes das nuvens de link local disponíveis</span><span class="sxs-lookup"><span data-stu-id="2d291-112">Example: Enumerating and Printing the Names of Available Link-Local Clouds</span></span>


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



 

 



