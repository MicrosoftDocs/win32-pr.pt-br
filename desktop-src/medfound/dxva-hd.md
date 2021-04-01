---
description: A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) é uma API para processamento de vídeo acelerado por hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646588"
---
# <a name="dxva-hd"></a><span data-ttu-id="8038e-103">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="8038e-103">DXVA-HD</span></span>

<span data-ttu-id="8038e-104">A alta definição da aceleração de vídeo do Microsoft DirectX (DXVA-HD) é uma API para processamento de vídeo acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="8038e-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <span data-ttu-id="8038e-105">O DXVA-HD usa a GPU para executar funções como desentrelaçamento, composição e conversão de espaço de cor.</span><span class="sxs-lookup"><span data-stu-id="8038e-105">DXVA-HD uses the GPU to perform functions such as deinterlacing, compositing, and color-space conversion.</span></span>

<span data-ttu-id="8038e-106">O DXVA-HD é semelhante ao [processamento de vídeo de DXVA](dxva-video-processing.md) (DXVA-VP), mas oferece recursos avançados e um modelo de processamento mais simples.</span><span class="sxs-lookup"><span data-stu-id="8038e-106">DXVA-HD is similar to [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), but offers enhanced features and a simpler processing model.</span></span> <span data-ttu-id="8038e-107">Ao fornecer um modelo de composição mais flexível, o DXVA-HD foi projetado para dar suporte à próxima geração de formatos ópticos de HD e padrões de difusão.</span><span class="sxs-lookup"><span data-stu-id="8038e-107">By providing a more flexible composition model, DXVA-HD is designed to support the next generation of HD optical formats and broadcast standards.</span></span>

<span data-ttu-id="8038e-108">A API de DXVA-HD requer um driver de vídeo WDDM que dá suporte à DDI (interface de driver de dispositivo) de DXVA-HD ou um processador de software de plug-in.</span><span class="sxs-lookup"><span data-stu-id="8038e-108">The DXVA-HD API requires either a WDDM display driver that supports the DXVA-HD device driver interface (DDI), or a plug-in software processor.</span></span>

