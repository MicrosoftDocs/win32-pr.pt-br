---
description: Mostra como visualizar o vídeo de um dispositivo de captura de vídeo usando a API MFPlay.
ms.assetid: 6e2b1636-9d24-40e6-9ed4-e17d1af6a044
title: Exemplo de SimpleCapture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6fd255ad4c69254eb6ff64bdb99731e0c5ba9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164883"
---
# <a name="simplecapture-sample"></a><span data-ttu-id="b2546-103">Exemplo de SimpleCapture</span><span class="sxs-lookup"><span data-stu-id="b2546-103">SimpleCapture Sample</span></span>

<span data-ttu-id="b2546-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b2546-104">\[Deprecated.</span></span> <span data-ttu-id="b2546-105">A API MFPlay pode ser removida de versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="b2546-105">The MFPlay API may be removed from future releases of Windows.</span></span> <span data-ttu-id="b2546-106">Os aplicativos devem usar o [leitor de origem](source-reader.md) para captura de vídeo.\]</span><span class="sxs-lookup"><span data-stu-id="b2546-106">Applications should use the [Source Reader](source-reader.md) for video capture.\]</span></span>

<span data-ttu-id="b2546-107">Mostra como visualizar o vídeo de um dispositivo de captura de vídeo usando a API MFPlay.</span><span class="sxs-lookup"><span data-stu-id="b2546-107">Shows how to preview video from a video capture device, using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="b2546-108">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="b2546-108">APIs Demonstrated</span></span>

<span data-ttu-id="b2546-109">Este exemplo demonstra as seguintes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="b2546-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="b2546-110">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="b2546-110">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="b2546-111">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="b2546-111">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="b2546-112">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="b2546-112">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="b2546-113">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="b2546-113">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="b2546-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2546-114">Requirements</span></span>



| <span data-ttu-id="b2546-115">Produto</span><span class="sxs-lookup"><span data-stu-id="b2546-115">Product</span></span>                                                        | <span data-ttu-id="b2546-116">Versão</span><span class="sxs-lookup"><span data-stu-id="b2546-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="b2546-117">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="b2546-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="b2546-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b2546-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b2546-119">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="b2546-119">Downloading the Sample</span></span>

<span data-ttu-id="b2546-120">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span><span class="sxs-lookup"><span data-stu-id="b2546-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2546-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2546-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2546-122">Captura de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="b2546-122">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="b2546-123">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2546-123">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



