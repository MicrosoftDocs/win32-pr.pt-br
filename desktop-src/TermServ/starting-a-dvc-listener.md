---
title: Iniciando um ouvinte DVC
description: Para estabelecer uma conexão bem-sucedida entre dois módulos DVC (canal virtual dinâmico) em execução no cliente e servidor do Conexão de Área de Trabalho Remota (RDC), um ouvinte DVC deve estar em execução e em um estado de escuta.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b625d5547facd0487af170af9d59eddd6bfed87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292786"
---
# <a name="starting-a-dvc-listener"></a>Iniciando um ouvinte DVC

Para estabelecer uma conexão bem-sucedida entre dois módulos DVC (canal virtual dinâmico) em execução no cliente e servidor do Conexão de Área de Trabalho Remota (RDC), um ouvinte DVC deve estar em execução e em um estado de escuta.

A instanciação de um ouvinte normalmente ocorre no método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) do plug-in DVC. No entanto, a instanciação não está limitada ao método **Initialize** e pode ser iniciada em qualquer ponto da execução do plug-in. O ouvinte é descrito pela interface [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) que é instanciada pelo [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Uma instância para o Gerenciador de canal é passada para o plug-in no ponto de inicialização. O plug-in pode manter uma referência interna à instância, contanto que seja necessário.

Um plug-in pode instanciar tantos ouvintes quantos forem necessários. Qualquer conexão de entrada será tratada pelo [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), que é fornecido no método [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager). Para obter um exemplo, confira a implementação de **CDVCSamplePlugin:: Initialize** no exemplo de código de [plug-in de cliente do DVC](dvc-client-plug-in-example.md) .

 

 




