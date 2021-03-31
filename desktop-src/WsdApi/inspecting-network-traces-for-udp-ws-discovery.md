---
description: Qualquer analisador de pacotes de rede que possa exibir pacotes brutos pode ser usado para inspecionar pacotes UDP WS-Discovery. O Monitor de Rede da Microsoft 3 (Netmon) é recomendado. Para obter mais informações sobre o Netmon, consulte baixando os filtros do Netmon e do DPWS de exemplo.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Inspecionando rastreamentos de rede para UDP WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f4acd79588ef48c7f8e1ace2a44c9a3458475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169800"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Inspecionando rastreamentos de rede para UDP WS-Discovery

Qualquer analisador de pacotes de rede que possa exibir pacotes brutos pode ser usado para inspecionar pacotes UDP WS-Discovery. O Monitor de Rede da Microsoft 3 (Netmon) é recomendado. Para obter mais informações sobre o Netmon, consulte [baixando os filtros do Netmon e do DPWS de exemplo](downloading-netmon-and-sample-dpws-filters.md).

**Para inspecionar rastreamentos de rede para o WS-Discovery de UDP**

1.  Configure o host e o cliente para serem executados na rede (ou seja, certifique-se de que o host e o cliente funcionarão em computadores diferentes).
2.  Instale o analisador de pacotes (Netmon) no cliente ou no host.
3.  Configure o analisador de pacotes para capturar o tráfego no adaptador de rede que está conectando o host e o cliente.
4.  Reproduza a falha iniciando o host e o cliente ou pressionando F5 no Gerenciador de rede.
5.  Filtre os resultados para isolar o tráfego de WS-Discovery. Para exibir os filtros de exemplo do Netmon, consulte [baixando os filtros de DPWS de Netmon e de exemplo](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Esta etapa é opcional.

     

6.  Verifique se as mensagens enviadas entre o cliente e o host atendem aos requisitos básicos de tráfego.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verificando se as mensagens atendem aos requisitos de tráfego

Os clientes e hosts WSDAPI devem enviar mensagens que estejam em conformidade com os critérios a seguir. Para obter informações gerais sobre os padrões de mensagem, consulte [descoberta e padrões de mensagem de troca de metadados](discovery-and-metadata-exchange-message-patterns.md).

-   As mensagens de [investigação](probe-message.md) devem ser enviadas por multicast UDP para a porta 3702.
-   O elemento **Types** de uma mensagem de [investigação](probe-message.md) deve estar presente e não deve estar vazio. Ele deve conter os tipos aos quais um host responderá.
-   Uma mensagem [ProbeMatches](probematches-message.md) deve ser enviada unicast para a porta UDP da qual a [investigação](probe-message.md) foi enviada.
-   O elemento **RelatesTo** de uma mensagem [ProbeMatches](probematches-message.md) deve estar presente e não deve estar vazio. Seu valor deve corresponder ao valor do elemento **MessageId** da mensagem de [investigação](probe-message.md) correspondente.
-   Se um elemento **XAddrs** foi incluído na mensagem [ProbeMatches](probematches-message.md) , os endereços de transporte fornecidos devem ser validados. Para obter mais informações, consulte [XAddr Validation Rules](xaddr-validation-rules.md).
-   Uma mensagem [ProbeMatches](probematches-message.md) deve ser enviada dentro de 4 segundos da mensagem de [investigação](probe-message.md) correspondente. O Firewall do Windows pode descartar uma mensagem ProbeMatches enviada mais de 4 segundos após uma mensagem de investigação.
-   Se nenhum elemento **XAddrs** foi incluído na mensagem [ProbeMatches](probematches-message.md) , e o cliente ou host enviará uma mensagem http (como uma solicitação de troca de metadados [Get](get--metadata-exchange--http-request-and-message.md) ou uma mensagem de serviço), o cliente ou o host deverá enviar uma mensagem de [resolução](resolve-message.md) por multicast UDP para a porta 3702.
-   Se uma mensagem de [resolução](resolve-message.md) for enviada, uma mensagem [ResolveMatches](resolvematches-message.md) deverá ser enviada por unicast para a porta UDP da qual a mensagem de resolução foi enviada.
-   Uma mensagem [ResolveMatches](resolvematches-message.md) deve ser enviada dentro de 4 segundos da mensagem de [resolução](resolve-message.md) correspondente. O Firewall do Windows pode cancelar um ResolveMatchesmessage enviado mais de 4 segundos após uma mensagem de resolução.

Se as mensagens enviadas pelo programa não estiverem em conformidade com esses requisitos de mensagem, a causa do problema foi identificada com êxito e nenhuma outra etapa de solução de problemas será necessária. Reescreva o programa para que ele gere mensagens de conformidade e teste o programa novamente.

Se a origem do problema ainda não puder ser identificada, entre em contato com o suporte da Microsoft para obter assistência. Antes de entrar em contato com o suporte, colete os arquivos de log apropriados para ajudar a identificar a causa raiz do problema. Para obter mais informações, consulte [habilitando o rastreamento WSDAPI](enabling-wsdapi-tracing.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Baixando os filtros de DPWS e de exemplo do Netmon](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



