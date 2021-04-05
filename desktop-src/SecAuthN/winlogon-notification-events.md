---
description: Lista os eventos de notificação do Winlogon.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Eventos de notificação do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58827dc2699c92dfc3a814d2366608e1bd3fb662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827025"
---
# <a name="winlogon-notification-events"></a>Eventos de notificação do Winlogon

O [*Winlogon*](../secgloss/w-gly.md) pode informar seu pacote de notificação dos eventos a seguir.



| Evento                               | Descrição                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bloquear**<br/>                 | Esse evento ocorre quando o usuário bloqueia a estação de trabalho.<br/>                                                                                                                                                                                                                                                   |
| **Verbos**<br/>               | Esse evento ocorre quando um usuário faz logoff do sistema. O evento de **logoff** é executado de forma síncrona, mesmo que as configurações do registro do pacote de notificação indiquem que ele pode manipular eventos de maneira assíncrona.<br/>                                                                                         |
| **Logon**<br/>                | Esse evento ocorre quando um usuário faz logon no sistema.<br/> Observe que o evento de **logon** ocorre antes que as conexões de rede do usuário sejam restauradas. Se o manipulador de eventos exigir acesso às conexões de rede do usuário, ele deverá manipular o evento **StartShell** em vez do evento de **logon** .<br/> |
| **Desligamento**<br/>             | Esse evento ocorre pouco antes de o sistema ser desligado.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Esse evento ocorre quando um usuário faz logon no sistema com um cartão inteligente.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Esse evento ocorre quando a proteção de tela é iniciada. Normalmente, isso acontece depois que um usuário fica inativo por um determinado período de tempo.<br/> As funções que manipulam esse evento não devem exibir uma interface do usuário. A notificação de eventos **StartScreenSaver** destina-se apenas a fins informativos.<br/> |
| **StartShell**<br/>           | Esse evento ocorre depois que o usuário fez logon no sistema, as conexões de rede foram estabelecidas e o programa de shell especificado pelo usuário (normalmente o Windows Explorer) foi iniciado.<br/>                                                                                                                |
| **Inicialização**<br/>              | Esse evento ocorre quando o sistema é iniciado ou reiniciado.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Esse evento ocorre quando a proteção de tela é interrompida. Normalmente, isso acontece quando há atividade de teclado ou de mouse.<br/> As funções que manipulam esse evento não devem exibir uma interface do usuário. A notificação de eventos **StopScreenSaver** destina-se apenas a fins informativos.<br/>                  |
| **Unlock**<br/>               | Esse evento ocorre quando o usuário desbloqueia a estação de trabalho ou quando um administrador do sistema substitui o bloqueio e faz o logoff do usuário.<br/>                                                                                                                                                                         |



 

 

 
