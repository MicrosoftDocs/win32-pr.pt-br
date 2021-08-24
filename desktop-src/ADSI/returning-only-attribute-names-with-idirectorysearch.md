---
title: Retornando apenas nomes de atributo com IDirectorySearch
description: Você pode executar uma pesquisa para determinar qual tipo de dados está disponível para um objeto específico.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Retornando apenas nomes de atributo com IDirectorySearch ADSI
- ADSI, Search, IDirectorySearch, outras opções de pesquisa, retornando apenas nomes de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b9c69a99cad0ece5c660ba45954fe537abe69cfa88947b52b0d69d7833b4e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444006"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Retornando apenas nomes de atributo com IDirectorySearch

Você pode executar uma pesquisa para determinar qual tipo de dados está disponível para um objeto específico. Nesse caso, você só está interessado nos nomes de atributos, não nos valores de atributo do objeto . A **opção ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** faz com que o servidor retorne apenas os nomes de atributo e não os valores de atributo. No entanto, o conjunto de resultados inclui apenas os atributos que têm valores atribuídos. Por exemplo, considere um objeto com os seguintes atributos:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Quando a **opção ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** é definida, o conjunto de resultados inclui:

``` syntax
name
sn
department
phone
```

O padrão é para valores de atributo e nomes a serem retornados.

Para recuperar apenas nomes de atributo, de definir uma opção de pesquisa **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** com um valor **\_ BOOLEAN ADSTYPE** **de TRUE** na matriz [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o [**método IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

O exemplo de código a seguir mostra como recuperar apenas nomes de atributo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Para obter mais informações e um exemplo de código que mostra como usar a opção de pesquisa **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY,** consulte Código de exemplo para pesquisar [atributos](example-code-for-searching-for-attributes.md).

 

 




