---
description: Mostra como gravar um decodificador para Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Exemplo de decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920630"
---
# <a name="decoder-sample"></a><span data-ttu-id="86867-103">Exemplo de decodificador</span><span class="sxs-lookup"><span data-stu-id="86867-103">Decoder Sample</span></span>

<span data-ttu-id="86867-104">Mostra como gravar um decodificador para Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="86867-104">Shows how to write a decoder for Microsoft Media Foundation.</span></span>

<span data-ttu-id="86867-105">Este exemplo implementa um decodificador de vídeo MPEG-1 simulado que exibe o código de tempo para cada quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="86867-105">This sample implements a mock MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="86867-106">Na verdade, ele não decodificará o fragmentado MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="86867-106">It does not actually decode the MPEG-1 bitstream.</span></span> <span data-ttu-id="86867-107">A imagem a seguir mostra a saída de vídeo do decodificador.</span><span class="sxs-lookup"><span data-stu-id="86867-107">The following image shows the video output from the decoder.</span></span>

![captura de tela de um quadro de vídeo do decodificador](images/decodersample.png)

> [!Note]  
> <span data-ttu-id="86867-109">Antes do SDK do Windows para o Windows 7, esse exemplo foi incluído como parte do [exemplo de MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="86867-109">Prior to the Windows SDK for Windows 7, this sample was included as part of the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="86867-110">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="86867-110">APIs Demonstrated</span></span>

<span data-ttu-id="86867-111">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="86867-111">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="86867-112">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="86867-112">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a><span data-ttu-id="86867-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86867-113">Requirements</span></span>



| <span data-ttu-id="86867-114">Produto</span><span class="sxs-lookup"><span data-stu-id="86867-114">Product</span></span>                                                        | <span data-ttu-id="86867-115">Versão</span><span class="sxs-lookup"><span data-stu-id="86867-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="86867-116">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="86867-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="86867-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86867-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="86867-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="86867-118">Downloading the Sample</span></span>

<span data-ttu-id="86867-119">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span><span class="sxs-lookup"><span data-stu-id="86867-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86867-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86867-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86867-121">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86867-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="86867-122">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86867-122">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="86867-123">Gravando uma MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="86867-123">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



