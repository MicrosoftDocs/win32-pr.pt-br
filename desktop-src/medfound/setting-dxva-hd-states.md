---
description: Definindo Estados de DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Definindo Estados de DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092694"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="06ebe-103">Definindo Estados de DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="06ebe-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="06ebe-104">Durante o processamento de vídeo, o dispositivo de alta definição (DXVA-HD) de aceleração de vídeo do Microsoft DirectX mantém um estado persistente de um quadro para o outro.</span><span class="sxs-lookup"><span data-stu-id="06ebe-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="06ebe-105">Cada Estado tem um padrão documentado.</span><span class="sxs-lookup"><span data-stu-id="06ebe-105">Each state has a documented default.</span></span> <span data-ttu-id="06ebe-106">Depois de configurar o dispositivo, defina os Estados que você deseja alterar de seus padrões.</span><span class="sxs-lookup"><span data-stu-id="06ebe-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="06ebe-107">Antes de processar cada quadro, atualize todos os Estados que devem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="06ebe-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="06ebe-108">Esse design difere do DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="06ebe-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="06ebe-109">No DXVA-VP, o aplicativo deve especificar todos os parâmetros de VP com cada quadro.</span><span class="sxs-lookup"><span data-stu-id="06ebe-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="06ebe-110">Os Estados do dispositivo se enquadram em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="06ebe-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="06ebe-111">Os Estados de *fluxo* aplicam cada fluxo de entrada separadamente.</span><span class="sxs-lookup"><span data-stu-id="06ebe-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="06ebe-112">Você pode aplicar configurações diferentes a cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="06ebe-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="06ebe-113">Os Estados *blit* se aplicam globalmente a todo o blit de processamento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="06ebe-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="06ebe-114">Os Estados de fluxo a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="06ebe-114">The following stream states are defined.</span></span>



| <span data-ttu-id="06ebe-115">Estado do fluxo</span><span class="sxs-lookup"><span data-stu-id="06ebe-115">Stream State</span></span>                                   | <span data-ttu-id="06ebe-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="06ebe-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06ebe-117">**DXVAHD \_ de \_ estado de fluxo \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="06ebe-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="06ebe-118">Formato de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="06ebe-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="06ebe-119">**\_formato de \_ quadro de estado de fluxo DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="06ebe-120">Entrelaça.</span><span class="sxs-lookup"><span data-stu-id="06ebe-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="06ebe-121">**\_espaço de \_ cor de entrada de estado de fluxo DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="06ebe-122">Espaço de cores de entrada.</span><span class="sxs-lookup"><span data-stu-id="06ebe-122">Input color space.</span></span> <span data-ttu-id="06ebe-123">Esse estado especifica o intervalo de cores RGB e a matriz de transferência YCbCr para o fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="06ebe-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="06ebe-124">**\_taxa de \_ saída de estado de fluxo DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="06ebe-125">Taxa de quadros de saída.</span><span class="sxs-lookup"><span data-stu-id="06ebe-125">Output frame rate.</span></span> <span data-ttu-id="06ebe-126">Esse estado controla a conversão de taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="06ebe-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="06ebe-127">**\_Rect de \_ origem de estado de fluxo DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="06ebe-128">Retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="06ebe-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="06ebe-129">**\_Rect de \_ destino de estado de fluxo DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="06ebe-130">Retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="06ebe-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="06ebe-131">**DXVAHD \_ de \_ estado de fluxo \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="06ebe-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="06ebe-132">Planar alfa.</span><span class="sxs-lookup"><span data-stu-id="06ebe-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="06ebe-133">**\_paleta de \_ Estados de fluxo DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="06ebe-134">Paleta de cores.</span><span class="sxs-lookup"><span data-stu-id="06ebe-134">Color palette.</span></span> <span data-ttu-id="06ebe-135">Esse Estado se aplica somente aos formatos de entrada palettized.</span><span class="sxs-lookup"><span data-stu-id="06ebe-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="06ebe-136">**\_chave de \_ Luma de estado de fluxo DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="06ebe-137">Chave Luma.</span><span class="sxs-lookup"><span data-stu-id="06ebe-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="06ebe-138">**\_taxa de \_ proporção do estado de fluxo DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="06ebe-139">Taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="06ebe-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="06ebe-140">**Filtro de estado de fluxo de DXVAHD \_ \_ \_ \_ xxxx**</span><span class="sxs-lookup"><span data-stu-id="06ebe-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="06ebe-141">Configurações de filtro de imagem.</span><span class="sxs-lookup"><span data-stu-id="06ebe-141">Image filter settings.</span></span> <span data-ttu-id="06ebe-142">O driver pode dar suporte a brilho, contraste e outros filtros de imagem.</span><span class="sxs-lookup"><span data-stu-id="06ebe-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="06ebe-143">Os seguintes Estados de blit são definidos:</span><span class="sxs-lookup"><span data-stu-id="06ebe-143">The following blit states are defined:</span></span>



| <span data-ttu-id="06ebe-144">Estado blit</span><span class="sxs-lookup"><span data-stu-id="06ebe-144">Blit State</span></span>                                   | <span data-ttu-id="06ebe-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="06ebe-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="06ebe-146">**\_ \_ \_ target Rect de estado DXVAHD BLT \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="06ebe-147">Retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="06ebe-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="06ebe-148">**\_cor do \_ plano de fundo do estado DXVAHD BLT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="06ebe-149">Cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="06ebe-149">Background color.</span></span>                                                            |
| <span data-ttu-id="06ebe-150">**\_espaço de \_ cor de saída de estado DXVAHD BLT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="06ebe-151">Espaço de cores de saída.</span><span class="sxs-lookup"><span data-stu-id="06ebe-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="06ebe-152">**\_ \_ preenchimento alfa do estado DXVAHD BLT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="06ebe-153">Modo de preenchimento alfa.</span><span class="sxs-lookup"><span data-stu-id="06ebe-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="06ebe-154">**\_restrição de \_ estado de BLT DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="06ebe-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="06ebe-155">Restrição.</span><span class="sxs-lookup"><span data-stu-id="06ebe-155">Constriction.</span></span> <span data-ttu-id="06ebe-156">Esse estado controla se o dispositivo downsamples a saída.</span><span class="sxs-lookup"><span data-stu-id="06ebe-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="06ebe-157">Para definir um estado de fluxo, chame o método [**IDXVAHD \_ VideoProcessor:: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) .</span><span class="sxs-lookup"><span data-stu-id="06ebe-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="06ebe-158">Para definir um estado blit, chame o método [**IDXVAHD \_ VideoProcessor:: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) .</span><span class="sxs-lookup"><span data-stu-id="06ebe-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="06ebe-159">Em ambos os métodos, um valor de enumeração Especifica o estado a ser definido.</span><span class="sxs-lookup"><span data-stu-id="06ebe-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="06ebe-160">Os dados de estado são fornecidos usando uma estrutura de dados específica de estado, que o aplicativo converte para um tipo **void \*** .</span><span class="sxs-lookup"><span data-stu-id="06ebe-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="06ebe-161">O exemplo de código a seguir define o formato de entrada e o retângulo de destino para o fluxo 0 e define a cor do plano de fundo como preto.</span><span class="sxs-lookup"><span data-stu-id="06ebe-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="06ebe-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06ebe-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06ebe-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="06ebe-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



