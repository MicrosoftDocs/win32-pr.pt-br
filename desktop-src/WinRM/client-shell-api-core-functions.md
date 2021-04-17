---
title: Funções principais da API do shell do cliente
description: A tabela a seguir fornece uma visão geral das funções básicas para a API do shell do cliente Gerenciamento Remoto do Windows (WinRM).
ms.assetid: cd0e6b55-03e8-4ebe-aea8-35d268cdb18c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebfe3390b3808cd0abbe9d6bf4ea83ccb0a92338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364063"
---
# <a name="client-shell-api-core-functions"></a>Funções principais da API do shell do cliente

A tabela a seguir fornece uma visão geral das funções básicas para a API do shell do cliente Gerenciamento Remoto do Windows (WinRM).



| Funções de núcleo                                                   | Descrição                                                                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManCloseCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosecommand)                   | Fecha um comando.                                                                                                                                                               |
| [**WSManCloseOperation**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseoperation)               | Fecha uma operação.                                                                                                                                                            |
| [**WSManCloseSession**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosesession)                   | Fecha uma sessão do WinRM.                                                                                                                                                         |
| [**WSManCloseShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseshell)                       | Fecha um objeto Shell.                                                                                                                                                          |
| [**WSManConnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshell)                   | Conecta-se a uma sessão de servidor existente.                                                                                                                                         |
| [**WSManConnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshellcommand)     | Conecta-se a um comando existente em execução em um shell.                                                                                                                             |
| [**WSManCreateSession**](/windows/desktop/api/Wsman/nf-wsman-wsmancreatesession)                 | Cria uma sessão do WinRM.                                                                                                                                                        |
| [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell)                     | Cria um objeto Shell.                                                                                                                                                         |
| [**WSManCreateShellEx**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshellex)                 | Cria um objeto shell usando a mesma funcionalidade que a função [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) , com a adição de uma ID de shell especificada pelo cliente.          |
| [**WSManDeinitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmandeinitialize)                   | Desinicializa a pilha de cliente do WinRM.                                                                                                                                           |
| [**WSManDisconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmandisconnectshell)             | Desconecta a conexão de rede de um shell ativo e seus comandos associados.                                                                                              |
| [**WSManInitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmaninitialize)                       | Inicializa o WinRM.                                                                                                                                                              |
| [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)       | Recebe a saída do Shell.                                                                                                                                                          |
| [**WSManReconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshell)               | Reconecta uma sessão de shell desconectada anteriormente. Para reconectar os comandos associados da sessão do Shell, use [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand). |
| [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand) | Reconecta um comando anteriormente desconectado.                                                                                                                                   |
| [**WSManRunShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand)             | Executa um comando do Shell.                                                                                                                                                           |
| [**WSManRunShellCommandEx**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommandex)         | Fornece a mesma funcionalidade que a função [**WSManRunShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand) , com a adição de uma opção de ID de comando.                                 |
| [**WSManSendShellInput**](/windows/desktop/api/Wsman/nf-wsman-wsmansendshellinput)               | Envia a entrada para um shell.                                                                                                                                                         |
| [**WSManSignalShell**](/windows/desktop/api/Wsman/nf-wsman-wsmansignalshell)                     | Sinaliza um shell.                                                                                                                                                                |



 

 

 




