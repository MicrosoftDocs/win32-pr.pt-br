---
title: APIs de cliente DVC
description: As APIs de cliente DVC (canal virtual dinâmico) são implementadas especificamente para o cliente RDC (Conexão de Área de Trabalho Remota) da conexão.
ms.assetid: 976a6cc2-7bbe-4ecc-91b4-b7c659eca5ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557f51adbf10562465f93a101e502632a791d5c272b278c5a8b7ea6124637913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130812"
---
# <a name="dvc-client-apis"></a>APIs de cliente DVC

As APIs de cliente DVC (canal virtual dinâmico) são implementadas especificamente para o cliente RDC (Conexão de Área de Trabalho Remota) da conexão. Algumas das APIs são implementadas pela estrutura DVC e outras são implementadas pelo desenvolvedor de plug-in. Algumas das APIs são usadas para dar suporte ao plug-in de cliente RDC (Conexão de Área de Trabalho Remota) e não estão diretamente relacionadas ao transporte de dados.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)
</dt> <dd>

Permite que o plug-in Conexão de Área de Trabalho Remota (RDC) seja carregado pelo cliente RDC (Conexão de Área de Trabalho Remota).

</dd> <dt>

[**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)
</dt> <dd>

Gerencia as definições de configuração para cada ouvinte para a conexão DVC (canal virtual dinâmico).

</dd> <dt>

[**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)
</dt> <dd>

Usado para notificar o plug-in do cliente RDC (Conexão de Área de Trabalho Remota) sobre solicitações de entrada em um ouvinte específico.

</dd> <dt>

[**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)
</dt> <dd>

Gerencia todos os plug-ins de cliente RDC (Conexão de Área de Trabalho Remota) e ouvintes DVC (canal virtual dinâmico).

</dd> <dt>

[**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)
</dt> <dd>

Usado para controlar o estado do canal e gravações no canal.

</dd> <dt>

[**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback)
</dt> <dd>

Recebe notificações sobre alterações de estado do canal ou dados recebidos.

</dd> <dt>

[**IWTSVirtualChannelCallback2**](iwtsvirtualchannelcallback2.md)
</dt> <dd>

Não há suporte para essa interface.

</dd> <dt>

[**VirtualChannelGetInstance**](virtualchannelgetinstance.md)
</dt> <dd>

Chamado para fazer com que o plug-in crie uma instância da interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos os plug-ins implementados pela DLL.

</dd> </dl>

 

 




