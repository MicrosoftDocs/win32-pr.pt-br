---
title: Escrevendo um módulo de DVC de cliente
description: Para gravar um módulo de cliente de canal virtual dinâmico (DVC), você deve primeiro implementar e registrar um plug-in de cliente Conexão de Área de Trabalho Remota (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105757921"
---
# <a name="writing-a-client-dvc-module"></a>Escrevendo um módulo de DVC de cliente

Para gravar um módulo de cliente de canal virtual dinâmico (DVC), você deve primeiro implementar e registrar um plug-in de cliente Conexão de Área de Trabalho Remota (RDC). O plug-in DVC é uma implementação de [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrada como um objeto Component Object Model (com).

> [!Note]  
> O plug-in deve ser implementado em um modelo de Threading livre. Não há suporte para implementação de modelo de apartamento.

 

A seguir está uma lista de interfaces que são implementadas por objetos que são instanciados pelo plug-in do.



| Interface                                                        | Descrição                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Permite que o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) seja carregado pelo cliente Conexão de Área de Trabalho Remota (RDC).<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Notifica o plug-in do cliente Conexão de Área de Trabalho Remota (RDC) sobre solicitações de entrada em um ouvinte específico.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Recebe notificações sobre alterações de estado de canal ou dados recebidos. Cada instância dessa interface é associada a uma instância de [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).<br/> |



 

A seguir está uma lista de interfaces que são implementadas por objetos que são instanciados pelo cliente de Conexão de Área de Trabalho Remota (RDC) e fazem parte da estrutura.



| Interface                                                      | Descrição                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Gerencia todos os plug-ins de cliente Conexão de Área de Trabalho Remota (RDC), ouvintes DVC ou canais virtuais estáticos.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Gerencia as definições de configuração de cada ouvinte para a conexão DVC.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Controla o estado do canal, bem como gravações no canal.<br/>                                           |



 

A ilustração a seguir mostra a relação entre o cliente de Conexão de Área de Trabalho Remota (RDC) e o plug-in cliente Conexão de Área de Trabalho Remota (RDC).

![relação entre cliente e plug-in](images/tsclient.png)

 

 





