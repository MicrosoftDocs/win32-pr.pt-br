---
description: Informações do AppSequence contidas WS-Discovery mensagens de resposta e comunicado (Hello, ProbeMatches e ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Regras de validação do AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f2acec9d9d3858b5d68b0240499d95dba059ac1bcac745f1dc69bebc2056a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738639"
---
# <a name="appsequence-validation-rules"></a>Regras de validação do AppSequence

Informações do AppSequence contidas WS-Discovery mensagens de resposta e comunicado[(Hello,](hello-message.md) [ProbeMatches](probematches-message.md)e [ResolveMatches).](resolvematches-message.md) Essas informações são processadas e validadas pelo WSDAPI antes que essas mensagens sejam passadas para componentes acima da pilha (como Gerenciador de Rede ou um aplicativo que chama o WSDAPI).

O XML a seguir mostra um elemento AppSequence de exemplo. O prefixo wsd refere-se ao namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

O WSDAPI ignora mensagens desleixadas. Para cada dispositivo (identificado exclusivamente pelo Endereço do Ponto de Extremidade no Corpo SOAP), o WSDAPI ignora todas as mensagens com um AppSequence MessageNumber menor do que a última mensagem vista.

O WSDAPI ignora anúncios de XAddr desadiciosos. Se AppSequence InstanceId for menor que a última InstanceId vista, o WSDAPI ignorará os XAddrs anunciados no corpo SOAP. Além disso, se a InstanceId for igual à anterior, mas a MetadataVersion for inferior à última MetadataVersion, o WSDAPI ignorará os XAddrs.

O WSDAPI ignora mensagens WS-Discovery duplicadas. Se duas mensagens WS-Discovery idênticas são enviadas ao WSDAPI, somente a primeira recebida será processada. Normalmente, isso é relevante apenas para aplicativos que chamam diretamente nas interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) ou [**IWSDiscoveryProvider.**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Padrões de mensagem de descoberta e Exchange metadados](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



