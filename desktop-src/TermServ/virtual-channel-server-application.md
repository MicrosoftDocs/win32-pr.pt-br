---
title: Aplicativo de servidor do virtual Channel
description: O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Observe que você deve fornecer um método para iniciar o aplicativo de servidor.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636206"
---
# <a name="virtual-channel-server-application"></a>Aplicativo de servidor do virtual Channel

O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Observe que você deve fornecer um método para iniciar o aplicativo de servidor. Você pode fazer isso de várias maneiras; por exemplo, você pode usar um script de logon ou um programa ou script na pasta Startup. Os usuários também podem iniciar o aplicativo.

Você deve armazenar o nome do aplicativo de servidor do virtual Channel no registro adicionando uma subchave no seguinte local:

**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **Terminal Server** \\ **AddIns**

Para obter mais informações sobre a subchave, consulte [monitorando conexões de sessão e desconexões](monitoring-session-connections-and-disconnections.md).

O aplicativo de servidor pode chamar a função [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) para abrir um identificador para um canal virtual. O aplicativo pode usar o identificador em qualquer uma das funções a seguir.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Fecha um identificador de canal virtual aberto.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Exclui todos os dados de entrada na fila enviados do cliente para o servidor em um canal virtual específico.

> [!Note]  
> Essa função não é usada atualmente por Serviços de Área de Trabalho Remota.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Exclui todos os dados de saída na fila enviados do servidor para o cliente em um canal virtual específico.

> [!Note]  
> Essa função não é usada atualmente por Serviços de Área de Trabalho Remota.

 

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Retorna informações sobre um canal virtual especificado.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Lê dados da extremidade do servidor de um canal virtual.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Grava dados na extremidade do servidor de um canal virtual.

</dd> </dl>

 

 




