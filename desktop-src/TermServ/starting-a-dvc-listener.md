---
title: Iniciando um ouvinte DVC
description: Para estabelecer uma conexão bem-sucedida entre dois módulos DVC (canal virtual dinâmico) que estão em execução no cliente e no servidor Conexão de Área de Trabalho Remota (RDC), um ouvinte DVC deve estar em execução e em um estado de escuta.
ms.assetid: c9130375-eb60-4996-84f5-a1081144e130
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d440069cb64597c16a14323a67926376bf1c425f5a29c77e451c52866a5399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000446"
---
# <a name="starting-a-dvc-listener"></a>Iniciando um ouvinte DVC

Para estabelecer uma conexão bem-sucedida entre dois módulos DVC (canal virtual dinâmico) que estão em execução no cliente e no servidor Conexão de Área de Trabalho Remota (RDC), um ouvinte DVC deve estar em execução e em um estado de escuta.

A insta instação de um ouvinte normalmente ocorre no método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) do plug-in DVC. No entanto, a instalização não está limitada ao método **Initialize** e pode ser iniciada em qualquer ponto da execução do plug-in. O ouvinte é descrito pela interface [**IWTSListener,**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) que é instanciada pelo [**IWTSVirtualChannelManager.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) Uma instância para o gerenciador de canais é passada para o plug-in no ponto de inicialização. O plug-in pode manter uma referência interna à instância, desde que seja necessário.

Um plug-in pode insinuar quantos ouvintes precisar. Qualquer conexão de entrada será tratada por [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), que é fornecido no método [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) [**de IWTSVirtualChannelManager.**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) Para ver um exemplo, consulte a implementação **de CDVCSamplePlugin::Initialize** no código de exemplo de Exemplo de [Plug-in](dvc-client-plug-in-example.md) do Cliente DVC.

 

 




