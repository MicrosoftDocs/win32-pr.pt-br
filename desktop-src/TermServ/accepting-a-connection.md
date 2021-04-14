---
title: Aceitando uma conexão (Serviços de Área de Trabalho Remota)
description: Em algum momento, o cliente do DVC (canal virtual dinâmico) solicitará uma conexão com o ouvinte DVC.
ms.assetid: eab17aa9-590c-4da2-a1a9-6e50a11d1de7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13aa0b78e459c85e7ba07e043e3da313b3f6118
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104552365"
---
# <a name="accepting-a-connection-remote-desktop-services"></a>Aceitando uma conexão (Serviços de Área de Trabalho Remota)

Em algum momento, o cliente do DVC (canal virtual dinâmico) solicitará uma conexão com o ouvinte DVC. Quando isso ocorre, o ouvinte pode gerar um canal de comunicação exclusivo para o cliente, que é manipulado pelo método [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) de [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback). Para obter um exemplo, consulte a implementação de **CDVCSamplePlugin:: OnNewChannelConnection** no código de exemplo do [plug-in cliente DVC](dvc-client-plug-in-example.md) .

A figura a seguir mostra a sequência de eventos para estabelecer uma conexão DVC. Os objetos sombreados são fornecidos pelo usuário (DVC Application/Service e [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), enquanto os objetos não sombreados fazem parte da estrutura (Host da Sessão da Área de Trabalho Remota (host da Sessão RD) Service, Listener e [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).

![sequência de eventos para estabelecer uma conexão DVC](images/acceptingconnection.png)

> [!Note]  
> Esta figura pressupõe que um objeto de ouvinte foi criado por meio de uma chamada [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) para [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)e que o plug-in especificou [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) como um parâmetro.

 

 

 




