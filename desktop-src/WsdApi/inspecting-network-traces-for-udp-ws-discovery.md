---
description: Qualquer analisador de pacotes de rede que pode exibir pacotes brutos pode ser usado para inspecionar pacotes UDP WS-Discovery pacotes. Monitor de Rede da Microsoft 3 (Netmon) é recomendado. Para obter mais informações sobre o Netmon, consulte Downloading Netmon and Sample DPWS Filters.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Inspecionando rastreamentos de rede para WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce21e2943a37640eb091aa03c02eba0886164166b2959e31e897ee788424cd41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920750"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Inspecionando rastreamentos de rede para WS-Discovery

Qualquer analisador de pacotes de rede que pode exibir pacotes brutos pode ser usado para inspecionar pacotes UDP WS-Discovery pacotes. Monitor de Rede da Microsoft 3 (Netmon) é recomendado. Para obter mais informações sobre o Netmon, consulte [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).

**Para inspecionar rastreamentos de rede para WS-Discovery UDP**

1.  Configure o host e o cliente para executar na rede (ou seja, certifique-se de que o host e o cliente operarão em diferentes máquinas).
2.  Instale o analisador de pacote (Netmon) no cliente ou no host.
3.  Configure o analisador de pacotes para capturar o tráfego no adaptador de rede que conecta o host e o cliente.
4.  Reproduza a falha iniciando o host e o cliente ou pressionando F5 no Gerenciador de Rede.
5.  Filtre os resultados para isolar WS-Discovery tráfego. Para exibir filtros Netmon de exemplo, consulte [Baixando o Netmon e exemplos de filtros DPWS](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Esta etapa é opcional.

     

6.  Verifique se as mensagens enviadas entre o cliente e o host atendem aos requisitos básicos de tráfego.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Verificar se as mensagens atendem aos requisitos de tráfego

Os clientes e hosts WSDAPI devem enviar mensagens em conformidade com os critérios a seguir. Para obter informações gerais sobre padrões de mensagem, consulte [Descoberta e metadados Exchange padrões de mensagem](discovery-and-metadata-exchange-message-patterns.md).

-   [As](probe-message.md) mensagens de investigação devem ser enviadas pelo multicast UDP para a porta 3702.
-   O **elemento Types** de uma mensagem [Probe](probe-message.md) deve estar presente e não deve estar vazio. Ele deve conter os tipos aos quais um host responderá.
-   Uma [mensagem ProbeMatches](probematches-message.md) deve ser enviada unicast para a porta UDP da qual [a Investigação](probe-message.md) foi enviada.
-   O **elemento RelatesTo** de uma [mensagem ProbeMatches](probematches-message.md) deve estar presente e não deve estar vazio. Seu valor deve corresponder ao valor do **elemento MessageId** da mensagem [Probe](probe-message.md) correspondente.
-   Se um **elemento XAddrs** tiver sido incluído na mensagem [ProbeMatches,](probematches-message.md) os endereços de transporte fornecidos deverão ser validados. Para obter mais informações, consulte [Regras de validação XAddr](xaddr-validation-rules.md).
-   Uma [mensagem ProbeMatches](probematches-message.md) deve ser enviada dentro de 4 segundos da mensagem [probe](probe-message.md) correspondente. O Windows firewall pode soltar uma mensagem ProbeMatches enviada mais de 4 segundos após uma mensagem probe.
-   Se nenhum elemento **XAddrs** tiver sido incluído na mensagem [ProbeMatches](probematches-message.md) e o cliente ou host enviar uma mensagem HTTP (como uma [](resolve-message.md) solicitação de troca obter metadados ou uma mensagem de serviço), o cliente ou host deverá enviar uma mensagem Resolver por multicast UDP para [a](get--metadata-exchange--http-request-and-message.md) porta 3702.
-   Se uma [mensagem Resolver](resolve-message.md) for enviada, uma mensagem [ResolveMatches](resolvematches-message.md) deverá ser enviada unicast para a porta UDP da qual a mensagem Resolver foi enviada.
-   Uma [mensagem ResolveMatches](resolvematches-message.md) deve ser enviada dentro de 4 segundos da mensagem [Resolver](resolve-message.md) correspondente. O Windows firewall pode soltar um ResolveMatchesmessage enviado mais de 4 segundos após uma mensagem Resolver.

Se as mensagens enviadas pelo programa não estão em conformidade com esses requisitos de mensagem, a causa do problema foi identificada com êxito e nenhuma outra etapa de solução de problemas é necessária. Reescreva o programa para que ele gere mensagens compatíveis e teste novamente o programa.

Se a origem do problema ainda não puder ser identificada, entre em contato com o suporte da Microsoft para saber mais. Antes de entrar em contato com o suporte, colete os arquivos de log apropriados para ajudar a identificar a causa raiz do problema. Para obter mais informações, consulte [Habilitando o rastreamento WSDAPI.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Procedimentos de diagnóstico do WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Baixando o Netmon e exemplos de filtros DPWS](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



