---
title: Pesquisas síncronas e assíncronas com IDirectorySearch
description: Quando você executa uma pesquisa usando a interface IDirectorySearch, o método IDirectorySearch ExecuteSearch não envia a solicitação de pesquisa para o servidor.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Pesquisas síncronas e assíncronas com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, pesquisas síncronas e assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363645"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Pesquisas síncronas e assíncronas com IDirectorySearch

Quando você executa uma pesquisa usando a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , o método [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) não envia a solicitação de pesquisa para o servidor. Esse método salva apenas os parâmetros de pesquisa. A solicitação de pesquisa é realmente enviada quando você chama [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).

Para pesquisas de Active Directory, a principal diferença entre síncrona e assíncrona é quando a primeira linha do resultado é retornada, ou seja, quando a primeira chamada [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) retorna.

Em uma pesquisa síncrona, se a paginação não estiver habilitada, a primeira linha será retornada quando o servidor tiver construído e retornado o conjunto de resultados inteiro para o cliente. Se a paginação estiver habilitada, a primeira linha será retornada quando a primeira página do conjunto de resultados for retornada.

Em uma pesquisa assíncrona, se a paginação não estiver habilitada, a primeira linha será retornada quando o servidor tiver construído a primeira linha do conjunto de resultados. Se a paginação estiver habilitada, a primeira linha será retornada quando a primeira página do conjunto de resultados for retornada.

O tipo de pesquisa padrão é síncrono. Para especificar uma pesquisa assíncrona, defina uma opção de pesquisa **\_ \_ assíncrona do ADS SEARCHPREF** com um valor **\_ booliano de ADSTYPE** **true** na matriz de [**informações de \_ SEARCHPREF \_ do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Essa operação é mostrada no exemplo de código a seguir.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




