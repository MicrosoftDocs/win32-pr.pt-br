---
description: Mostra como usar o Microsoft DirectX vídeo Acceleration High Definition (DXVA-HD).
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: Exemplo de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826731"
---
# <a name="dxva-hd-sample"></a><span data-ttu-id="4a871-103">Exemplo de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="4a871-103">DXVA-HD Sample</span></span>

<span data-ttu-id="4a871-104">Mostra como usar o Microsoft DirectX vídeo Acceleration High Definition (DXVA-HD).</span><span class="sxs-lookup"><span data-stu-id="4a871-104">Shows how to use Microsoft DirectX Video Acceleration High Definition (DXVA-HD).</span></span>

<span data-ttu-id="4a871-105">Esse exemplo é essencialmente uma porta do [exemplo de \_ VideoProc DXVA2](dxva2-videoproc-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4a871-105">This sample is essentially a port of the [DXVA2\_VideoProc Sample](dxva2-videoproc-sample.md).</span></span> <span data-ttu-id="4a871-106">Ele tem as mesmas funções básicas e a maioria dos comandos de teclado é a mesma.</span><span class="sxs-lookup"><span data-stu-id="4a871-106">It has the same basic functions, and most of the keyboard commands are the same.</span></span>

<span data-ttu-id="4a871-107">O exemplo gera programaticamente vídeo com um fluxo primário e um subfluxo.</span><span class="sxs-lookup"><span data-stu-id="4a871-107">The sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="4a871-108">O fluxo primário exibe barras de cores SMPTE.</span><span class="sxs-lookup"><span data-stu-id="4a871-108">The primary stream displays SMPTE color bars.</span></span> <span data-ttu-id="4a871-109">O Subfluxo é misturado no fluxo principal usando Luma de chave.</span><span class="sxs-lookup"><span data-stu-id="4a871-109">The substream is alpha-blended onto the primary stream using luma keying.</span></span> <span data-ttu-id="4a871-110">O usuário pode alterar os parâmetros de processamento de vídeo, incluindo o valor alfa do planar, os retângulos de origem e de destino, os ajustes de cor e o espaço de cores.</span><span class="sxs-lookup"><span data-stu-id="4a871-110">The user can change the video processing parameters, including the planar alpha value, source and destination rectangles, color adjustments, and color space.</span></span> <span data-ttu-id="4a871-111">A imagem a seguir mostra o vídeo que é gerado.</span><span class="sxs-lookup"><span data-stu-id="4a871-111">The following image shows that video that is generated.</span></span>

![captura de tela do exemplo de DXVA-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="4a871-113">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="4a871-113">APIs Demonstrated</span></span>

<span data-ttu-id="4a871-114">Este exemplo demonstra as seguintes interfaces de DXVA-HD:</span><span class="sxs-lookup"><span data-stu-id="4a871-114">This sample demonstrates the following DXVA-HD interfaces:</span></span>

-   [<span data-ttu-id="4a871-115">**\_Dispositivo IDXVAHD**</span><span class="sxs-lookup"><span data-stu-id="4a871-115">**IDXVAHD\_Device**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [<span data-ttu-id="4a871-116">**IDXVAHD \_ VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="4a871-116">**IDXVAHD\_VideoProcessor**</span></span>](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a><span data-ttu-id="4a871-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a871-117">Requirements</span></span>



| <span data-ttu-id="4a871-118">Produto</span><span class="sxs-lookup"><span data-stu-id="4a871-118">Product</span></span>                                                        | <span data-ttu-id="4a871-119">Versão</span><span class="sxs-lookup"><span data-stu-id="4a871-119">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="4a871-120">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="4a871-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="4a871-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4a871-121">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4a871-122">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="4a871-122">Downloading the Sample</span></span>

<span data-ttu-id="4a871-123">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span><span class="sxs-lookup"><span data-stu-id="4a871-123">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a871-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a871-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a871-125">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="4a871-125">DXVA-HD</span></span>](dxva-hd.md)
</dt> <dt>

[<span data-ttu-id="4a871-126">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4a871-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



