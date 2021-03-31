---
description: Lista os procedimentos de diagnóstico a serem usados ao solucionar problemas do Gerenciador de rede.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Solucionando problemas do Gerenciador de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920900"
---
# <a name="troubleshooting-the-network-explorer"></a>Solucionando problemas do Gerenciador de rede

O Gerenciador de rede:

-   Sempre usa WS-Discovery UDP para descoberta de dispositivo
-   Sempre inicia uma conexão HTTP ou HTTPS para a troca de metadados
-   Às vezes usa um canal seguro (HTTPS) para troca de metadados

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o Gerenciador de rede.

**Para solucionar problemas do Gerenciador de rede**

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Use o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspecione os rastreamentos de rede para o WS-Discovery de UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspecione os rastreamentos de rede para a troca de metadados http](inspecting-network-traces-for-http-metadata-exchange.md).

O Gerenciador de rede usa a [descoberta de função](/previous-versions/windows/desktop/fundisc/fd-portal) para enumerar dispositivos de rede. Para obter mais informações sobre solução de problemas, consulte [Solucionando problemas de clientes de descoberta de função](troubleshooting-function-discovery-clients.md).

Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solucionando problemas de clientes de descoberta de função](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
