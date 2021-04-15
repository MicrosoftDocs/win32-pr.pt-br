---
description: Exibindo legendas ocultas
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Exibindo legendas ocultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562614"
---
# <a name="viewing-closed-captions"></a><span data-ttu-id="a3141-103">Exibindo legendas ocultas</span><span class="sxs-lookup"><span data-stu-id="a3141-103">Viewing Closed Captions</span></span>

<span data-ttu-id="a3141-104">Para dar suporte a legendas codificadas na televisão analógica, o filtro de captura expõe um PIN que fornece dados de VBI ou de legenda oculta.</span><span class="sxs-lookup"><span data-stu-id="a3141-104">To support closed captions in analog television, the capture filter exposes a pin that delivers either VBI or closed caption data.</span></span> <span data-ttu-id="a3141-105">O PIN terá uma das seguintes categorias de PIN:</span><span class="sxs-lookup"><span data-stu-id="a3141-105">The pin will have one of the following pin categories:</span></span>

-   <span data-ttu-id="a3141-106">VBI PIN (fixar \_ categoria \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="a3141-106">VBI pin (PIN\_CATEGORY\_VBI).</span></span> <span data-ttu-id="a3141-107">Fornece um fluxo de exemplos de formato de onda VBI.</span><span class="sxs-lookup"><span data-stu-id="a3141-107">Delivers a stream of VBI waveform samples.</span></span> <span data-ttu-id="a3141-108">Eles são passados para um filtro de decodificador que extrai os dados de legenda codificada.</span><span class="sxs-lookup"><span data-stu-id="a3141-108">These are passed to a decoder filter that extracts the closed captioning data.</span></span>
-   <span data-ttu-id="a3141-109">PIN CC (fixar \_ categoria \_ CC).</span><span class="sxs-lookup"><span data-stu-id="a3141-109">CC pin (PIN\_CATEGORY\_CC).</span></span> <span data-ttu-id="a3141-110">Entrega pares de bytes de legenda fechada, extraídos dos dados de linha-21.</span><span class="sxs-lookup"><span data-stu-id="a3141-110">Delivers closed-caption byte pairs, extracted from the line-21 data.</span></span>
-   <span data-ttu-id="a3141-111">PIN do CC de fatia de hardware ( \_ captura de vídeo CC do PINNAME \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="a3141-111">Hardware slicing CC pin (PINNAME\_VIDEO\_CC\_CAPTURE).</span></span>

<span data-ttu-id="a3141-112">Para visualizar legendas ocultas, chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com a categoria VBI PIN e, se isso falhar, chame-a novamente com a categoria CC.</span><span class="sxs-lookup"><span data-stu-id="a3141-112">To preview closed captions, call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the VBI pin category, and if that fails, call it again with the CC category.</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



<span data-ttu-id="a3141-113">O diagrama a seguir mostra um grafo de filtro típico para exibir legendas ocultas.</span><span class="sxs-lookup"><span data-stu-id="a3141-113">The following diagram shows a typical filter graph for displaying closed captions.</span></span>

![Grafo de visualização de legendagem oculta](images/vidcap08.png)

<span data-ttu-id="a3141-115">Este grafo usa os seguintes filtros para exibição de legenda oculta:</span><span class="sxs-lookup"><span data-stu-id="a3141-115">This graph uses the following filters for closed caption display:</span></span>

-   <span data-ttu-id="a3141-116">[Conversor de t/coletor de alto-para-coletor](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="a3141-116">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="a3141-117">Aceita as informações de VBI do filtro de captura e divide-as em fluxos separados para cada um dos serviços de dados presentes no sinal.</span><span class="sxs-lookup"><span data-stu-id="a3141-117">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span> <span data-ttu-id="a3141-118">A Microsoft fornece codecs VBI para legendas codificadas, NABTS e teletextos padrão mundiais (WST).</span><span class="sxs-lookup"><span data-stu-id="a3141-118">Microsoft provides VBI codecs for Closed Caption, NABTS, and World Standard Teletext (WST).</span></span>
-   <span data-ttu-id="a3141-119">[Decodificador CC](cc-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a3141-119">[CC Decoder](cc-decoder-filter.md).</span></span> <span data-ttu-id="a3141-120">Decodifica os dados do CC das amostras de onda de VBI amostradas fornecidas pelo filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="a3141-120">Decodes CC data from the sampled VBI waveforms provided by the capture filter.</span></span>
-   <span data-ttu-id="a3141-121">[Decodificador de linha 21](line-21-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a3141-121">[Line 21 Decoder](line-21-decoder-filter.md).</span></span> <span data-ttu-id="a3141-122">Traduz os pares de bytes de CC e desenha o texto da legenda em bitmaps.</span><span class="sxs-lookup"><span data-stu-id="a3141-122">Translates the CC byte pairs and draws the caption text onto bitmaps.</span></span> <span data-ttu-id="a3141-123">O filtro downstream (nesse caso, o mixer de sobreposição) sobrepõe os bitmaps no vídeo.</span><span class="sxs-lookup"><span data-stu-id="a3141-123">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="a3141-124">O método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) do construtor do grafo de captura adiciona esses filtros automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a3141-124">The Capture Graph Builder's [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds these filters automatically.</span></span> <span data-ttu-id="a3141-125">Se o filtro de captura tiver um PIN de CC em vez de um PIN de VBI, o PIN de CC será conectado diretamente ao filtro de decodificador de linha 21.</span><span class="sxs-lookup"><span data-stu-id="a3141-125">If the capture filter has a CC pin instead of a VBI pin, the CC pin is connected directly to the Line 21 Decoder filter.</span></span>

> [!Note]  
> <span data-ttu-id="a3141-126">Se você estiver usando o filtro de processador de mixagem de vídeo (VMR) para renderização, use o filtro de decodificador de linha 21 2.</span><span class="sxs-lookup"><span data-stu-id="a3141-126">If you are using the Video Mixing Renderer (VMR) filter for rendering, use the Line 21 Decoder Filter 2.</span></span> <span data-ttu-id="a3141-127">Esse filtro tem a mesma funcionalidade que o decodificador de linha 21, mas o CLSID é CLSID \_ Line21Decoder2.</span><span class="sxs-lookup"><span data-stu-id="a3141-127">This filter has the same functionality as the Line 21 Decoder, but the CLSID is CLSID\_Line21Decoder2.</span></span>

 

> [!Note]  
> <span data-ttu-id="a3141-128">O filtro de decodificador de CC foi removido do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a3141-128">The CC Decoder filter was removed in Windows Vista.</span></span> <span data-ttu-id="a3141-129">Os novos aplicativos devem usar o filtro VBICodec, documentado na documentação das tecnologias de TV da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3141-129">New applications should use the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

 

<span data-ttu-id="a3141-130">Se o dispositivo de captura usar uma porta de vídeo, o filtro de captura poderá ter uma porta de vídeo VBI PIN (PIN \_ Category \_ VIDEOPORT \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="a3141-130">If the capture device uses a video port, the capture filter might have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="a3141-131">Esse PIN deve ser conectado ao filtro de [alocador de superfície VBI](vbi-surface-allocator.md) , que aloca superfícies para manter os dados VBI capturados.</span><span class="sxs-lookup"><span data-stu-id="a3141-131">This pin must be connected to the [VBI Surface Allocator](vbi-surface-allocator.md) filter, which allocates surfaces to hold the captured VBI data.</span></span> <span data-ttu-id="a3141-132">O método [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) adicionará esse filtro se for necessário.</span><span class="sxs-lookup"><span data-stu-id="a3141-132">The [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds this filter if it is required.</span></span> <span data-ttu-id="a3141-133">O diagrama a seguir mostra um gráfico de filtro com o alocador de superfície VBI.</span><span class="sxs-lookup"><span data-stu-id="a3141-133">The following diagram shows a filter graph with the VBI Surface Allocator.</span></span>

![Grafo de visualização de legenda codificada com alocador de superfície VBI](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a><span data-ttu-id="a3141-135">Habilitando e desabilitando as legendas</span><span class="sxs-lookup"><span data-stu-id="a3141-135">Enabling and Disabling the Captions</span></span>

<span data-ttu-id="a3141-136">Para controlar a exibição de legendas, use a interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) no filtro linha 21 de decodificador.</span><span class="sxs-lookup"><span data-stu-id="a3141-136">To control the captioning display, use the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface on the Line 21 Decoder filter.</span></span> <span data-ttu-id="a3141-137">Por exemplo, você pode desativar a exibição de legendas usando o método [**IAMLine21Decoder:: Setservicestate**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a3141-137">For example, you can turn off the captioning display using the [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) method, as follows:</span></span>


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



<span data-ttu-id="a3141-138">Este exemplo usa o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para localizar a interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) .</span><span class="sxs-lookup"><span data-stu-id="a3141-138">This example uses the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface.</span></span> <span data-ttu-id="a3141-139">O primeiro parâmetro para **FindInterface** é **&parecer \_ \_ somente DOWNSTREAM**, que especifica a pesquisa downstream do filtro de captura (*pcap*).</span><span class="sxs-lookup"><span data-stu-id="a3141-139">The first parameter to **FindInterface** is **&LOOK\_DOWNSTREAM\_ONLY**, which specifies to search downstream from the capture filter (*pCap*).</span></span>

### <a name="capturing-closed-caption-bitmaps"></a><span data-ttu-id="a3141-140">Capturando bitmaps de legenda oculta</span><span class="sxs-lookup"><span data-stu-id="a3141-140">Capturing Closed Caption Bitmaps</span></span>

<span data-ttu-id="a3141-141">Você pode capturar os bitmaps de legenda em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="a3141-141">You can capture the caption bitmaps into a file.</span></span> <span data-ttu-id="a3141-142">Para fazer isso, adicione a seção de gravação de arquivo do gráfico de filtro, conforme descrito em [capturando vídeo em um arquivo](capturing-video-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="a3141-142">To do so, add the file-writing section of the filter graph, as described in [Capturing Video to a File](capturing-video-to-a-file.md).</span></span> <span data-ttu-id="a3141-143">Em seguida, processe o PIN CC ou VBI para o filtro Mux:</span><span class="sxs-lookup"><span data-stu-id="a3141-143">Then render the CC or VBI pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



<span data-ttu-id="a3141-144">Se você também estiver capturando o vídeo, isso criará um arquivo com dois fluxos de vídeo separados.</span><span class="sxs-lookup"><span data-stu-id="a3141-144">If you are also capturing the video, this will create a file with two separate video streams.</span></span> <span data-ttu-id="a3141-145">Ele não capturará vídeo com legendas sobrepostas sobre a imagem.</span><span class="sxs-lookup"><span data-stu-id="a3141-145">It will not capture video with captions overlaid on top of the picture.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3141-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3141-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3141-147">Legendas e teletextos codificados</span><span class="sxs-lookup"><span data-stu-id="a3141-147">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



