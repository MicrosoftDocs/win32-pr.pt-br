---
title: Serviços de Área de Trabalho Remota administração
description: A API Serviços de Área de Trabalho Remota permite enumerar e gerenciar servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), sessões de cliente e processos.
ms.assetid: 85a9ed9d-79d6-4011-93a4-00847c689747
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46df6277b924d25608b3c4def5074c1f156738e23d114de075af01521953e7d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000276"
---
# <a name="remote-desktop-services-administration"></a>Serviços de Área de Trabalho Remota administração

A API Serviços de Área de Trabalho Remota permite enumerar e gerenciar servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD), sessões de cliente e processos.

Para recuperar os nomes de todos os Host da Sessão RD em um domínio, chame a função [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) para enumerar servidores do tipo SV \_ TYPE \_ TERMINALSERVER. Para abrir um handle para um servidor Host da Sessão RD específico, passe o nome do servidor em uma chamada para a [**função WTSOpenServer.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera) Quando terminar de usar o handle, libere-o chamando a [**função WTSCloseServer.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)

Você pode usar o handle retornado **por WTSOpenServer** para executar as seguintes operações no servidor.



| Função                                                         | Operação                                                                                                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)             | Desconecta o cliente de uma sessão especificada. A sessão permanece ativa e o usuário pode fazer logon novamente para se conectar à mesma sessão.                                                                         |
| [**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)             | Retorna uma lista de sessões no servidor Host da Sessão RD especificado.                                                                                                                                               |
| [**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)           | Retorna uma lista de processos no servidor Host da Sessão RD especificado.                                                                                                                                              |
| [**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)                     | Faz o logs da sessão especificada.                                                                                                                                                                                   |
| [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) | Retorna informações sobre a sessão especificada no servidor Host da Sessão RD especificado.                                                                                                                          |
| [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)                         | Mostra uma caixa de mensagem na exibição do cliente de uma sessão especificada.                                                                                                                                                 |
| [**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)                   | Desliga e, opcionalmente, reinicia um servidor Host da Sessão RD especificado.                                                                                                                                            |
| [**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)               | Encerra um processo especificado em um servidor Host da Sessão RD especificado.                                                                                                                                             |
| [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)           | Abre um alça para a extremidade do servidor de um canal virtual especificado. Para obter mais informações sobre canais virtuais, consulte [Using Serviços de Área de Trabalho Remota Virtual Channels](using-terminal-services-virtual-channels.md). |
| [**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)                 | Aguarda um evento, como a criação de uma sessão de cliente ou de um usuário fazendo logon no servidor Host da Sessão RD servidor.                                                                                                  |



 

Várias dessas funções alocam buffers para retornar informações ao chamador. Quando terminar de usar o buffer, livre-o chamando a [**função WTSFreeMemory.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)

 

 