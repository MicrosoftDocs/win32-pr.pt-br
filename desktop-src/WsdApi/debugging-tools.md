---
description: Um conjunto de ferramentas de depuração criado na API WSDAPI (Serviços Web em Dispositivos) está disponível no SDK do Windows e no WDK (Kit de Driver Windows).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Ferramentas de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e744b37a5376d228ac9023ed7556ce63e26a7a1c20b23fb98aff090e7ae9616f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856776"
---
# <a name="debugging-tools"></a>Ferramentas de depuração

Um conjunto de ferramentas de depuração criado na API WSDAPI (Serviços Web em Dispositivos) está disponível no SDK do Windows e no WDK (Kit de Driver Windows). Essas ferramentas podem ser usadas para testar a funcionalidade de aplicativos personalizados escritos em WSDAPI ou dispositivos e clientes escritos usando outras pilhas de DPWS (Perfil de Dispositivo para Serviços Web).

As ferramentas Host de Depuração do WSD (wsddebughost.exe) e Cliente de Depuração do \_ WSD (wsddebugclient.exe) podem ser usadas para inspecionar as características de clientes \_ ou hosts DPWS. Eles também podem ser usados para solucionar problemas de conectividade ou configuração. Para obter mais informações, consulte Guia de solução de problemas do [WSDAPI.](wsdapi-troubleshooting-guide.md) Essas ferramentas só estão disponíveis no SDK. As ferramentas do SDK estão localizadas no seguinte diretório: <Windows SDK Install Folder> \\ Bin.

A [WSDBIT (Ferramenta de Interoperabilidade Básica do WSDAPI)](https://msdn.microsoft.com/library/cc264250.aspx) pode ser usada para testar a interoperabilidade no nível soap ou no nível do transporte (ou seja, garantir que as mensagens sejam bem formadas). Essa ferramenta só está disponível no WDK.

## <a name="the-wsd-debug-client"></a>O cliente de depuração do WSD

O WSD Debug Client (wsddebugclient.exe) fornece um console interativo que pode ser usado para enviar e receber mensagens WS-Discovery e para obter \_ metadados. Ele também pode ser usado para gerar e consumir mensagens brutas de multicast.

O cliente de depuração do WSD opera em um dos três modos: multicast, descoberta e metadados.



| Mode      | Descrição                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multicast | No modo Multicast, o Cliente de Depuração do WSD envia e recebe mensagens multicast não formatada na porta UDP 3702, conforme definido em WS-Discovery. O usuário pode salvar essas mensagens SOAP em um arquivo de texto e pode modificar e readivar as mensagens com o Cliente de Depuração do WSD.                                                                                                                                 |
| Descoberta | No modo descoberta, o cliente de depuração do WSD envia e recebe mensagens WS-Discovery formatadas. Ele pode exibir mensagens [Hello](hello-message.md), [Bye,](bye-message.md) [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) recebidas. Ele pode enviar [mensagens de](probe-message.md) investigação por UDP ou HTTP e [Resolver](resolve-message.md) mensagens por UDP. |
| Metadados  | Além de implementar todos os recursos do modo de descoberta, o modo de metadados também tenta recuperar metadados de dispositivos.                                                                                                                                                                                                                                                                    |



 

Para obter mais informações, consulte Using a Generic Host and Client for [HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), Using a Generic Host and [Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md)e [Using WSD Debug Client](using-wsddebug-client-to-verify-multicast-traffic.md)to Verify Multicast Traffic .

## <a name="the-wsd-debug-host"></a>O host de depuração do WSD

O Host de Depuração do WSD (wsddebughost.exe) fornece um console interativo usado para anunciar o host, responder às solicitações do cliente e imprimir \_ informações de diagnóstico.

O Host de Depuração do WSD opera em um dos dois modos: descoberta e metadados.



| Mode      | Descrição                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descoberta | No modo descoberta, o Host de Depuração do WSD imprime WS-Discovery mensagens formatadas. Ele também envia [mensagens Hello](hello-message.md) e [Bye](bye-message.md) e responde automaticamente às [mensagens Probe](probe-message.md) e [Resolve.](resolve-message.md) |
| Metadados  | Além de implementar todos os recursos do modo de descoberta, o modo de metadados anuncia um serviço de metadados e permite que os clientes se conectem e executem a troca de metadados.                                                                                       |



 

Para obter mais informações, consulte Using a Generic Host and [Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) e Using a Generic Host and Client for [UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de aplicativos do WSD Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Ferramentas de desenvolvimento do WSDAPI](wsdapi-development-tools.md)
</dt> <dt>

[Guia de solução de problemas do WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



