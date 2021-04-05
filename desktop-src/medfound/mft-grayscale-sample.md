---
description: Mostra como implementar um efeito de vídeo como uma Media Foundation transformação (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Exemplo de MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091051"
---
# <a name="mft_grayscale-sample"></a><span data-ttu-id="9be53-103">Exemplo de escala de cinza da MFT \_</span><span class="sxs-lookup"><span data-stu-id="9be53-103">MFT\_Grayscale Sample</span></span>

<span data-ttu-id="9be53-104">Mostra como implementar um efeito de vídeo como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="9be53-104">Shows how to implement a video effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="9be53-105">O MFT em escala de cinza converte o vídeo YUV em escala de cinza definindo os valores de croma no vídeo como neutro.</span><span class="sxs-lookup"><span data-stu-id="9be53-105">The grayscale MFT converts YUV video to grayscale by setting the chroma values in the video to neutral.</span></span> <span data-ttu-id="9be53-106">O MFT aceita vídeo descompactado nos formatos UYVY, YUY2 ou NV12.</span><span class="sxs-lookup"><span data-stu-id="9be53-106">The MFT accepts uncompressed video in UYVY, YUY2, or NV12 formats.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="9be53-107">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="9be53-107">APIs Demonstrated</span></span>

<span data-ttu-id="9be53-108">Este exemplo demonstra as seguintes interfaces de Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="9be53-108">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="9be53-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="9be53-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="9be53-110">Uso</span><span class="sxs-lookup"><span data-stu-id="9be53-110">Usage</span></span>

<span data-ttu-id="9be53-111">O exemplo de escala de cinza do MFT \_ cria uma DLL que é um servidor com para o MFT.</span><span class="sxs-lookup"><span data-stu-id="9be53-111">The MFT\_GrayScale sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="9be53-112">Antes de usar o MFT, você deve registrar a DLL.</span><span class="sxs-lookup"><span data-stu-id="9be53-112">Before using the MFT, you must register the DLL.</span></span>

<span data-ttu-id="9be53-113">Para ver o MFT em escala de cinza em uso, execute o [exemplo PlaybackFX](/previous-versions//bb970336(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9be53-113">To see the grayscale MFT in use, run the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)).</span></span> <span data-ttu-id="9be53-114">Você também pode usar a ferramenta TopoEdit para criar uma topologia que inclui o MFT em tons de cinza.</span><span class="sxs-lookup"><span data-stu-id="9be53-114">You can also use the TopoEdit tool to build a topology that includes the grayscale MFT.</span></span> <span data-ttu-id="9be53-115">Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="9be53-115">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9be53-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9be53-116">Requirements</span></span>



| <span data-ttu-id="9be53-117">Produto</span><span class="sxs-lookup"><span data-stu-id="9be53-117">Product</span></span>                                                        | <span data-ttu-id="9be53-118">Versão</span><span class="sxs-lookup"><span data-stu-id="9be53-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="9be53-119">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="9be53-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="9be53-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9be53-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="9be53-121">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9be53-121">Downloading the Sample</span></span>

<span data-ttu-id="9be53-122">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span><span class="sxs-lookup"><span data-stu-id="9be53-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9be53-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9be53-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9be53-124">Sobre o vídeo YUV</span><span class="sxs-lookup"><span data-stu-id="9be53-124">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="9be53-125">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9be53-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="9be53-126">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9be53-126">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="9be53-127">Exemplo de AudioDelay de MFT \_</span><span class="sxs-lookup"><span data-stu-id="9be53-127">MFT\_AudioDelay Sample</span></span>](mft-audiodelay-sample.md)
</dt> <dt>

[<span data-ttu-id="9be53-128">Gravando uma MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="9be53-128">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
