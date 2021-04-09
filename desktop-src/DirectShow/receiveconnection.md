---
description: ReceiveConnection
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: ReceiveConnection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fd9fe31f87a34dc3bfdfc4ecfb532255138b9c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087656"
---
# <a name="receiveconnection"></a><span data-ttu-id="3bd25-103">ReceiveConnection</span><span class="sxs-lookup"><span data-stu-id="3bd25-103">ReceiveConnection</span></span>

<span data-ttu-id="3bd25-104">Esse mecanismo permite que um pino de saída proponha uma alteração de formato ao seu par downstream, quando o novo formato requer um buffer maior.</span><span class="sxs-lookup"><span data-stu-id="3bd25-104">This mechanism enables an output pin to propose a format change to its downstream peer, when the new format requires a larger buffer.</span></span> <span data-ttu-id="3bd25-105">O pino de saída faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3bd25-105">The output pin does the following:</span></span>

1.  <span data-ttu-id="3bd25-106">Chama [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="3bd25-106">Calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the downstream input pin.</span></span>
2.  <span data-ttu-id="3bd25-107">Se `ReceiveConnection` tiver sucesso, chama [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="3bd25-107">If `ReceiveConnection` succeeds, calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) on the input pin.</span></span>

<span data-ttu-id="3bd25-108">Além disso, o pino de saída pode precisar chamar [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) e, em seguida, desconfirmar e reconfirmar o alocador para alterar os tamanhos do buffer.</span><span class="sxs-lookup"><span data-stu-id="3bd25-108">In addition, the output pin may need to call [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) and then decommit and recommit the allocator in order to change buffer sizes.</span></span> <span data-ttu-id="3bd25-109">Certifique-se de entregar todas as amostras pendentes no formato antigo antes de alterar o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="3bd25-109">Make sure to deliver all pending samples in the old format before changing the buffer size.</span></span>

<span data-ttu-id="3bd25-110">Alguns decodificadores MPEG-2 usam esse mecanismo para alternar entre MPEG-1 e MPEG-2 output ou se o tamanho do vídeo for alterado.</span><span class="sxs-lookup"><span data-stu-id="3bd25-110">Some MPEG-2 decoders use this mechanism to switch between MPEG-1 and MPEG-2 output or if the video size changes.</span></span>

 

 



