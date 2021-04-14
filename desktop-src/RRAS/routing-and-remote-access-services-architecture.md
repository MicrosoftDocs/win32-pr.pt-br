---
title: Arquitetura de serviços de roteamento e acesso remoto
description: A ilustração a seguir apresenta uma visão geral da arquitetura do roteador do Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- Serviço de roteamento e acesso remoto serviços RRAS, roteamento e acesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453664"
---
# <a name="routing-and-remote-access-services-architecture"></a>Arquitetura de serviços de roteamento e acesso remoto

A ilustração a seguir apresenta uma visão geral da arquitetura do roteador do Windows 2000.

Os componentes específicos à família do protocolo IP são mostrados em cinza claro. Os componentes específicos para a família de protocolo IPX são mostrados em cinza escuro. Os componentes que são gerais para todas as famílias de protocolos não são sombreados.

O serviço de roteamento e acesso remoto fornece APIs para administrar e configurar o serviço. Essas APIs incluem agentes SNMP para IP e IPX.

O RRAS inclui protocolos de roteamento para IP e IPX. Para IP, o RRAS fornece o RIP (Routing Information Protocol) e protocolos de roteamento OSPF (Open Shortest Path First). Para o IPX, o RRAS fornece IPX RIP e protocolo de anúncio de serviço (SAP).

O RRAS usa um Gerenciador de tabela de roteamento (RTM) para IP e IPX. No entanto, cada família de protocolos tem seu próprio Gerenciador de roteador. O RRAS também tem um componente separado para gerenciar grupos de multicast.

As interfaces do Gerenciador de interface dinâmica (DIM) com serviços PPP e TAPI para gerenciar interfaces PPP usadas por algumas rotas.

![Visão geral da arquitetura do roteador do Windows 2000](images/rtarch.png)

 

 




