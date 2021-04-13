---
description: 'Saiba mais sobre: conformidade de especificação de WS-Discovery'
ms.assetid: b795a385-b48d-4a16-9d91-e48bca120572
title: Conformidade de especificação de WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcae062448b1913f0cc62dff3b6c86b98280a902
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370553"
---
# <a name="ws-discovery-specification-compliance"></a>Conformidade de especificação de WS-Discovery

O [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) descreve como executar as seguintes tarefas:

-   Anunciar a disponibilidade de serviços na sub-rede local
-   Pesquisar serviços na sub-rede
-   Localizar um serviço referenciado anteriormente

Para fazer isso, WS-Discovery define mensagens de 2 1 vias, [saudação](hello-message.md) e [adeus](bye-message.md), e duas mensagens de pesquisa bidirecionais, [teste](probe-message.md) e [resolução](resolve-message.md).

WS-Discovery também fornece endereços e uma porta reservada para a descoberta local do link IPv4 e IPv6. A especificação também permite que associações alternativas sejam definidas em outro lugar, como a investigação sobre a associação HTTP definida no [perfil de dispositivos para serviços Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).

A especificação de WS-Discovery descreve a funcionalidade facultativos usando os termos podem ou deve estar em uma determinada recomendação ou restrição de implementação. A funcionalidade omitida pode ser a funcionalidade descrita conforme necessário na especificação de WS-Discovery que não foi implementada pelo WSDAPI ou pode ser a funcionalidade que o WSDAPI implementou em um método diferente daquele especificado na especificação WS-Discovery.

Este tópico descreve como WS-Discovery restrições, requisitos e a funcionalidade facultativos são tratados pela implementação do WSDAPI. Este tópico é melhor lido em conjunto com a especificação de WS-Discovery.

## <a name="ws-discovery-and-soap-over-udp-support"></a>Suporte a WS-Discovery e SOAP-over-UDP

No SOAP-over-UDP, a seção 3,2 especifica que a mensagem UDP deve caber em um datagrama de 64K. O WSDAPI aceitará mensagens UDP de 64K, mas a restrição DPWS de tamanho máximo de \_ envelope \_ (32K) restringirá o tamanho da mensagem. Conforme exigido pelo [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), o WSDAPI dá suporte aos padrões de mensagem descritos na seção 4.

O WSDAPI pode ser configurado para dar suporte ao modelo de segurança nas seções 7 e 8. Quando configurado, o WSDAPI assinará mensagens de WS-Discovery de saída e validará as assinaturas em mensagens de entrada.

O WSDAPI implementa o algoritmo de retransmissão definido no apêndice I conforme alterado pelo DPWS apêndice I.

No WS-Discovery, o WSDAPI usa os endereços especificados na seção 2,4. O WSDAPI estende \_ \_ o atraso máximo do aplicativo da seção 2,4, mas não da extensão, conforme definido no apêndice DPWS I. Para obter mais informações sobre o \_ atraso máximo do aplicativo \_ , consulte [funcionalidade adicional de WS-Discovery](additional-ws-discovery-functionality.md).

WS-Discovery descreve a `uuid:` recomendação de formato de URI na seção 2,6, mas o WSDAPI substitui essa recomendação. Em vez disso, o WSDAPI usa o `urn:uuid:` formato de URI descrito em DPWS.

A seção 3 de WS-Discovery descreve como um cliente interage com um proxy de descoberta. O WSDAPI não reconhece essa interação e ignora anúncios de proxies de descoberta. No Windows 7, o WSDAPI implementa uma extensão privada para o protocolo WS-Discovery, WS-Discovery extensões remotas, para permitir que os clientes de descoberta pesquisem serviços distribuídos em várias redes diferentes enviando solicitações para proxies centralizados. Para obter mais informações, consulte [funcionalidade adicional de WS-Discovery](additional-ws-discovery-functionality.md).

A seção 4,1, parágrafo 3 de WS-Discovery requer que um temporizador decorra antes que uma mensagem de [saudação](hello-message.md) seja enviada. A API de hospedagem não espera antes de enviar uma mensagem de saudação. Se um cenário exigir um atraso antes que uma mensagem de saudação seja enviada, o desenvolvedor do aplicativo deverá implementar uma espera.

O WSDAPI implementa todas as mensagens descritas em WS-Discovery seções 4, 5 e 6. O WSDAPI também impõe o \_ tempo limite de correspondência descrito na seção 7, conforme emendado pelo apêndice DPWS I. o WSDAPI protege somente contra "replay" das considerações seguras na seção 9.

O WSDAPI implementa o sequenciamento de aplicativos, conforme descrito em WS-Discovery apêndice I.

 

 



