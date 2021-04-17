---
title: Administração de Serviços de Área de Trabalho Remota
description: A API Serviços de Área de Trabalho Remota permite enumerar e gerenciar servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), sessões de cliente e processos.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e763a652335c85931225746334bc21db0e6e086d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105757186"
---
# <a name="remote-desktop-services-administration"></a>Administração de Serviços de Área de Trabalho Remota

A API Serviços de Área de Trabalho Remota permite enumerar e gerenciar servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), sessões de cliente e processos.

Para recuperar os nomes de todos os servidores de Host da Sessão RD em um domínio, chame a função [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) para enumerar servidores do tipo TERMINALSERVER de VA do tipo \_ \_ . Para abrir um identificador para um servidor de Host da Sessão RD específico, passe o nome do servidor em uma chamada para a função [**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) . Quando você terminar de usar o identificador, libere-o chamando a função [**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver) .

Você pode usar o identificador retornado pelo **WTSOpenServer** para executar as seguintes operações no servidor.



| Função                                                         | Operação                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Desconecta o cliente de uma sessão especificada. A sessão permanece ativa e o usuário pode fazer logon novamente para se conectar à mesma sessão.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Retorna uma lista de sessões no servidor de Host da Sessão RD especificado.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Retorna uma lista de processos no servidor de Host da Sessão RD especificado.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Faz logoff da sessão especificada.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Retorna informações sobre a sessão especificada no servidor de Host da Sessão RD especificado.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Mostra uma caixa de mensagem na exibição do cliente de uma sessão especificada.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Desliga e, opcionalmente, reinicia um servidor de Host da Sessão RD especificado.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Finaliza um processo especificado em um servidor de Host da Sessão RD especificado.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Abre um identificador para a extremidade do servidor de um canal virtual especificado. Para obter mais informações sobre canais virtuais, consulte [usando serviços de área de trabalho remota canais virtuais](using-terminal-services-virtual-channels.md). |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Aguarda um evento, como a criação de uma sessão de cliente ou um usuário que faz logon no servidor de Host da Sessão RD.                                                                                                  |



 

Várias dessas funções alocam buffers para retornar informações ao chamador. Quando você terminar de usar o buffer, libere-o chamando a função [**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory) .

 

 