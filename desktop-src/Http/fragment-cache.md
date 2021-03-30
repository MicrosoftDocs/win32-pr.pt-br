---
title: Cache de fragmento
description: A API do servidor HTTP fornece a funcionalidade para que os usuários armazenem fragmentos de dados em um cache para uso na forma de respostas HTTP rapidamente.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3979fb03c4f8898644329fd27eafb7007adbcc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916060"
---
# <a name="fragment-cache"></a>Cache de fragmento

A API do servidor HTTP fornece a funcionalidade para que os usuários armazenem fragmentos de dados em um cache para uso na forma de respostas HTTP rapidamente.

Os fragmentos podem ser adicionados ao cache chamando a função [**HttpAddFragmentToCache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) . Um fragmento é identificado por uma URL contida no parâmetro *pUrlPrefix* . Uma chamada para essa função com a URL de um fragmento existente substitui o fragmento existente.

Um fragmento pode ser excluído ou substituído pelo proprietário da fila de solicitações que inicialmente adicionou o fragmento. A função [**HttpFlushResponseCache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) chamada com um URLPrefix exclui todos os fragmentos dentro desse prefixo, bem como os descendentes hierárquicos desse URLPrefix. A função [**HttpReadFragmentFromCache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) lê em todo o fragmento ou em um intervalo de bytes especificado dentro do fragmento.

> [!Note]  
> A adição de um fragmento ao cache não garante que ele esteja disponível para chamadas futuras para enviar uma resposta. As entradas de cache de fragmento podem ficar indisponíveis a qualquer momento. Uma chamada que usa um fragmento que não está disponível falha. Os aplicativos que usam o cache de fragmento devem estar preparados para lidar com essa falha.

 

## <a name="sending-a-response-with-a-fragment"></a>Enviando uma resposta com um fragmento

Os fragmentos podem ser usados para formar todas ou partes de um corpo de entidade de respostas HTTP. Você pode enviar uma resposta e corpo de entidade em uma chamada para a função [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) especificando uma matriz de estruturas de [**\_ \_ partes de dados http**](/windows/desktop/api/Http/ns-http-http_data_chunk) na estrutura de [**\_ resposta http**](http-response.md) .

Uma [**\_ \_ parte de dados http**](/windows/desktop/api/Http/ns-http-http_data_chunk) pode especificar um bloco de memória, um identificador para um arquivo já aberto ou uma entrada de cache de fragmento. Elas correspondem aos tipos **de \_ \_ partes de dados http** : **HttpDataChunkFromMemory**, **HttpDataChunkFromFileHandle** e **HttpDataChunkFromFragmentCache**, respectivamente. As respostas completas no cache HTTP também podem ser usadas como fragmentos na estrutura [**de \_ resposta http**](http-response.md) , embora essa prática não seja recomendada.

A estrutura de [**\_ resposta http**](http-response.md) contém um ponteiro para uma matriz de estruturas de [**\_ \_ partes de dados http**](/windows/desktop/api/Http/ns-http-http_data_chunk) que compõem o corpo da entidade da resposta. A estrutura de **\_ resposta http** também contém uma contagem correspondente que especifica a dimensão da matriz de estruturas de **\_ \_ partes de dados http** . O valor de HttpDataChunkFromFragmentCache na estrutura de **\_ \_ partes de dados http** especifica o tipo de cache de fragmento da parte de dados. A estrutura da **\_ \_ parte de dados http** também especifica o nome do fragmento.

Uma resposta que contém um fragmento armazenado em cache falha com um \_ caminho \_ de erro não \_ encontrado se qualquer uma das entradas de cache de fragmento não estiver disponível. Como não há garantia de que as entradas do cache do fragmento estejam disponíveis, os aplicativos devem estar preparados para lidar com esse caso. Uma maneira de lidar com esse caso é tentar adicionar novamente a entrada do cache de fragmento e reenviar a resposta. Se ocorrerem falhas repetidas, o aplicativo poderá usar partes de dados armazenadas em buffers de memória em vez de entradas de cache de fragmento.

As entradas de cache de fragmento também podem ser especificadas na função [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) . O fragmento é adicionado ao corpo da entidade na estrutura [**da \_ \_ parte de dados http**](/windows/desktop/api/Http/ns-http-http_data_chunk) , conforme descrito acima. Novamente, o envio poderá falhar se qualquer uma das entradas de cache de fragmento especificadas não estiver disponível.

 

 




