---
title: Escrevendo um módulo DVC do cliente
description: Para escrever um módulo de cliente DVC (canal virtual dinâmico), primeiro você deve implementar e registrar um plug-in de cliente RDC (Conexão de Área de Trabalho Remota).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa9f365034ff7771baf8eaeca102d7156f592e71d0cedffc97cef6d75b81fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008256"
---
# <a name="writing-a-client-dvc-module"></a>Escrevendo um módulo DVC do cliente

Para escrever um módulo de cliente DVC (canal virtual dinâmico), primeiro você deve implementar e registrar um plug-in de cliente RDC (Conexão de Área de Trabalho Remota). O plug-in do DVC é uma implementação [**de IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrado como um objeto COM (Component Object Model).

> [!Note]  
> O plug-in deve ser implementado em um modelo de threading livre. Não há suporte para a implementação de apartment-model.

 

Veja a seguir uma lista de interfaces que são implementadas por objetos que são instautados pelo plug-in.



| Interface                                                        | Descrição                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | Permite que o plug-in Conexão de Área de Trabalho Remota (RDC) seja carregado pelo cliente RDC (Conexão de Área de Trabalho Remota).<br/>                                                                 |
| [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | Notifica o plug-in Conexão de Área de Trabalho Remota cliente (RDC) sobre solicitações de entrada em um ouvinte específico.<br/>                                                                             |
| [**IWTSVirtualChannelCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | Recebe notificações sobre alterações de estado do canal ou dados recebidos. Cada instância dessa interface está associada a uma instância de [**IWTSVirtualChannel.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)<br/> |



 

Veja a seguir uma lista de interfaces implementadas por objetos que são instandados pelo cliente RDC (Conexão de Área de Trabalho Remota) e que fazem parte da estrutura.



| Interface                                                      | Descrição                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | Gerencia todos os plug-ins de cliente RDC (Conexão de Área de Trabalho Remota), ouvintes DVC ou canais virtuais estáticos.<br/> |
| [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | Gerencia as definições de configuração para cada ouvinte para a conexão DVC.<br/>                                |
| [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | Controla o estado do canal, bem como as gravações no canal.<br/>                                           |



 

A ilustração a seguir mostra a relação entre o cliente Conexão de Área de Trabalho Remota (RDC) e o plug-in do cliente RDC (Conexão de Área de Trabalho Remota).

![relação de cliente e plug-in](images/tsclient.png)

 

 





