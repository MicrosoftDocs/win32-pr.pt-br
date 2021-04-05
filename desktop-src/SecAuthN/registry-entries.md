---
description: Explica as entradas de registro para eventos do Winlogon.
ms.assetid: dbebe23f-84ff-4a3e-8b8c-fa3bda10fa57
title: Entradas do registro (autenticação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d50b413d99d2bc31a7af4e8e101ab27e51a8892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828224"
---
# <a name="registry-entries-authentication"></a>Entradas do registro (autenticação)

Para que o pacote receba notificações de eventos do [*Winlogon*](../secgloss/w-gly.md), você deve fornecer o nome do pacote, os nomes das funções do manipulador de eventos no pacote, a dll responsável pela implementação do pacote e as informações sobre se a dll dá suporte a eventos assíncronos e à representação.

Você deve criar a chave do registro do pacote de notificação como uma subchave de

**HKEY \_ \_** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Notify** do software da máquina local

O nome da chave é geralmente o mesmo que o nome da DLL; no entanto, isso não é obrigatório. O nome escolhido para o seu pacote não deve entrar em conflito com os nomes de outros pacotes de notificação instalados.

Na chave **notificar** registro, crie os valores de registro a seguir se houver uma função de manipulador de eventos relevante em seu pacote.



| Tipo de dados nome do valor \[\]                         | Description                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Assíncrono** \[ **Reg \_ VALOR DWORD**\]<br/>    | Indica se o pacote pode manipular eventos de forma assíncrona. Se esse valor for definido como 1, o Winlogon chamará as funções de pacote em um thread separado. Caso contrário, isso não acontece.<br/>                                                                                                                                                                                                                                 |
| **DllName** \[ **Reg \_ EXPANDa \_ sz**\]<br/>    | Nome da DLL que implementa o pacote de notificação, por exemplo: "Notify.dll".<br/>                                                                                                                                                                                                                                                                                                                          |
| **Representar** \[ **Reg \_ VALOR DWORD**\]<br/>     | Indica se o Winlogon deve representar o [*contexto*](../secgloss/c-gly.md) de segurança do usuário conectado ao chamar as funções do pacote de notificação. Se esse valor for definido como 1, o Winlogon usará a representação. Caso contrário, isso não acontece.<br/>                                                                                                                    |
| **Bloquear** \[ **Reg \_ SZ**\]<br/>               | Nome da função que manipula eventos de bloqueio da área de trabalho, por exemplo: "WLEventLock".<br/>                                                                                                                                                                                                                                                                                                                           |
| Fazer **logoff** \[ **Reg \_ SZ**\]<br/>             | Nome da função que manipula eventos de logoff, por exemplo: "WLEventLogoff".<br/>                                                                                                                                                                                                                                                                                                                               |
| **Logon** \[ do **Reg \_ SZ**\]<br/>              | Nome da função que manipula eventos de logon, por exemplo: "WLEventLogon".<br/>                                                                                                                                                                                                                                                                                                                                 |
| **Desligar** \[ **Reg \_ SZ**\]<br/>           | Nome da função que lida com eventos de desligamento, por exemplo: "WLEventShutdown".<br/>                                                                                                                                                                                                                                                                                                                           |
| **SmartCardLogonNotify** \[ **Valor DWORD**\]<br/> | Indica se o Winlogon deve gerar uma notificação para eventos de logon de cartões inteligentes. Se esse valor for definido como 1, o Winlogon permitirá notificações de cartão inteligente. Caso contrário, isso não acontece.<br/>                                                                                                                                                                                                                     |
| **StartScreenSaver** \[ **Reg \_ SZ**\]<br/>   | Nome da função que lida com os eventos de início da proteção de tela, por exemplo: "WLEventStartScreenSaver".<br/>                                                                                                                                                                                                                                                                                                          |
| **StartShell** \[ **Reg \_ SZ**\]<br/>         | Nome da função que manipula eventos de inicialização do Shell, por exemplo: "WLEventStartShell".<br/> Um evento de inicialização do Shell ocorre depois que o usuário faz logon, mas antes que a área de trabalho seja exibida. Ele é diferente do evento de logon no qual o [*contexto*](../secgloss/c-gly.md) de segurança do usuário foi estabelecido e recursos como conexões de rede estão disponíveis.<br/> |
| **Inicialização** \[ do **Reg \_ SZ**\]<br/>            | Nome da função que manipula eventos de inicialização do sistema, por exemplo: "WLEventStartup".<br/>                                                                                                                                                                                                                                                                                                                       |
| **StopScreenSaver** \[ **Reg \_ SZ**\]<br/>    | Nome da função que lida com eventos de parada da proteção de tela, por exemplo: "WLEventStopScreenSaver".<br/>                                                                                                                                                                                                                                                                                                            |
| **Desbloquear** \[ **Reg \_ SZ**\]<br/>             | Nome da função que manipula eventos de desbloqueio da área de trabalho, por exemplo: "WLEventUnlock".<br/>                                                                                                                                                                                                                                                                                                                        |



 

 

 
