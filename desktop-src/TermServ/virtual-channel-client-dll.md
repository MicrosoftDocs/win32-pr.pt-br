---
title: DLL de cliente de canal virtual
description: O cliente de um aplicativo de canais virtuais é uma DLL que é carregada durante a inicialização do Serviços de Área de Trabalho Remota no computador cliente. A DLL deve ser registrada no computador cliente.
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd7ffccda8b1da7dfc3920b0a47a12e97840e0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005579"
---
# <a name="virtual-channel-client-dll"></a>DLL de cliente de canal virtual

O cliente de um aplicativo de canais virtuais é uma DLL que é carregada durante a inicialização do Serviços de Área de Trabalho Remota no computador cliente. A DLL deve ser registrada no computador cliente. Para obter mais informações, consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md).

A DLL do cliente deve exportar uma função [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) , que serviços de área de trabalho remota chamadas durante a inicialização. O ponto de entrada **VirtualChannelEntry** recebe um ponteiro para uma estrutura de [**pontos de \_ entrada \_ de canal**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points) . Essa estrutura contém ponteiros para as funções que a DLL do cliente chama para acessar canais virtuais.



| Função                                                      | Descrição                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | Registra os nomes dos canais virtuais a serem usados pelo cliente e fornece uma função de retorno de chamada [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) por meio da qual o serviços de área de trabalho remota notifica o cliente sobre eventos que afetam a conexão do cliente.<br/> |
| [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | Abre a extremidade do cliente de um canal virtual especificado e fornece uma função de retorno de chamada [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) por meio da qual o serviços de área de trabalho remota notifica o cliente sobre eventos que afetam o canal virtual.<br/>                    |
| [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | Grava dados em um canal virtual. Serviços de Área de Trabalho Remota envia esses dados para a extremidade do servidor do canal virtual. A extremidade do servidor chama a função [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) para ler os dados.<br/>                                             |
| [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | Fecha um canal virtual.<br/>                                                                                                                                                                                                                                                  |



 

A função [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) de sua DLL deve chamar a função [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) para inicializar o acesso aos canais virtuais. Ao chamar **VirtualChannelInit**, você deve passar um ponteiro para a função de retorno de chamada [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) . Serviços de Área de Trabalho Remota chama essa função de retorno de chamada quando a inicialização é concluída e novamente quando uma conexão é estabelecida com um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

Depois que a conexão é estabelecida, você pode chamar a função [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) para abrir os canais virtuais registrados pela chamada [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) . A chamada **VirtualChannelOpen** especifica um ponteiro para sua função de retorno de chamada [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) .

Depois que a chamada [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) retorna, você pode chamar a função [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) para gravar no canal virtual. A operação de gravação é assíncrona, portanto, você não deve liberar ou reutilizar o buffer passado para **VirtualChannelWrite** até que serviços de área de trabalho remota chame sua função [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) para indicar que a operação de gravação foi concluída. Ao chamar **VirtualChannelWrite**, você pode passar uma parte dos dados do usuário que identifica a operação de gravação. Serviços de Área de Trabalho Remota passa esses dados do usuário de volta quando chama **VirtualChannelOpenEvent** para notificá-lo de que a operação foi concluída. Na extremidade do servidor do canal virtual, o suplemento do servidor chama a função [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) para ler os dados.

Serviços de Área de Trabalho Remota também chama sua função [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) quando os dados são gravados no canal virtual pelo módulo do servidor. O módulo de servidor chama a função [**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) para gravar dados na extremidade do servidor do canal virtual.

Os módulos cliente e servidor podem gravar blocos de dados de qualquer tamanho para o canal virtual. No entanto, antes de enviar os dados, Serviços de Área de Trabalho Remota segmenta os dados em partes de bytes de comprimento da parte do canal \_ \_ . Serviços de Área de Trabalho Remota chama sua função [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) uma vez para cada parte dos dados, em vez de recriar os dados em um bloco do tamanho original. Cada chamada para **VirtualChannelOpenEvent** indica o tamanho da parte, o tamanho total gravado pelo servidor e se os dados constituem o início, o meio ou o fim de um bloco gravado pelo servidor.

Você pode chamar a função [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) para fechar um canal. No entanto, não é necessário chamá-lo porque Serviços de Área de Trabalho Remota fecha todos os canais automaticamente quando o cliente se desconecta do servidor.

 

 





