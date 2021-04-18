---
description: Codificação de vídeo com compactação temporal
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codificação de vídeo com compactação temporal (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791556"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a><span data-ttu-id="a927d-103">Codificação de vídeo com compactação temporal (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="a927d-103">Video Encoding with Temporal Compression (Microsoft Media Foundation)</span></span>

<span data-ttu-id="a927d-104">Para obter as maiores taxas de compactação possíveis, os codecs de vídeo do Windows Media usam a *compactação temporal*.</span><span class="sxs-lookup"><span data-stu-id="a927d-104">To achieve the highest compression ratios possible, the Windows Media Video codecs use *temporal compression*.</span></span> <span data-ttu-id="a927d-105">A compactação temporal é uma técnica para reduzir o tamanho do vídeo compactado não codificando cada quadro como uma imagem completa.</span><span class="sxs-lookup"><span data-stu-id="a927d-105">Temporal compression is a technique of reducing compressed video size by not encoding each frame as a complete image.</span></span> <span data-ttu-id="a927d-106">Os quadros codificados completamente (como uma imagem estática) são chamados de *quadros-chave*.</span><span class="sxs-lookup"><span data-stu-id="a927d-106">The frames that are encoded completely (like a static image) are called *key frames*.</span></span> <span data-ttu-id="a927d-107">Todos os outros quadros do vídeo são representados por dados que especificam a alteração desde o último quadro.</span><span class="sxs-lookup"><span data-stu-id="a927d-107">All other frames in the video are represented by data specifying the change since the last frame.</span></span> <span data-ttu-id="a927d-108">Esses quadros são chamados de *quadros Delta*.</span><span class="sxs-lookup"><span data-stu-id="a927d-108">These frames are called *delta frames*.</span></span>

<span data-ttu-id="a927d-109">A quantidade de compactação que pode ser obtida usando a compactação temporal depende do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a927d-109">The amount of compression that can be achieved using temporal compression depends upon the content.</span></span> <span data-ttu-id="a927d-110">Se o vídeo for estático, sem muito movimento ou outras alterações na imagem, muitos quadros Delta poderão ser criados para cada quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="a927d-110">If the video is static, without a lot of motion or other changes in image, many delta frames can be created for each key frame.</span></span> <span data-ttu-id="a927d-111">Quanto mais quadros Delta forem usados, menor será o fluxo de vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="a927d-111">The more delta frames that are used, the smaller the encoded video stream.</span></span> <span data-ttu-id="a927d-112">No entanto, se o vídeo for dinâmico, com muitas cores de movimento ou alteração, o benefício de usar a compactação temporal será menor.</span><span class="sxs-lookup"><span data-stu-id="a927d-112">However, if the video is dynamic, with lots of motion or changing colors, the benefit of using temporal compression is smaller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a927d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a927d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a927d-114">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="a927d-114">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



