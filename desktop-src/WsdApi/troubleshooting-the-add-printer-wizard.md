---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas do assistente para adicionar impressora.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Solução de problemas do assistente para adicionar impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760508"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Solução de problemas do assistente para adicionar impressora

O assistente para adicionar impressora:

-   Sempre usa WS-Discovery UDP para descoberta de dispositivo
-   Sempre inicia uma conexão HTTP ou HTTPS para a troca de metadados
-   Às vezes usa a descoberta direcionada
-   Às vezes usa um canal seguro (HTTPS) para troca de metadados

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o assistente para adicionar impressora.

**Para solucionar problemas do assistente para adicionar impressora**

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
</dt> <dt>

[Solucionando problemas de aplicativos usando a descoberta direcionada](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



