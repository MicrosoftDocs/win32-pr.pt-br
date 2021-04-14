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
# <a name="accepting-a-connection-remote-desktop-services"></a><span data-ttu-id="b42b2-103">Aceitando uma conexão (Serviços de Área de Trabalho Remota)</span><span class="sxs-lookup"><span data-stu-id="b42b2-103">Accepting a Connection (Remote Desktop Services)</span></span>

<span data-ttu-id="b42b2-104">Em algum momento, o cliente do DVC (canal virtual dinâmico) solicitará uma conexão com o ouvinte DVC.</span><span class="sxs-lookup"><span data-stu-id="b42b2-104">At some point in time, the dynamic virtual channel (DVC) client will request a connection to the DVC listener.</span></span> <span data-ttu-id="b42b2-105">Quando isso ocorre, o ouvinte pode gerar um canal de comunicação exclusivo para o cliente, que é manipulado pelo método [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) de [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span><span class="sxs-lookup"><span data-stu-id="b42b2-105">When this occurs, the listener can spawn a unique communication channel to the client, which is handled by the [**OnNewChannelConnection**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtslistenercallback-onnewchannelconnection) method of [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback).</span></span> <span data-ttu-id="b42b2-106">Para obter um exemplo, consulte a implementação de **CDVCSamplePlugin:: OnNewChannelConnection** no código de exemplo do [plug-in cliente DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="b42b2-106">For an example, see the implementation of **CDVCSamplePlugin::OnNewChannelConnection** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

<span data-ttu-id="b42b2-107">A figura a seguir mostra a sequência de eventos para estabelecer uma conexão DVC.</span><span class="sxs-lookup"><span data-stu-id="b42b2-107">The following figure shows the sequence of events for establishing a DVC connection.</span></span> <span data-ttu-id="b42b2-108">Os objetos sombreados são fornecidos pelo usuário (DVC Application/Service e [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), enquanto os objetos não sombreados fazem parte da estrutura (Host da Sessão da Área de Trabalho Remota (host da Sessão RD) Service, Listener e [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span><span class="sxs-lookup"><span data-stu-id="b42b2-108">The shaded objects are user-supplied (DVC application/service and [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)), while the un-shaded objects are part of the framework (Remote Desktop Session Host (RD Session Host) service, listener, and [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)).</span></span>

![sequência de eventos para estabelecer uma conexão DVC](images/acceptingconnection.png)

> [!Note]  
> <span data-ttu-id="b42b2-110">Esta figura pressupõe que um objeto de ouvinte foi criado por meio de uma chamada [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) para [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager)e que o plug-in especificou [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b42b2-110">This figure assumes that a listener object has been created through a [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) call to [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager), and that the plug-in has specified [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback) as a parameter.</span></span>

 

 

 




