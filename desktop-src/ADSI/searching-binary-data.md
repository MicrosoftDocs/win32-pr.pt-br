---
title: Pesquisando dados binários
description: Embora o recurso de pesquisa ADSI só seja compatível com a pesquisa de dados de cadeia de caracteres, é possível pesquisar dados binários.
ms.assetid: 52b75ae0-dbf1-4310-8b6b-a176de9f1b7d
ms.tgt_platform: multiple
keywords:
- Pesquisando ADSI de dados binários
- ADSI de Dados Binários
- ADSI de dados binários, pesquisando dados binários
- ADSI ADSI , código de exemplo C/C++, pesquisando dados binários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f77ead11f4e2d02c6e7ef3e25975a7059c2c057dbc62f71e406bbda3e24c3b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005416"
---
# <a name="searching-binary-data"></a>Pesquisando dados binários

Embora o recurso de pesquisa ADSI só seja compatível com a pesquisa de dados de cadeia de caracteres, é possível pesquisar dados binários. Para fazer isso, use a [**função ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) para converter os dados binários em uma cadeia de caracteres que pode ser usada com os métodos de pesquisa. A pesquisa de dados binários é particularmente útil ao pesquisar um GUID ou um SID porque esses tipos de dados são armazenados como dados binários.

Ao usar [**a função ADsEncodeBinaryData,**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) a memória alocada deve ser liberada usando a [**função FreeADsMem.**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)

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



 

 




