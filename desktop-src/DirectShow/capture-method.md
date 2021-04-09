---
description: O método Capture captura uma imagem ainda do quadro de vídeo quando o objeto MSWebDVD está no modo sem janela.
ms.assetid: 704e64ef-3593-403c-8ecf-625fb4983882
title: Método Capture
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db16bbc6ef50de303dbcdac66bd066861bb5811
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087313"
---
# <a name="capture-method"></a><span data-ttu-id="588da-103">Método Capture</span><span class="sxs-lookup"><span data-stu-id="588da-103">Capture Method</span></span>

> [!Note]  
> <span data-ttu-id="588da-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="588da-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="588da-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="588da-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="588da-106">O `Capture` método captura uma imagem ainda do quadro de vídeo quando o objeto MSWebDVD está no modo sem janela.</span><span class="sxs-lookup"><span data-stu-id="588da-106">The `Capture` method captures a still image from the video frame when the MSWebDVD object is in windowless mode.</span></span>

``` syntax
MSWebDVD.Capture()
```

## <a name="remarks"></a><span data-ttu-id="588da-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="588da-107">Remarks</span></span>

<span data-ttu-id="588da-108">Esse método captura o quadro atual da imagem de DVD-Video e cola-o em uma janela da qual o usuário pode salvar ou editar a imagem.</span><span class="sxs-lookup"><span data-stu-id="588da-108">This method captures the current frame from the DVD-Video image and pastes it into a window from which the user can save or edit the image.</span></span> <span data-ttu-id="588da-109">O objeto MSWebDVD deve estar no modo sem janela para que esse método tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="588da-109">The MSWebDVD object must be in windowless mode for this method to succeed.</span></span>

 

 



