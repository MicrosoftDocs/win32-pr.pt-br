---
title: Armazenando em cache o resultado (lado do cliente)
description: O armazenamento em cache do lado do cliente armazena o conjunto de resultados na memória do cliente, fornecendo aprimoramentos de desempenho para o lado do cliente.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Caching do resultado (lado do cliente) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915911"
---
# <a name="caching-the-result-client-side"></a>Armazenando em cache o resultado (lado do cliente)

O armazenamento em cache do lado do cliente armazena o conjunto de resultados na memória do cliente, fornecendo aprimoramentos de desempenho para o lado do cliente. Um cliente pode revisitar um objeto repetidamente sem várias viagens para o servidor. Por padrão, a ADSI armazena em cache o conjunto de resultados para os clientes. Isso permite que a ADSI forneça aos clientes suporte ao cursor do tipo SQL. Você pode iterar em um determinado conjunto de resultados várias vezes.

A ADSI também permite que os clientes desliguem o cache para reduzir os requisitos de memória. Se o cache do lado do cliente estiver desabilitado, o cliente não manterá o conjunto de resultados na memória. Cada linha é liberada depois que o aplicativo a recupera. Desabilitar o armazenamento em cache do lado do cliente pode ser útil para diminuir os requisitos de memória do lado do cliente nesses casos, como quando você pretende fazer uma passagem única do conjunto de resultados. No entanto, quando os clientes optam por não armazenar o resultado em cache, eles oferecem suporte ao cursor.

Para obter mais informações sobre o cache de resultados com uma interface de pesquisa específica, consulte:

-   [Cache de resultados com IDirectorySearch](result-caching-with-idirectorysearch.md)
-   [Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 




