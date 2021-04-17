---
title: Gravando dados usando um canal DVC
description: Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente.
ms.assetid: 33bacbf0-c558-497a-a08a-95eb398fad97
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd6f26e926958ceba5418a72849b75a66b11d2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780092"
---
# <a name="writing-data-by-using-a-dvc-channel"></a><span data-ttu-id="d3f9d-103">Gravando dados usando um canal DVC</span><span class="sxs-lookup"><span data-stu-id="d3f9d-103">Writing Data by Using a DVC Channel</span></span>

<span data-ttu-id="d3f9d-104">Gravar dados de canal usando um canal virtual dinâmico (DVC) é simétrico para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) e o cliente.</span><span class="sxs-lookup"><span data-stu-id="d3f9d-104">Writing channel data by using a dynamic virtual channel (DVC) is symmetric for both the Remote Desktop Session Host (RD Session Host) server and the client.</span></span> <span data-ttu-id="d3f9d-105">A gravação de dados do canal é implementada pelo método [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) da interface [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) .</span><span class="sxs-lookup"><span data-stu-id="d3f9d-105">The writing of channel data is implemented by the [**Write**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsvirtualchannel-write) method of the [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel) interface.</span></span>

<span data-ttu-id="d3f9d-106">A ilustração a seguir mostra o envio e recebimento do pacote de dados entre o cliente DVC e o servidor (plug-in DVC).</span><span class="sxs-lookup"><span data-stu-id="d3f9d-106">The following illustration shows the sending and receiving of the data packet between the DVC client and server (DVC plug-in).</span></span>

![enviando e recebendo um pacote de dados entre o cliente e o servidor do DVC](images/writedvcchannel.png)

 

 




