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
# <a name="starting-a-dvc-listener"></a><span data-ttu-id="433d1-103">Iniciando um ouvinte DVC</span><span class="sxs-lookup"><span data-stu-id="433d1-103">Starting a DVC Listener</span></span>

<span data-ttu-id="433d1-104">Para estabelecer uma conexão bem-sucedida entre dois módulos DVC (canal virtual dinâmico) em execução no cliente e servidor do Conexão de Área de Trabalho Remota (RDC), um ouvinte DVC deve estar em execução e em um estado de escuta.</span><span class="sxs-lookup"><span data-stu-id="433d1-104">To establish a successful connection between two dynamic virtual channel (DVC) modules that are running on the Remote Desktop Connection (RDC) client and server, a DVC listener must be running and in a listening state.</span></span>

<span data-ttu-id="433d1-105">A instanciação de um ouvinte normalmente ocorre no método [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) do plug-in DVC.</span><span class="sxs-lookup"><span data-stu-id="433d1-105">The instantiation of a listener typically occurs in the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of the DVC plug-in.</span></span> <span data-ttu-id="433d1-106">No entanto, a instanciação não está limitada ao método **Initialize** e pode ser iniciada em qualquer ponto da execução do plug-in.</span><span class="sxs-lookup"><span data-stu-id="433d1-106">However, instantiation is not limited to the **Initialize** method, and can be started at any point of the plug-in execution.</span></span> <span data-ttu-id="433d1-107">O ouvinte é descrito pela interface [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) que é instanciada pelo [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="433d1-107">The listener is described by the [**IWTSListener**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener) interface which is instantiated by the [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="433d1-108">Uma instância para o Gerenciador de canal é passada para o plug-in no ponto de inicialização.</span><span class="sxs-lookup"><span data-stu-id="433d1-108">An instance to the channel manager is passed to the plug-in at the initialization point.</span></span> <span data-ttu-id="433d1-109">O plug-in pode manter uma referência interna à instância, contanto que seja necessário.</span><span class="sxs-lookup"><span data-stu-id="433d1-109">The plug-in can maintain an internal reference to the instance as long as it needs to.</span></span>

<span data-ttu-id="433d1-110">Um plug-in pode instanciar tantos ouvintes quantos forem necessários.</span><span class="sxs-lookup"><span data-stu-id="433d1-110">A plug-in can instantiate as many listeners as it needs to.</span></span> <span data-ttu-id="433d1-111">Qualquer conexão de entrada será tratada pelo [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), que é fornecido no método [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) de [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span><span class="sxs-lookup"><span data-stu-id="433d1-111">Any incoming connection will be handled by [**IWTSListenerCallback**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback), which is supplied in the [**CreateListener**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannelmanager-createlistener) method of [**IWTSVirtualChannelManager**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager).</span></span> <span data-ttu-id="433d1-112">Para obter um exemplo, confira a implementação de **CDVCSamplePlugin:: Initialize** no exemplo de código de [plug-in de cliente do DVC](dvc-client-plug-in-example.md) .</span><span class="sxs-lookup"><span data-stu-id="433d1-112">For an example, see the implementation of **CDVCSamplePlugin::Initialize** in the [DVC Client Plug-in Example](dvc-client-plug-in-example.md) sample code.</span></span>

 

 




