---
description: O perfil de dispositivo para hosts de serviços Web (DPWS) e clientes se comunicam pela rede usando uma série de mensagens SOAP por UDP e HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Padrões de mensagem de troca de metadados e descoberta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104172440"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a>Padrões de mensagem de troca de metadados e descoberta

O perfil de dispositivo para hosts de serviços Web (DPWS) e clientes se comunicam pela rede usando uma série de mensagens SOAP por UDP e HTTP.

O diagrama a seguir mostra uma visão geral do tráfego esperado de UDP e HTTP entre um host DPWS e um cliente.

![Diagrama mostrando o tráfego UDP e HTTP entre um host DPWS e um cliente.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

As mensagens [Hello](hello-message.md), [adeus](bye-message.md), [Probe](probe-message.md), [resolve](resolve-message.md)e [Get](get--metadata-exchange--http-request-and-message.md) são todas geradas sem solicitação de rede; essas mensagens são usadas para anunciar o estado do dispositivo ou para emitir uma solicitação de pesquisa. As mensagens [ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)e [GetResponse](getresponse--metadata-exchange--message.md) são geradas em resposta à investigação, resolução e obtenção de mensagens.

As mensagens [Hello](hello-message.md), [adeus](bye-message.md), [resolve](resolve-message.md)e [ResolveMatches](resolvematches-message.md) sempre ocorrerão sobre o UDP. Da mesma forma, as mensagens de metadados [Get](get--metadata-exchange--http-request-and-message.md) e [GetResponse](getresponse--metadata-exchange--message.md) sempre ocorrerão via http ou HTTPS. As mensagens de [investigação](probe-message.md) e de [ProbeMatches](probematches-message.md) são normalmente transmitidas por UDP, mas ocorrem em uma conexão http ou HTTPS em um cenário de descoberta direcionada. Para obter mais informações sobre padrões de mensagem de descoberta direcionada, consulte [Solucionando problemas de aplicativos usando a descoberta direcionada](troubleshooting-applications-using-directed-discovery.md).

A lista a seguir mostra a sequência típica de mensagens na conexão. Nem todas as mensagens são obrigatórias.

1.  [Olá](hello-message.md)
2.  [Investigação](probe-message.md)
3.  [ProbeMatches](probematches-message.md)
4.  [Resolver](resolve-message.md)
5.  [ResolveMatches](resolvematches-message.md)
6.  [Get](get--metadata-exchange--http-request-and-message.md) (solicitação de troca de metadados)
7.  [GetResponse](getresponse--metadata-exchange--message.md)
8.  [Logo](bye-message.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os serviços Web em dispositivos](about-web-services-for-devices.md)
</dt> </dl>

 

 



