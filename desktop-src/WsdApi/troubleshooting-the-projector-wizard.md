---
description: Lista os procedimentos de diagnóstico a usar ao solucionar problemas do Assistente de Projetor.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Solução de problemas do Assistente de Projetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5767e9827174d2d8135ac6dfb96c335d49acb82f0a0162b06f22a89c4dbdebef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856066"
---
# <a name="troubleshooting-the-projector-wizard"></a>Solução de problemas do Assistente de Projetor

O Assistente de Projetor:

-   Sempre usa o WS-Discovery UDP para descoberta de dispositivo
-   Sempre usa HTTP para troca de metadados
-   Às vezes, usa a descoberta direcionada

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o Assistente de Projetor.

**Para solucionar problemas do Assistente de Projetor**

1.  Se a descoberta direcionada for usada, [solucione problemas de descoberta direcionada.](troubleshooting-applications-using-directed-discovery.md)
2.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
3.  [Use um host genérico e um cliente para ODP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
4.  [Use o Cliente de Depuração do WSD para verificar o tráfego multicast.](using-wsddebug-client-to-verify-multicast-traffic.md)
5.  [Inspecione rastreamentos de rede para WS-Discovery UDP.](inspecting-network-traces-for-udp-ws-discovery.md)
6.  [Use um host genérico e um cliente para troca de metadados HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
7.  [Use o registro em log do WinHTTP para verificar Obter tráfego](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Inspecione os rastreamentos de rede para troca de metadados HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em Habilitando o rastreamento [WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



