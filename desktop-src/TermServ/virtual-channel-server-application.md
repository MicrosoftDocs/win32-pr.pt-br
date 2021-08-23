---
title: Aplicativo de Servidor de Canal Virtual
description: O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Observe que você deve fornecer um método para iniciar o aplicativo de servidor.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63a758f4860a0ab606f18c4a5086d305b1f627475bf7bab588648cea8aabd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423556"
---
# <a name="virtual-channel-server-application"></a>Aplicativo de Servidor de Canal Virtual

O módulo de servidor de um aplicativo que usa canais virtuais deve ser um aplicativo de modo de usuário em execução em uma sessão de cliente no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Observe que você deve fornecer um método para iniciar o aplicativo de servidor. Você pode fazer isso de várias maneiras; por exemplo, você pode usar um script de logon ou um programa ou script na pasta Inicialização. Os usuários também podem iniciar o aplicativo.

Você deve armazenar o nome do aplicativo de servidor de canal virtual no Registro adicionando uma sub-chave no seguinte local:

**HKEY \_ Complementos \_ do** servidor do terminal \\  \\ **de controle CurrentControlSet** \\  \\  \\ **do sistema** LOCAL MACHINE

Para obter mais informações sobre a sub-chave, consulte [Monitoramento de conexões de sessão e desconexões](monitoring-session-connections-and-disconnections.md).

O aplicativo de servidor pode chamar a [**função WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) para abrir um handle para um canal virtual. Em seguida, o aplicativo pode usar o handle em qualquer uma das funções a seguir.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Fecha um alça de canal virtual aberto.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Exclui todos os dados de entrada na fila enviados do cliente para o servidor em um canal virtual específico.

> [!Note]  
> Atualmente, essa função não é usada por Serviços de Área de Trabalho Remota.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Exclui todos os dados de saída na fila enviados do servidor para o cliente em um canal virtual específico.

> [!Note]  
> Atualmente, essa função não é usada por Serviços de Área de Trabalho Remota.

 

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

Grava dados no final do servidor de um canal virtual.

</dd> </dl>

 

 




