---
description: Os hosts e os clientes do DPWS (Perfil de Dispositivo para Serviços Web) se comunicam pela rede usando uma série de mensagens SOAP por UDP e HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Padrões de mensagem de descoberta e Exchange metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b41267e86358a9d6e263f4bc8971632f1061eb1c94d1e64cc76d65020ce255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856786"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Padrões de mensagem de descoberta e Exchange metadados

Os hosts e os clientes do DPWS (Perfil de Dispositivo para Serviços Web) se comunicam pela rede usando uma série de mensagens SOAP por UDP e HTTP.

O diagrama a seguir mostra uma visão geral do tráfego UDP e HTTP esperado entre um host e um cliente DPWS.

![Diagrama mostrando o tráfego UDP e HTTP entre um host e um cliente DPWS.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

[As](hello-message.md)mensagens Hello , [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md)e [Get](get--metadata-exchange--http-request-and-message.md) são geradas sem solicitação de rede; essas mensagens são usadas para anunciar o estado do dispositivo ou para emitir uma solicitação de pesquisa. [As mensagens ProbeMatches,](probematches-message.md) [ResolveMatches](resolvematches-message.md)e [GetResponse](getresponse--metadata-exchange--message.md) são geradas em resposta às mensagens Probe, Resolve and Get.

[As](hello-message.md)mensagens Hello , [Bye](bye-message.md), [Resolve](resolve-message.md)e [ResolveMatches](resolvematches-message.md) sempre ocorrerão por UDP. Da mesma forma, [as mensagens](get--metadata-exchange--http-request-and-message.md) de metadados Get [e GetResponse](getresponse--metadata-exchange--message.md) sempre ocorrerão por HTTP ou HTTPS. [As](probe-message.md) mensagens [Probe e ProbeMatches](probematches-message.md) normalmente são transmitidas por UDP, mas ocorrem em uma conexão HTTP ou HTTPS em um cenário de descoberta direcionada. Para obter mais informações sobre padrões de mensagens de descoberta direcionadas, consulte [Solução de problemas de aplicativos usando a descoberta direcionada.](troubleshooting-applications-using-directed-discovery.md)

A lista a seguir mostra a sequência típica de mensagens na transmissão. Nem todas as mensagens são obrigatórias.

1.  [Olá](hello-message.md)
2.  [Investigação](probe-message.md)
3.  [Probematches](probematches-message.md)
4.  [Resolver](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (solicitação de troca de metadados)
7.  [Getresponse](getresponse--metadata-exchange--message.md)
8.  [Tchau](bye-message.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre serviços Web em dispositivos](about-web-services-for-devices.md)
</dt> </dl>

 

 