-   [<span data-ttu-id="8038e-109">Melhorias em relação a DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="8038e-109">Improvements over DXVA-VP</span></span>](#improvements-over-dxva-vp)
-   [<span data-ttu-id="8038e-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8038e-110">Related topics</span></span>](#related-topics)

## <a name="improvements-over-dxva-vp"></a><span data-ttu-id="8038e-111">Melhorias em relação a DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="8038e-111">Improvements over DXVA-VP</span></span>

<span data-ttu-id="8038e-112">DXVA-HD expande o conjunto de recursos fornecidos pelo DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="8038e-112">DXVA-HD expands the set of features provided by DXVA-VP.</span></span> <span data-ttu-id="8038e-113">Os aprimoramentos incluem:</span><span class="sxs-lookup"><span data-stu-id="8038e-113">Enhancements include:</span></span>

-   <span data-ttu-id="8038e-114">Mixagem de RGB e YUV.</span><span class="sxs-lookup"><span data-stu-id="8038e-114">RGB and YUV mixing.</span></span> <span data-ttu-id="8038e-115">Qualquer fluxo pode ser RGB ou YUV.</span><span class="sxs-lookup"><span data-stu-id="8038e-115">Any stream can be either RGB or YUV.</span></span> <span data-ttu-id="8038e-116">Não há mais uma distinção entre o fluxo principal e os subfluxos.</span><span class="sxs-lookup"><span data-stu-id="8038e-116">There is no longer a distinction between the primary stream and the substreams.</span></span>
-   <span data-ttu-id="8038e-117">Desentrelaçamento de vários fluxos.</span><span class="sxs-lookup"><span data-stu-id="8038e-117">Deinterlacing of multiple streams.</span></span> <span data-ttu-id="8038e-118">Qualquer fluxo pode ser progressivo ou entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="8038e-118">Any stream can be either progressive or interlaced.</span></span> <span data-ttu-id="8038e-119">Além disso, a cadência e a taxa de quadros podem variar de um fluxo de entrada para o outro.</span><span class="sxs-lookup"><span data-stu-id="8038e-119">Moreover, the cadence and frame rate can can vary from one input stream to the next.</span></span>
-   <span data-ttu-id="8038e-120">Cores de fundo RGB.</span><span class="sxs-lookup"><span data-stu-id="8038e-120">RGB background colors.</span></span> <span data-ttu-id="8038e-121">Anteriormente, há suporte apenas para cores de plano de fundo YUV.</span><span class="sxs-lookup"><span data-stu-id="8038e-121">Previously, only YUV background colors were supported.</span></span>
-   <span data-ttu-id="8038e-122">Luma de chave.</span><span class="sxs-lookup"><span data-stu-id="8038e-122">Luma keying.</span></span> <span data-ttu-id="8038e-123">Quando o Luma de chaveamento está habilitado, os valores de Luma que se enquadram em um intervalo designado tornam-se transparentes</span><span class="sxs-lookup"><span data-stu-id="8038e-123">When luma keying is enabled, luma values that fall within a designated range become transparent.</span></span>
-   <span data-ttu-id="8038e-124">Alternância dinâmica entre os modos de desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="8038e-124">Dynamic switching between deinterlace modes.</span></span>

<span data-ttu-id="8038e-125">O DXVA-HD também define alguns recursos avançados aos quais os drivers podem dar suporte.</span><span class="sxs-lookup"><span data-stu-id="8038e-125">DXVA-HD also defines some advanced features that drivers can support.</span></span> <span data-ttu-id="8038e-126">No entanto, os aplicativos não devem pressupor que todos os drivers oferecerão suporte a esses recursos.</span><span class="sxs-lookup"><span data-stu-id="8038e-126">However, applications should not assume that all drivers will support these features.</span></span> <span data-ttu-id="8038e-127">Os recursos avançados incluem:</span><span class="sxs-lookup"><span data-stu-id="8038e-127">The advanced features include:</span></span>

-   <span data-ttu-id="8038e-128">Telecineon inverso (por exemplo, 60i para 24p).</span><span class="sxs-lookup"><span data-stu-id="8038e-128">Inverse telecine (for example, 60i to 24p).</span></span>
-   <span data-ttu-id="8038e-129">Conversão de taxa de quadros (por exemplo, 24p para 120P).</span><span class="sxs-lookup"><span data-stu-id="8038e-129">Frame-rate conversion (for example, 24p to 120p).</span></span>
-   <span data-ttu-id="8038e-130">Modos de preenchimento alfa.</span><span class="sxs-lookup"><span data-stu-id="8038e-130">Alpha-fill modes.</span></span>
-   <span data-ttu-id="8038e-131">Redução de ruído e filtragem de aprimoramento de borda.</span><span class="sxs-lookup"><span data-stu-id="8038e-131">Noise reduction and edge enhancement filtering.</span></span>
-   <span data-ttu-id="8038e-132">Anamorphic dimensionamento não linear.</span><span class="sxs-lookup"><span data-stu-id="8038e-132">Anamorphic non-linear scaling.</span></span>
-   <span data-ttu-id="8038e-133">YCbCr estendido (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="8038e-133">Extended YCbCr (xvYCC).</span></span>

<span data-ttu-id="8038e-134">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="8038e-134">This section contains the following topics.</span></span>

-   [<span data-ttu-id="8038e-135">Criando um processador de vídeo de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="8038e-135">Creating a DXVA-HD Video Processor</span></span>](creating-a-dxva-hd-video-processor.md)
-   [<span data-ttu-id="8038e-136">Verificando os formatos de DXVA-HD com suporte</span><span class="sxs-lookup"><span data-stu-id="8038e-136">Checking Supported DXVA-HD Formats</span></span>](checking-supported-dxva-hd-formats.md)
-   [<span data-ttu-id="8038e-137">Criando superfícies de vídeo de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="8038e-137">Creating DXVA-HD Video Surfaces</span></span>](creating-dxva-hd-video-surfaces.md)
-   [<span data-ttu-id="8038e-138">Definindo Estados de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="8038e-138">Setting DXVA-HD States</span></span>](setting-dxva-hd-states.md)
-   [<span data-ttu-id="8038e-139">Executando o blit DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="8038e-139">Performing the DXVA-HD Blit</span></span>](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a><span data-ttu-id="8038e-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8038e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8038e-141">Aceleração de vídeo do DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="8038e-141">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="8038e-142">Exemplo de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="8038e-142">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
</dt> </dl>

 

 



