---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas do assistente de projetor.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Solução de problemas do assistente do projetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761217"
---
# <a name="troubleshooting-the-projector-wizard"></a>Solução de problemas do assistente do projetor

O assistente do projetor:

-   Sempre usa WS-Discovery UDP para descoberta de dispositivo
-   Sempre usa HTTP para troca de metadados
-   Às vezes usa a descoberta direcionada

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o assistente do projetor.

**Para solucionar problemas do assistente de projetor**

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

 

 



