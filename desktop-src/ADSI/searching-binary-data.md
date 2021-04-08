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
# <a name="searching-binary-data"></a>Pesquisando dados binários

Embora o recurso de pesquisa ADSI só dê suporte à pesquisa de dados de cadeia de caracteres, é possível pesquisar dados binários. Para fazer isso, use a função [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) para converter os dados binários em uma cadeia de caracteres que pode ser usada com os métodos de pesquisa. A pesquisa de dados binários é particularmente útil ao pesquisar um GUID ou um SID, pois esses tipos de dados são armazenados como dados binários.

Ao usar a função [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) , a memória alocada deve ser liberada usando a função [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .

O exemplo de código C++ a seguir mostra como criar uma cadeia de caracteres de consulta para pesquisar um objeto que tenha um valor **objectGUID** específico.


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



 

 




