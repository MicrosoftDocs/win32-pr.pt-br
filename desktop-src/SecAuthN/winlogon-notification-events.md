---
description: Lista eventos de notificação do Winlogon.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Eventos de notificação do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7359ef4d1d053e438d30564fcededbf3a0ccb10275cd6e4f669c2a20c54b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785707"
---
# <a name="winlogon-notification-events"></a>Eventos de notificação do Winlogon

[*O Winlogon*](../secgloss/w-gly.md) pode informar seu pacote de notificação dos eventos a seguir.



| Evento                               | Descrição                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bloquear**<br/>                 | Esse evento ocorre quando o usuário bloqueia a estação de trabalho.<br/>                                                                                                                                                                                                                                                   |
| **Logoff**<br/>               | Esse evento ocorre quando um usuário faz o login do sistema. O **evento Logoff** é executado de forma síncrona, mesmo que as configurações do registro do pacote de notificação indiquem que ele pode manipular eventos de forma assíncrona.<br/>                                                                                         |
| **Logon**<br/>                | Esse evento ocorre quando um usuário faz logs no sistema.<br/> Observe que o **evento Logon** ocorre antes que as conexões de rede do usuário sejam restauradas. Se o manipulador de eventos exigir acesso às conexões de rede do usuário, ele deverá manipular o evento **StartShell** em vez do **evento Logon.**<br/> |
| **Desligamento**<br/>             | Esse evento ocorre logo antes do sistema ser desligado.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Esse evento ocorre quando um usuário faz login no sistema com um cartão inteligente.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Esse evento ocorre quando a economia de tela é iniciada. Normalmente, isso acontece depois que um usuário está inativo por um período de tempo definido.<br/> As funções que manipulam esse evento não devem exibir uma interface do usuário. **A notificação de evento StartScreenSaver** destina-se apenas a fins informacionais.<br/> |
| **StartShell**<br/>           | Esse evento ocorre depois que o usuário faz logout no sistema, as conexões de rede foram estabelecidas e o programa de shell especificado pelo usuário (geralmente Windows Explorer) foi iniciado.<br/>                                                                                                                |
| **Inicialização**<br/>              | Esse evento ocorre quando o sistema é iniciado ou reiniciado.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Esse evento ocorre quando a economia de tela foi interrompida. Normalmente, isso acontece quando há atividade de teclado ou mouse.<br/> As funções que manipulam esse evento não devem exibir uma interface do usuário. **A notificação de evento StopScreenSaver** destina-se apenas a fins informacionais.<br/>                  |
| **Desbloquear**<br/>               | Esse evento ocorre quando o usuário desbloqueia a estação de trabalho ou quando um administrador do sistema substitui o bloqueio e faz o login do usuário.<br/>                                                                                                                                                                         |



 

 

 
