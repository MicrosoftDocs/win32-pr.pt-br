---
title: Retornando somente nomes de atributo com IDirectorySearch
description: Você pode executar uma pesquisa para determinar que tipo de dados está disponível para um determinado objeto.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Retornando somente nomes de atributo com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, retornando apenas nomes de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105749383"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Retornando somente nomes de atributo com IDirectorySearch

Você pode executar uma pesquisa para determinar que tipo de dados está disponível para um determinado objeto. Nesse caso, você está interessado apenas nos nomes dos atributos, não nos valores de atributo do objeto. A opção **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ somente** faz com que o servidor retorne apenas os nomes de atributo e não os valores de atributo. No entanto, o conjunto de resultados inclui apenas os atributos que têm valores atribuídos. Por exemplo, considere um objeto com os seguintes atributos:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Quando a opção **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ somente** é definida, o conjunto de resultados inclui:

``` syntax
name
sn
department
phone
```

O padrão é que os valores de atributo e os nomes sejam retornados.

Para recuperar apenas os nomes de atributo, defina uma opção de pesquisa **\_ \_ \_ somente ADS SEARCHPREF ATTRIBTYPES** com um valor **\_ booliano de ADSTYPE** **true** na matriz de [**informações do ADS \_ \_ SEARCHPREF**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

O exemplo de código a seguir mostra como recuperar somente nomes de atributo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Para obter mais informações e um exemplo de código que mostra como usar a opção de pesquisa **\_ \_ \_ somente ATTRIBTYPES do ADS SEARCHPREF** , consulte o [código de exemplo para pesquisar atributos](example-code-for-searching-for-attributes.md).

 

 




