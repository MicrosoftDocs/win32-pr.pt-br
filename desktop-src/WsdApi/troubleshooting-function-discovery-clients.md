---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas de clientes de descoberta de função.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Solucionando problemas de clientes de descoberta de função
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647691"
---
# <a name="troubleshooting-function-discovery-clients"></a>Solucionando problemas de clientes de descoberta de função

Clientes de descoberta de função:

-   Sempre usar WS-Discovery UDP para descoberta de dispositivo
-   Sempre iniciar conexões HTTP ou HTTPS para troca de metadados
-   Às vezes, use a descoberta direcionada
-   Às vezes, use um canal seguro (HTTPS) para troca de metadados

A lista a seguir mostra a sequência típica de mensagens enviadas e recebidas por clientes de descoberta de função. Nem todas as mensagens são obrigatórias.

1.  O cliente envia uma mensagem de [investigação](probe-message.md) para descobrir dispositivos e serviços. Se o cliente estiver usando a descoberta direcionada, essa mensagem será enviada por HTTP ou HTTPS; caso contrário, a mensagem será enviada por multicast UDP para a porta 3702.
2.  O cliente recebe mensagens [ProbeMatches](probematches-message.md) de dispositivos ou serviços correspondentes. As mensagens de descoberta direcionadas são enviadas por HTTP ou HTTPS; caso contrário, essas mensagens são enviadas por UDP unicast e originadas da porta 3702.
3.  Se nenhum XAddrs tiver sido incluído na mensagem ProbeMatches, o cliente enviará uma mensagem de [resolução](resolve-message.md) por multicast UDP para a porta 3702.
4.  Se uma mensagem de [resolução](resolve-message.md) for enviada, o cliente receberá uma mensagem [ResolveMatches](resolvematches-message.md) de serviços correspondentes. Essa mensagem é enviada por UDP unicast da porta 3702 para a porta na qual a mensagem de resolução foi originada.
5.  O cliente envia uma mensagem [Get](get--metadata-exchange--http-request-and-message.md) para solicitar metadados do dispositivo ou serviço. Essa mensagem é enviada por HTTP ou HTTPS.
6.  O cliente recebe uma mensagem [GetResponse](getresponse--metadata-exchange--message.md) com os metadados do dispositivo ou do serviço. Essa mensagem é enviada por HTTP ou HTTPS.

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um cliente de descoberta de função.

**Para solucionar problemas de um cliente de descoberta de função**

1.  Se a descoberta direcionada for usada, [solucione o problema de descoberta direcionada](troubleshooting-applications-using-directed-discovery.md).
2.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
3.  [Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
7.  [Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



