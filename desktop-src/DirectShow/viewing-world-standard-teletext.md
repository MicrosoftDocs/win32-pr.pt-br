---
description: Exibindo teletexto do mundo Standard
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Exibindo teletexto do mundo Standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b0885c08403de9578a8dee1eca6e000408ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296524"
---
# <a name="viewing-world-standard-teletext"></a><span data-ttu-id="2ef41-103">Exibindo teletexto do mundo Standard</span><span class="sxs-lookup"><span data-stu-id="2ef41-103">Viewing World Standard Teletext</span></span>

> [!Note]  
> <span data-ttu-id="2ef41-104">Essa funcionalidade foi removida do Windows Vista e de sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="2ef41-104">This functionality has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="2ef41-105">Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2ef41-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="2ef41-106">O teletexto padrão mundial (WST) é codificado no intervalo vertical em branco (VBI) do sinal de televisão analógica.</span><span class="sxs-lookup"><span data-stu-id="2ef41-106">World Standard Teletext (WST) is encoded in the vertical blanking interval (VBI) of the analog television signal.</span></span> <span data-ttu-id="2ef41-107">O grafo de filtro para visualização de teletexto é semelhante ao gráfico usado para exibir legendas ocultas.</span><span class="sxs-lookup"><span data-stu-id="2ef41-107">The filter graph for previewing teletext is similar to the graph used to view closed captions.</span></span> <span data-ttu-id="2ef41-108">O diagrama a seguir ilustra esse grafo.</span><span class="sxs-lookup"><span data-stu-id="2ef41-108">The following diagram illustrates this graph.</span></span>

![Grafo de visualização de WST](images/vidcap10.png)

<span data-ttu-id="2ef41-110">Este grafo usa os seguintes filtros para exibição de WST:</span><span class="sxs-lookup"><span data-stu-id="2ef41-110">This graph uses the following filters for WST display:</span></span>

