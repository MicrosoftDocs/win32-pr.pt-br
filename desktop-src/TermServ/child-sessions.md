---
title: Sessões filho
description: Começando com Windows Server 2012 e Windows 8, o Área de Trabalho Remota dá suporte ao conceito de uma sessão filho, que é uma sessão de loopback especial Área de Trabalho Remota que está vinculada à sessão existente de um usuário.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d79fa6e18cece69c672b60a65e679441ce986a6cd8a0ad46524440738c3844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010416"
---
# <a name="child-sessions"></a>Sessões filho

Começando com Windows Server 2012 e Windows 8, o Área de Trabalho Remota dá suporte ao conceito de uma sessão filho *,* que é uma sessão de loopback especial Área de Trabalho Remota que está vinculada à sessão existente de um usuário.

Não há suporte para sessões filho nos seguintes sistemas operacionais:

<dl> Windows RT  
Windows Server 2012 Opção de instalação Server Core  
Microsoft Hyper-V Server 2012  
</dl>

Um sistema só pode ter uma sessão filho ativa e conectada em um determinado momento.

A sessão filho pode ser encerrada fazendo logon diretamente dela ou será encerrada quando sua sessão pai for encerrada.

Antes que as sessões filho possam ser usadas em um sistema, você deve habilitar a funcionalidade de sessão filho chamando a [**função WTSEnableChildSessions.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) Você também pode determinar se as sessões filho foram habilitadas usando a [**função WTSIsChildSessionsEnabled.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)

Uma sessão filho só pode ser criada de dentro da sessão de um usuário existente usando o controle Área de Trabalho Remota ActiveX e definindo [a](remote-desktop-activex-control.md) propriedade "ConnectToChildSession" com [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) antes de se conectar. Quando o método [**IMsTscAx.Conexão**](imstscax-connect.md) for chamado, o controle Área de Trabalho Remota ActiveX fará logon automaticamente na sessão filho sem solicitar credenciais, exceto quando o usuário estiver conectado à sessão pai usando um cartão inteligente. Ao contrário de uma sessão Área de Trabalho Remota regular, um usuário não precisa do direito interativo remoto para fazer logon na sessão filho porque essa é uma sessão de loopback.

Uma sessão filho não pode ser bloqueada. Ele não terá nenhuma economia de tela e nenhuma tela de logon. Além disso, ao contrário de uma sessão regular, se a política de texto de logon do WinLogon estiver definida, o texto de logon não será exibido nesta sessão filho. Além disso, não haverá nenhum efeito de Conexão de Área de Trabalho Remota de Grupo de Tempo Conexão de Área de Trabalho Remota na sessão filho se essas políticas estão definidas.

As seguintes APIs são usadas em conjunto com sessões filho:

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Propriedade "ConnectToChildSession" [ **em IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)

 

 




