---
title: Pesquisas assíncronas
description: A habilitação da pesquisa assíncrona (Async) resulta em uma chamada para GetFirstRow ou a primeira chamada para blocos GetNextRow até que a primeira entrada seja retornada do servidor.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- ADSI de pesquisas assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bca36a30b3b0a46f983da54ecaee753a4b15a455b0e69f9399eacdec68aecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082780"
---
# <a name="asynchronous-searches"></a>Pesquisas assíncronas

A habilitação da pesquisa assíncrona (Async) resulta em uma chamada para **GetFirstRow** ou a primeira chamada para blocos **GetNextRow** até que a primeira entrada seja retornada do servidor. Ou seja, se a pesquisa no servidor exigir muito tempo, os primeiros resultados serão retornados rapidamente. Isso pode ajudar ao preencher uma caixa de listagem com os resultados da pesquisa. Os resultados da pesquisa são exibidos à medida que são retornados.

Se Async estiver desabilitado, a primeira chamada para **GetFirstRow** ou **GetNextRow** será bloqueada até que o servidor Calcule todo o conjunto de resultados e retorna. Somente a primeira linha é retornada. Isso não é recomendado se o conjunto de resultados deve ser grande.

Se a paginação e a Async estiverem habilitadas, a primeira chamada para **GetFirstRow** ou **GetNextRow** será bloqueada até que o servidor gere e envie a primeira página de resultados. Se um tamanho de página razoável tiver sido definido, os resultados aparecerão imediatamente. Mais importante, se os resultados da pesquisa forem muito grandes e você pesquisar por uma entrada específica, não será necessário solicitar mais resultados do servidor depois de encontrar as entradas que lhe interessam.

A pesquisa assíncrona paginável fornece um controle fino de uma pesquisa. Isso será útil se os resultados da pesquisa puderem ser muito grandes e exigirem tempo extensivo do servidor.

Para obter mais informações sobre como usar pesquisas assíncronas com uma interface de pesquisa específica, consulte:

-   [Pesquisas síncronas e assíncronas com IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




