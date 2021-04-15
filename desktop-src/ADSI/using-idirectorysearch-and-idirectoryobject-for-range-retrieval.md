---
title: Usando IDirectorySearch e IDirectoryObject para recuperação de intervalo
description: As interfaces IDirectoryObject ou IDirectorySearch podem ser usadas para recuperar um intervalo de valores de propriedade. Para fazer isso, especifique o atributo e o intervalo para um dos atributos solicitados na consulta.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI, usando para a variação para recuperar membros de um grupo
- IDirectoryObject ADSI, usando para a variação para recuperar membros de um grupo
- ADSI de recuperação de intervalo, usando IDirectorySearch e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591d2cf7b65b7a8159a92de324f18fbe93164f0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754013"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Usando IDirectorySearch e IDirectoryObject para recuperação de intervalo

As interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ou [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) podem ser usadas para recuperar um intervalo de valores de propriedade. Para fazer isso, especifique o atributo e o intervalo para um dos atributos solicitados na consulta.

## <a name="range-retrieval-with-idirectoryobject"></a>Recuperação de intervalo com IDirectoryObject

A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pode ser usada para recuperação de intervalo, especificando o atributo e o intervalo para um dos atributos na matriz *pAttributesName* ao chamar o método [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Para obter mais informações e um exemplo de código que mostra como usar a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para recuperação de intervalo, consulte o [código de exemplo para variar com IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Recuperação de intervalo com IDirectorySearch

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pode ser usada para recuperação de intervalo, especificando o atributo e o intervalo para um dos atributos recuperados na matriz *pAttributesName* ao chamar o método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) .


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Ao usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para recuperação de intervalo, há um problema que deve ser resolvido especificamente. Quando o intervalo solicitado excede o número de valores restantes, [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) retornará a **\_ coluna ADS \_ E \_ não \_ definida**. Para recuperar os valores restantes, é necessário usar o curinga de intervalo ' \* '. Por exemplo, se um grupo contiver 150 Membros, os valores de membro 0-100 poderão ser recuperados normalmente usando a recuperação em intervalos. Se o intervalo 101-200 for solicitado, **IDirectorySearch:: GetColumn** retornará **E a \_ \_ coluna ADS \_ não será \_ definida**. Esse problema pode ser evitado usando o método [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) . Normalmente, **GetNextColumnName** retornará a cadeia de caracteres de consulta original. No entanto, quando o intervalo solicitado excede o número de valores restantes, **GetNextColumnName** retornará uma versão modificada da cadeia de caracteres de consulta, substituindo o valor de intervalo alto pelo curinga de intervalo ' \* '. No exemplo acima, a primeira consulta seria executada com uma cadeia de caracteres de atributo "membro; intervalo = 0-100" e **GetNextColumnName** retornará "membro; intervalo = 0-100". Na segunda consulta, a cadeia de caracteres do atributo seria "membro; intervalo = 101-200", mas **GetNextColumnName** retornará "membro; intervalo = 101- \* ". Esse caso pode ser determinado comparando a cadeia de caracteres do atributo original com o resultado de **GetNextColumnName**. Se as cadeias de caracteres forem diferentes, o último bloco de valores deverá ser solicitado novamente com o curinga de intervalo.

Para obter mais informações e um exemplo de código que mostra como usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para recuperação de intervalo, consulte o [código de exemplo para variar com IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




