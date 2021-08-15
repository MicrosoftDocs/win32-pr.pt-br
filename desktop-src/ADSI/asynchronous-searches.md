---
title: Pesquisas assíncronas
description: A habilitação da pesquisa assíncrona (assíncrona) resulta em uma chamada para GetFirstRow ou na primeira chamada para blocos GetNextRow até que a primeira entrada seja retornada do servidor.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- ADSI de Pesquisas Assíncronas
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

A habilitação da pesquisa assíncrona (assíncrona) resulta em uma chamada para **GetFirstRow** ou na primeira chamada para blocos **GetNextRow** até que a primeira entrada seja retornada do servidor. Ou seja, se a pesquisa no servidor exigir muito tempo, os primeiros resultados serão retornados rapidamente. Isso pode ajudar ao preencher uma caixa de listagem com os resultados da pesquisa. Os resultados da pesquisa são exibidos à medida que são retornados.

Se a assíncrona estiver desabilitada, a primeira chamada para **GetFirstRow** ou **GetNextRow** bloqueará até que o servidor compute todo o conjunto de resultados e retorne. Somente então é a primeira linha retornada. Isso não será recomendado se o conjunto de resultados for grande.

Se a paging e a assíncrona estão habilitadas, a primeira chamada para **GetFirstRow** ou **GetNextRow** será bloqueado até que o servidor gere e envie a primeira página de resultados. Se um tamanho de página razoável tiver sido definido, os resultados serão exibidos imediatamente. Mais importante, se espera-se que os resultados da pesquisa sejam muito grandes e você pesquise uma entrada específica, não será necessário solicitar mais resultados do servidor depois de encontrar as entradas que lhe interessam.

Uma pesquisa assíncrona páginada fornece um controle fino de uma pesquisa. Isso é útil se os resultados da pesquisa podem ser muito grandes e exigem muito tempo do servidor.

Para obter mais informações sobre como usar pesquisas assíncronas com uma interface de pesquisa específica, consulte:

-   [Pesquisas síncronas e assíncronas com IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Pesquisando com objetos ActiveX dados](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




