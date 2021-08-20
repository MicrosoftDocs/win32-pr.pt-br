---
description: Lista os procedimentos de diagnóstico a usar ao solucionar problemas do Gerenciador de Rede.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Solução de problemas de Gerenciador de Rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a7c8e270fa3f1e07ce9b44fb9ce619d9fe5225e2c4d3ae87896d5e7cf20a2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120576"
---
# <a name="troubleshooting-the-network-explorer"></a>Solução de problemas de Gerenciador de Rede

O Gerenciador de Rede:

-   Sempre usa udp WS-Discovery para descoberta de dispositivo
-   Sempre inicia uma conexão HTTP ou HTTPS para troca de metadados
-   Às vezes, usa um https (canal seguro) para troca de metadados

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o Gerenciador de Rede.

**Para solucionar problemas de Gerenciador de Rede**

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para ODP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
3.  [Use o Cliente de Depuração do WSD para verificar o tráfego multicast.](using-wsddebug-client-to-verify-multicast-traffic.md)
4.  [Inspecione rastreamentos de rede para WS-Discovery UDP.](inspecting-network-traces-for-udp-ws-discovery.md)
5.  [Use um host genérico e um cliente para troca de metadados HTTP.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
6.  [Use o registro em log do WinHTTP para verificar Obter tráfego](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspecione os rastreamentos de rede para troca de metadados HTTP.](inspecting-network-traces-for-http-metadata-exchange.md)

O Gerenciador de Rede usa a [Descoberta de Funções](/previous-versions/windows/desktop/fundisc/fd-portal) para enumerar dispositivos de rede. Para obter mais informações de solução de problemas, consulte [Solução de problemas de clientes de descoberta de funções](troubleshooting-function-discovery-clients.md).

Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em Habilitando o rastreamento [WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida solução de problemas do WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solucionando problemas de clientes de descoberta de funções](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
