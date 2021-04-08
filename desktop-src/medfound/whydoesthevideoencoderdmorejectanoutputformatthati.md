---
description: Por que o codificador de vídeo rejeita um formato de saída que tento definir, quando recuperei o formato do mesmo objeto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Por que o codificador de vídeo rejeita um formato de saída que tento definir, quando recuperei o formato do mesmo objeto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010797"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a><span data-ttu-id="663da-103">Por que o codificador de vídeo rejeita um formato de saída que tento definir, quando recuperei o formato do mesmo objeto?</span><span class="sxs-lookup"><span data-stu-id="663da-103">Why does the video encoder reject an output format that I try to set, when I retrieved the format from the same object?</span></span>

<span data-ttu-id="663da-104">Diferentemente dos tipos de saída do codificador de áudio, as saídas com suporte enumeradas pelos codificadores de vídeo não são concluídas como entregues.</span><span class="sxs-lookup"><span data-stu-id="663da-104">Unlike audio encoder output types, the supported outputs enumerated by the video encoders are not complete as delivered.</span></span> <span data-ttu-id="663da-105">Você deve definir a taxa de bits do fluxo no membro **dwBitrate** da estrutura **VIDEOINFOHEADER** para corresponder ao valor definido para a propriedade [MFPKEY \_ RAVG](mfpkey-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="663da-105">You must set the bit rate of the stream in the **dwBitrate** member of the **VIDEOINFOHEADER** structure to match the value set for the [MFPKEY\_RAVG](mfpkey-ravgproperty.md) property.</span></span>

<span data-ttu-id="663da-106">Depois que todas as opções forem definidas da maneira desejada, você deverá recuperar os dados privados do codec e acrescentá-los à estrutura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="663da-106">After all of the options are set the way that you want them, you must retrieve the codec private data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="663da-107">Para obter mais informações, consulte [usando dados privados do codec de vídeo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="663da-107">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="663da-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="663da-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="663da-109">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="663da-109">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



