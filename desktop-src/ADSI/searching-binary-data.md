---
title: Pesquisando dados binários
description: Embora o recurso de pesquisa ADSI só dê suporte à pesquisa de dados de cadeia de caracteres, é possível pesquisar dados binários.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Pesquisando dados binários ADSI
- ADSI de dados binários
- Dados binários ADSI, pesquisando dados binários
- ADSI ADSI, código de exemplo C/C++, pesquisando dados binários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0973ff7a769d68abf85e6557fef2e1d434ba3ff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004861"
---
# <a name="searching-binary-data"></a><span data-ttu-id="80276-107">Pesquisando dados binários</span><span class="sxs-lookup"><span data-stu-id="80276-107">Searching Binary Data</span></span>

<span data-ttu-id="80276-108">Embora o recurso de pesquisa ADSI só dê suporte à pesquisa de dados de cadeia de caracteres, é possível pesquisar dados binários.</span><span class="sxs-lookup"><span data-stu-id="80276-108">Even though the ADSI search feature only supports searching for string data, it is possible to search for binary data.</span></span> <span data-ttu-id="80276-109">Para fazer isso, use a função [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) para converter os dados binários em uma cadeia de caracteres que pode ser usada com os métodos de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="80276-109">To do this, use the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function to convert the binary data into a string that can be used with the search methods.</span></span> <span data-ttu-id="80276-110">A pesquisa de dados binários é particularmente útil ao pesquisar um GUID ou um SID, pois esses tipos de dados são armazenados como dados binários.</span><span class="sxs-lookup"><span data-stu-id="80276-110">Searching for binary data is particularly useful when searching for a GUID or a SID because these data types are stored as binary data.</span></span>

<span data-ttu-id="80276-111">Ao usar a função [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) , a memória alocada deve ser liberada usando a função [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="80276-111">When using the [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) function, the memory allocated must be freed using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="80276-112">O exemplo de código C++ a seguir mostra como criar uma cadeia de caracteres de consulta para pesquisar um objeto que tenha um valor **objectGUID** específico.</span><span class="sxs-lookup"><span data-stu-id="80276-112">The following C++ code example shows how to build a query string to search for an object that has a particular **objectGUID** value.</span></span>


```C++
LPWSTR pwszGuid = NULL;
LPWSTR pwszFormat = L"(objectGUID=%s)";
LPWSTR pwszSearch = NULL;
hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
if(FAILED(hr))
{
    goto cleanup;
}

pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
if(NULL == pwszSearch)
{
    goto cleanup;
}
    
swprintf_s(pwszSearch, pwszFormat, pwszGuid);

// Use pwszSearch to perform a query for the object.

cleanup:    
if(pwszGuid)
{
    FreeADsMem(pwszGuid);
}
if(pwszSearch)
{
    delete pwszSearch;
}

```



 

 




