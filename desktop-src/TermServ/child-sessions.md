---
title: Sessões filho
description: A partir do Windows Server 2012 e do Windows 8, o Área de Trabalho Remota dá suporte ao conceito de uma sessão filho, que é uma sessão de Área de Trabalho Remota de loopback especial que está vinculada à sessão existente de um usuário.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159349"
---
# <a name="child-sessions"></a>Sessões filho

A partir do Windows Server 2012 e do Windows 8, o Área de Trabalho Remota dá suporte ao conceito de uma *sessão filho*, que é uma sessão de área de trabalho remota de loopback especial que está vinculada à sessão existente de um usuário.

Não há suporte para sessões filhas nos seguintes sistemas operacionais:

<dl> Windows RT  
Opção de instalação do Windows Server 2012 Server Core  
Microsoft Hyper-V Server 2012  
</dl>

Um sistema pode ter apenas uma sessão filho ativa e conectada em um determinado momento.

A sessão filho pode ser finalizada fazendo logoff diretamente ou será encerrada quando a sessão pai for encerrada.

Antes que as sessões filho possam ser usadas em um sistema, você deve habilitar a funcionalidade de sessão filho chamando a função [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) . Você também pode determinar se as sessões filhas foram habilitadas usando a função [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .

Uma sessão filho só pode ser criada de dentro de uma sessão de usuário existente usando o [controle ActiveX área de trabalho remota](remote-desktop-activex-control.md) e definindo a propriedade "ConnectToChildSession" com [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) antes da conexão. Quando o método [**IMsTscAx. Connect**](imstscax-connect.md) for chamado, o controle ActiveX de área de trabalho remota fará logon automaticamente na sessão filho sem solicitar credenciais, exceto quando o usuário estiver conectado à sessão pai usando um cartão inteligente. Ao contrário de uma sessão de Área de Trabalho Remota regular, um usuário não precisa do direito interativo remoto de fazer logon na sessão filho porque esta é uma sessão de loopback.

Uma sessão filho não pode ser bloqueada. Ele não terá proteção de tela nem nenhuma tela de logon. Além disso, ao contrário de uma sessão regular, se a política de texto de logon do WinLogon for definida, o texto de logon não será exibido nessa sessão filho. Além disso, não haverá nenhum efeito de Conexão de Área de Trabalho Remota políticas de grupo de tempo limite na sessão filho se essas políticas estiverem definidas.

As seguintes APIs são usadas em conjunto com sessões filho:

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Propriedade "ConnectToChildSession" em [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)

 

 




