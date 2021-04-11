---
title: APIs de cliente do DVC
description: As APIs de cliente de canal virtual dinâmico (DVC) são implementadas especificamente para o cliente de Conexão de Área de Trabalho Remota (RDC) da conexão.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c29d360fb0ad4d6e31e828f9c62f42f64fb311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292060"
---
# <a name="dvc-client-apis"></a>APIs de cliente do DVC

As APIs de cliente de canal virtual dinâmico (DVC) são implementadas especificamente para o cliente de Conexão de Área de Trabalho Remota (RDC) da conexão. Algumas das APIs são implementadas pela estrutura DVC e algumas são implementadas pelo desenvolvedor de plug-ins. Algumas das APIs são usadas para dar suporte ao plug-in de cliente Conexão de Área de Trabalho Remota (RDC) e não estão diretamente relacionadas ao transporte de dados.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Permite que o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) seja carregado pelo cliente Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Gerencia definições de configuração para cada ouvinte para a conexão de canal virtual dinâmico (DVC).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Usado para notificar o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) sobre solicitações de entrada em um ouvinte específico.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Gerencia todos os plug-ins de cliente Conexão de Área de Trabalho Remota (RDC) e ouvintes de canal virtual dinâmico (DVC).

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Usado para controlar o estado do canal e grava no canal.

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Recebe notificações sobre alterações de estado de canal ou dados recebidos.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Não há suporte para essa interface.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Chamado para que o plug-in crie uma instância da interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos os plug-ins implementados pela dll.

</dd> </dl>

 

 




