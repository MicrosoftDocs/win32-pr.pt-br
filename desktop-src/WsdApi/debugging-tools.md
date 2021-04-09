---
description: Um conjunto de ferramentas de depuração criado em serviços da Web na API de dispositivos (WSDAPI) está disponível no SDK do Windows e no WDK (Kit de driver do Windows).
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Ferramentas de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091708"
---
# <a name="debugging-tools"></a>Ferramentas de depuração

Um conjunto de ferramentas de depuração criado em serviços da Web na API de dispositivos (WSDAPI) está disponível no SDK do Windows e no WDK (Kit de driver do Windows). Essas ferramentas podem ser usadas para testar a funcionalidade de aplicativos personalizados escritos em WSDAPI, ou dispositivos e clientes gravados usando outro perfil de dispositivo para as pilhas de serviços Web (DPWS).

As ferramentas de host de depuração WSD (wsddebug \_host.exe) e de cliente de depuração WSD (wsddebug \_client.exe) podem ser usadas para inspecionar as características de clientes DPWS ou hosts. Eles também podem ser usados para solucionar problemas de conectividade ou configuração. Para obter mais informações, consulte [Guia de solução de problemas de WSDAPI](wsdapi-troubleshooting-guide.md). Essas ferramentas estão disponíveis apenas no SDK. As ferramentas do SDK estão localizadas no seguinte diretório: <Windows SDK Install Folder> \\ bin.

A [ferramenta de interoperabilidade básica do WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) pode ser usada para testar a interoperabilidade no nível do protocolo SOAP ou no nível de transporte (ou seja, garantir que as mensagens estejam bem formadas). Essa ferramenta só está disponível no WDK.

## <a name="the-wsd-debug-client"></a>O cliente de depuração WSD

O cliente de depuração WSD (wsddebug \_client.exe) fornece um console interativo que pode ser usado para enviar e receber mensagens de WS-Discovery e para obter metadados. Ele também pode ser usado para gerar e consumir mensagens brutas de multicast.

O cliente de depuração WSD opera em um dos três modos: multicast, descoberta e metadados.



| Mode      | Descrição                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multicast | No modo multicast, o cliente de depuração WSD envia e recebe mensagens multicast não formatadas na porta UDP 3702, conforme definido em WS-Discovery. O usuário pode salvar essas mensagens SOAP em um arquivo de texto e pode modificar e retransmitir as mensagens com o cliente de depuração WSD.                                                                                                                                 |
| Descoberta | No modo de descoberta, o cliente de depuração WSD envia e recebe mensagens de WS-Discovery formatadas. Ele pode exibir [mensagens de](bye-message.md) [saudação](hello-message.md), [ProbeMatches](probematches-message.md)e [ResolveMatches](resolvematches-message.md) recebidas. Ele pode enviar mensagens de [investigação](probe-message.md) por UDP ou http e [resolver](resolve-message.md) mensagens por UDP. |
| Metadados  | Além de implementar todos os recursos do modo de descoberta, o modo de metadados também tenta recuperar metadados de dispositivos.                                                                                                                                                                                                                                                                    |



 

Para obter mais informações, consulte [usando um host genérico e um cliente para troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md), [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md)e [usando o cliente de depuração WSD para verificar o tráfego multicast](using-wsddebug-client-to-verify-multicast-traffic.md).

## <a name="the-wsd-debug-host"></a>O host de depuração WSD

O host de depuração WSD (wsddebug \_host.exe) fornece um console interativo usado para anunciar o host, responder a solicitações de cliente e imprimir informações de diagnóstico.

O host de depuração WSD opera em um dos dois modos: descoberta e metadados.



| Mode      | Descrição                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descoberta | No modo de descoberta, o host de depuração WSD imprime as mensagens WS-Discovery formatadas. Ele também envia mensagens de [saudação](hello-message.md) e de [adeus](bye-message.md) e responde automaticamente a [investigações](probe-message.md) e a [resolver](resolve-message.md) mensagens. |
| Metadados  | Além de implementar todos os recursos do modo de descoberta, o modo de metadados anuncia um serviço de metadados e permite que os clientes se conectem e executem a troca de metadados.                                                                                       |



 

Para obter mais informações, consulte [usando um host genérico e um cliente para troca de metadados http](using-a-generic-host-and-client-for-http-metadata-exchange.md) e [usando um host genérico e um cliente para WS-Discovery de UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvimento de aplicativos WSD no Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[Ferramentas de desenvolvimento do WSDAPI](wsdapi-development-tools.md)
</dt> <dt>

[Guia de solução de problemas de WSDAPI](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



