---
description: AppSequence informações contidas em mensagens de anúncio e resposta do WS-Discovery (Olá, ProbeMatches e ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Regras de validação do AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505707"
---
# <a name="appsequence-validation-rules"></a>Regras de validação do AppSequence

AppSequence informações contidas em mensagens de anúncio e resposta do WS-Discovery ([Olá](hello-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md)). Essas informações são processadas e validadas pelo WSDAPI antes que essas mensagens sejam passadas para os componentes acima da pilha (como o Gerenciador de rede ou um aplicativo chamando o WSDAPI).

O XML a seguir mostra um exemplo de elemento AppSequence. O prefixo WSD refere-se ao namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

O WSDAPI ignora mensagens obsoletas. Para cada dispositivo (identificado exclusivamente pelo endereço do ponto de extremidade no corpo SOAP), o WSDAPI ignora todas as mensagens com um AppSequence MessageNumber inferior à última mensagem vista.

O WSDAPI ignora os anúncios de XAddr obsoletos. Se a InstanceId AppSequence for menor do que a última InstanceId vista, o WSDAPI ignorará o XAddrs anunciado no corpo SOAP. Além disso, se a InstanceId for a mesma que a anterior, mas a MetadataVersion for menor do que a última MetadataVersion, o WSDAPI ignorará o XAddrs.

O WSDAPI ignora mensagens de WS-Discovery duplicadas. Se duas mensagens de WS-Discovery idênticas forem enviadas para WSDAPI, somente o primeiro recebimento será processado. Isso geralmente é relevante apenas para aplicativos que chamam diretamente para as interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) ou [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Padrões de mensagem de troca de metadados e descoberta](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



