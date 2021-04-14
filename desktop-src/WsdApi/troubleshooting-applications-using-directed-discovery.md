---
description: Os aplicativos que usam a descoberta direcionada enviam mensagens de investigação por HTTP ou HTTPS para descobrir dispositivos.
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: Solução de problemas de aplicativos WSDAPI usando a descoberta direcionada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505701"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a>Solução de problemas de aplicativos WSDAPI usando a descoberta direcionada

Os aplicativos que usam a descoberta direcionada enviam mensagens de [investigação](probe-message.md) por http ou HTTPS para descobrir dispositivos. As mensagens [ProbeMatches](probematches-message.md) correspondentes enviadas em resposta também são enviadas por http ou HTTPS. A descoberta direcionada pode ser iniciada pelo Assistente para adicionar impressora, um cliente de descoberta de função ou um aplicativo WSDAPI. As mensagens de investigação e ProbeMatches são estruturalmente idênticas às enviadas por UDP. As mensagens são prefixadas com os cabeçalhos HTTP ou HTTPS apropriados.

Os procedimentos de diagnóstico a seguir devem ser usados (em ordem) para ajudar a identificar problemas com um aplicativo usando a descoberta direcionada.

**Para solucionar problemas de um aplicativo WSDAPI usando a descoberta direcionada**

1.  [Inspecione as configurações do adaptador e do firewall](inspecting-adapter-and-firewall-settings.md).
2.  [Use um host genérico e um cliente para a troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Use o log do WinHTTP para verificar o tráfego de obtenção](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspecione os rastreamentos de rede de um aplicativo usando a descoberta direcionada](inspecting-network-traces-for-applications-using-directed-discovery.md).

Se a origem do problema não puder ser identificada usando os procedimentos de diagnóstico acima, siga as instruções em [habilitando o rastreamento de WSDAPI](enabling-wsdapi-tracing.md) e entre em contato com o suporte da Microsoft.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com a solução de problemas de WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Solução de problemas do assistente para adicionar impressora](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[Solução de problemas de aplicativos WSDAPI](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



