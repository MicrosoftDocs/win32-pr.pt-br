---
title: Usando IDirectorySearch e IDirectoryObject para recuperação de intervalo
description: As interfaces IDirectoryObject ou IDirectorySearch podem ser usadas para recuperar um intervalo de valores de propriedade. Para fazer isso, especifique o atributo e o intervalo para um dos atributos solicitados na consulta.
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- IDirectorySearch ADSI , usando para a variação para recuperar membros de um grupo
- IDirectoryObject ADSI , usando para a variação para recuperar membros de um grupo
- ADSI de Recuperação de Intervalo usando IDirectorySearch e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d061dd49c98bdb3b8cc731a28d0dc0ee5fe9a0df5816abf259ece17e456ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023054"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>Usando IDirectorySearch e IDirectoryObject para recuperação de intervalo

As interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ou [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) podem ser usadas para recuperar um intervalo de valores de propriedade. Para fazer isso, especifique o atributo e o intervalo para um dos atributos solicitados na consulta.

## <a name="range-retrieval-with-idirectoryobject"></a>Recuperação de intervalo com IDirectoryObject

A interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) pode ser usada para recuperação de intervalo especificando o atributo e o intervalo para um dos atributos na matriz *pAttributesName* ao chamar o método [**IDirectoryObject::GetObjectAttributes.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



Para obter mais informações e um exemplo de código que mostra como usar a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para recuperação de intervalo, consulte Código de exemplo para variar com [IDirectoryObject](example-code-for-ranging-with-idirectoryobject.md).

## <a name="range-retrieval-with-idirectorysearch"></a>Recuperação de intervalo com IDirectorySearch

A interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pode ser usada para recuperação de intervalo especificando o atributo e o intervalo para um dos atributos recuperados na matriz *pAttributesName* ao chamar o método [**IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



Ao usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para recuperação de intervalo, há um problema que deve ser resolvido especificamente. Quando o intervalo solicitado exceder o número de valores restantes, [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) retornará **E ADS COLUMN NOT \_ \_ \_ \_ SET**. Para recuperar os valores restantes, é necessário usar o curinga de intervalo \* ' '. Por exemplo, se um grupo contiver 150 membros, os valores de membro de 0 a 100 poderão ser recuperados normalmente usando a recuperação de intervalo. Se o intervalo 101-200 for solicitado, **IDirectorySearch::GetColumn** retornará **A COLUNA DE ANÚNCIOS NÃO \_ \_ \_ \_ DEFINIDA.** Esse problema pode ser evitado usando o [**método IDirectorySearch::GetNextColumnName.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) Normalmente, **GetNextColumnName retornará** a cadeia de caracteres de consulta original. No entanto, quando o intervalo solicitado exceder o número de valores restantes, **GetNextColumnName** retornará uma versão modificada da cadeia de caracteres de consulta substituindo o valor de intervalo alto pelo curinga \* ''. No exemplo acima, a primeira consulta seria executada com uma cadeia de caracteres de atributo "member;range=0-100" e **GetNextColumnName** retornará "member;range=0-100". Na segunda consulta, a cadeia de caracteres de atributo seria "member;range=101-200", mas **GetNextColumnName** retornará "member;range=101- \* ". Esse caso pode ser determinado comparando a cadeia de caracteres de atributo original com o resultado de **GetNextColumnName**. Se as cadeias de caracteres são diferentes, o último bloco de valores deve ser solicitado novamente com o curinga de intervalo.

Para obter mais informações e um exemplo de código que mostra como usar a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para recuperação de intervalo, consulte Código de exemplo para variar com [IDirectorySearch](example-code-for-ranging-with-idirectorysearch.md).

 

 




