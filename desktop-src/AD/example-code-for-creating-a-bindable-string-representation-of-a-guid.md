---
title: Exemplo de código para criar uma representação de cadeia de caracteres vinculável de um GUID
description: O exemplo de código a seguir pode ser usado para retornar uma representação de cadeia de caracteres de um GUID que pode ser usado para associar ao objeto.
ms.assetid: e39a6994-4328-40f2-8cb5-8b1f971e50d8
ms.tgt_platform: multiple
keywords:
- Exemplos de Active Directory Active Directory, criando uma representação de cadeia de caracteres ligável de um GUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6614ebeaf1028452ba75c0fc5dbaffb364e1ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004928"
---
# <a name="example-code-for-creating-a-bindable-string-representation-of-a-guid"></a><span data-ttu-id="39ca8-104">Exemplo de código para criar uma representação de cadeia de caracteres vinculável de um GUID</span><span class="sxs-lookup"><span data-stu-id="39ca8-104">Example Code for Creating a Bindable String Representation of a GUID</span></span>

<span data-ttu-id="39ca8-105">O exemplo de código a seguir pode ser usado para retornar uma representação de cadeia de caracteres de um GUID que pode ser usado para associar ao objeto.</span><span class="sxs-lookup"><span data-stu-id="39ca8-105">The following code example can be used to return a string representation of a GUID that can be used to bind to the object.</span></span>


```C++
//*******************************************************************
//
//  GUIDtoBindableString()
//
//  Converts a GUID into a string that can be used for binding with  
//  the <GUID= or <WKGUID= syntax. The caller must free the allocated  
//  string with the FreeADsStr when it is no longer required.
//
//*******************************************************************

HRESULT GUIDtoBindableString(LPGUID pGUID, LPWSTR *ppGUIDString)
{
    if((!pGUID) || (ppGUIDString==NULL))
    {
        return E_INVALIDARG;
    }

    // Build bindable GUID string.
    DWORD dwBytes =  sizeof(GUID);
    WCHAR szByte[3];
    LPWSTR pwszGUID = new WCHAR[(dwBytes * 2) + 1];
    if(NULL == pwszGUID)
    {
        return E_OUTOFMEMORY;
    }

    *pwszGUID = NULL;

    HRESULT hr = S_OK;
    LPBYTE lpByte;
    DWORD dwItem;

    // Loop through to add each byte to the string.
    for(dwItem = 0, 
        lpByte = (LPBYTE)pGUID; dwItem < dwBytes; 
        dwItem++)
    {
        // Append to pwszGUID, double-byte, byte at dwItem index.
        swprintf_s(szByte, L"%02x", lpByte[dwItem]);
        wcscat_s(pwszGuid, szByte);
    }
    
    // Allocate memory for the string.
    *ppGUIDString = AllocADsStr(pwszGUID);

    delete [] pwszGUID;
    
    if(NULL != *ppGUIDString)
    {
        hr = S_OK;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    
    // Caller must free ppGUIDString using FreeADsStr.
    return hr;
}
```



 

 