-   <span data-ttu-id="2ef41-111">[Conversor de t/coletor de alto-para-coletor](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="2ef41-111">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="2ef41-112">Aceita as informações de VBI do filtro de captura e divide-as em fluxos separados para cada um dos serviços de dados presentes no sinal.</span><span class="sxs-lookup"><span data-stu-id="2ef41-112">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span>
-   <span data-ttu-id="2ef41-113">[Codec de WST](wst-codec-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2ef41-113">[WST Codec](wst-codec-filter.md).</span></span> <span data-ttu-id="2ef41-114">Decodifica os dados do TELETEXT dos exemplos de VBI.</span><span class="sxs-lookup"><span data-stu-id="2ef41-114">Decodes the Teletext data from the VBI samples.</span></span>
-   <span data-ttu-id="2ef41-115">[Decodificador de WST](wst-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2ef41-115">[WST Decoder](wst-decoder-filter.md).</span></span> <span data-ttu-id="2ef41-116">Traduz dados do TELETEXT e desenha o texto em bitmaps.</span><span class="sxs-lookup"><span data-stu-id="2ef41-116">Translates teletext data and draws the text onto bitmaps.</span></span> <span data-ttu-id="2ef41-117">O filtro downstream (nesse caso, o mixer de sobreposição) sobrepõe os bitmaps no vídeo.</span><span class="sxs-lookup"><span data-stu-id="2ef41-117">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="2ef41-118">O método **RenderStream** do construtor do grafo de captura não dá suporte a filtros de WST diretamente, portanto, seu aplicativo deve fazer algum trabalho extra.</span><span class="sxs-lookup"><span data-stu-id="2ef41-118">The Capture Graph Builder's **RenderStream** method does not support the WST filters directly, so your application must do some extra work.</span></span>

1.  <span data-ttu-id="2ef41-119">Adicione o filtro do mixer de sobreposição ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="2ef41-119">Add the Overlay Mixer filter to the filter graph.</span></span> <span data-ttu-id="2ef41-120">O código a seguir usa a função AddFilterByCLSID descrita em [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="2ef41-120">The following code uses the AddFilterByCLSID function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span> <span data-ttu-id="2ef41-121">(AddFilterByCLSID não é uma API do DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="2ef41-121">(AddFilterByCLSID is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  <span data-ttu-id="2ef41-122">Conecte o pino de visualização ao filtro de processador de vídeo por meio do mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="2ef41-122">Connect the preview pin to the Video Renderer filter through the Overlay Mixer.</span></span> <span data-ttu-id="2ef41-123">Você pode usar o método **RenderStream** , da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2ef41-123">You can use the **RenderStream** method, as follows:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  <span data-ttu-id="2ef41-124">Adicione o filtro de conversor de Altova/coletor para coletor ao grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="2ef41-124">Add the Tee/Sink-to-Sink Converter filter to the filter graph.</span></span> <span data-ttu-id="2ef41-125">O código a seguir usa a função CreateKernelFilter descrita em [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2ef41-125">The following code uses the CreateKernelFilter function described in [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span> <span data-ttu-id="2ef41-126">(CreateKernelFilter não é uma API do DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="2ef41-126">(CreateKernelFilter is not a DirectShow API.)</span></span>
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  <span data-ttu-id="2ef41-127">Adicione o filtro de codec de WST ao gráfico de filtro:</span><span class="sxs-lookup"><span data-stu-id="2ef41-127">Add the WST Codec filter to the filter graph:</span></span>
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  <span data-ttu-id="2ef41-128">Chame **RenderStream** para conectar o PIN do VBI do filtro de captura ao conversor de alto/coletor-para-coletor e o conversor de alto/coletor para coletor para o filtro de codec de WST:</span><span class="sxs-lookup"><span data-stu-id="2ef41-128">Call **RenderStream** to connect the capture filter's VBI pin to the Tee/Sink-to-Sink Converter, and the Tee/Sink-to-Sink Converter to the WST Codec filter:</span></span>
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  <span data-ttu-id="2ef41-129">Chame **RenderStream** novamente para conectar o filtro de codec de WST ao mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="2ef41-129">Call **RenderStream** again to connect the WST Codec filter to the Overlay Mixer.</span></span> <span data-ttu-id="2ef41-130">O filtro de decodificador de WST é automaticamente colocado no grafo.</span><span class="sxs-lookup"><span data-stu-id="2ef41-130">The WST Decoder filter is automatically brought into the graph.</span></span>
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  <span data-ttu-id="2ef41-131">Lembre-se de liberar todas as interfaces de filtro.</span><span class="sxs-lookup"><span data-stu-id="2ef41-131">Remember to release all of the filter interfaces.</span></span>
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> <span data-ttu-id="2ef41-132">Atualmente, o filtro de decodificador de WST não oferece suporte a conexões com o filtro de processador de mixagem de vídeo (VMR).</span><span class="sxs-lookup"><span data-stu-id="2ef41-132">Currently, the WST Decoder filter does not support connections to the Video Mixing Renderer (VMR) filter.</span></span> <span data-ttu-id="2ef41-133">Portanto, você deve usar o filtro de renderização de vídeo herdado para exibir o teletexto.</span><span class="sxs-lookup"><span data-stu-id="2ef41-133">Therefore, you must use the legacy Video Renderer filter to view teletext.</span></span>

 

<span data-ttu-id="2ef41-134">Se o filtro de captura tiver uma porta de vídeo VBI PIN (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI), conecte-o ao filtro de [alocador de superfície de VBI](vbi-surface-allocator.md) .</span><span class="sxs-lookup"><span data-stu-id="2ef41-134">If the capture filter has a video port VBI pin (PIN\_CATEGPORY\_VIDEOPORT\_VBI), connect it to the [VBI Surface Allocator](vbi-surface-allocator.md) filter.</span></span> <span data-ttu-id="2ef41-135">Caso contrário, o grafo não será executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="2ef41-135">The graph will not run correctly otherwise.</span></span> <span data-ttu-id="2ef41-136">O exemplo de código a seguir usa a função AddFilterByCLSID, descrita em [Adicionar um filtro por CLSID](add-a-filter-by-clsid.md), e a função FindPinByCategory, descrita em [trabalhando com categorias de PIN](working-with-pin-categories.md).</span><span class="sxs-lookup"><span data-stu-id="2ef41-136">The following code example uses the AddFilterByCLSID function, described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the FindPinByCategory function, described in [Working with Pin Categories](working-with-pin-categories.md).</span></span> <span data-ttu-id="2ef41-137">(Nenhuma função é uma API do DirectShow.)</span><span class="sxs-lookup"><span data-stu-id="2ef41-137">(Neither function is a DirectShow API.)</span></span>


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="2ef41-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2ef41-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ef41-139">Legendas e teletextos codificados</span><span class="sxs-lookup"><span data-stu-id="2ef41-139">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



