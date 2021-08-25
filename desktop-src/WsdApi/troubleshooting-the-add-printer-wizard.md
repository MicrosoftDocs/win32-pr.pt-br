---
description: Lista os procedimentos de diagnóstico a usar ao solucionar problemas do Assistente para Adicionar Impressora.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Solução de problemas do Assistente para Adicionar Impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6c6971108b0f6fb46a373be47943a3ccbc7fcd97b830733c139653f991debd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860046"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Solução de problemas do Assistente para Adicionar Impressora

O Assistente para Adicionar Impressora:

-   Sempre usa udp WS-Discovery para descoberta de dispositivo
-   Sempre inicia uma conexão HTTP ou HTTPS para troca de metadados
-   Às vezes, usa a descoberta direcionada
-   Às vezes, usa um https (canal seguro) para troca de metadados

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com o Assistente para Adicionar Impressora.

**Para solucionar problemas do Assistente para Adicionar Impressora**

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
</dt> <dt>

[Solução de problemas de aplicativos usando a descoberta direcionada](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



