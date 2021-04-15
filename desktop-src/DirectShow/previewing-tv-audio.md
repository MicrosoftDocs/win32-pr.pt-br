---
description: Visualizando áudio de TV
ms.assetid: 25da8bcc-51c1-49f0-b4b5-885ff4f254d8
title: Visualizando áudio de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cc63583c946d47ed744eacd51f0939ec852d53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456565"
---
# <a name="previewing-tv-audio"></a><span data-ttu-id="c73d2-103">Visualizando áudio de TV</span><span class="sxs-lookup"><span data-stu-id="c73d2-103">Previewing TV Audio</span></span>

<span data-ttu-id="c73d2-104">Para visualizar o áudio de TV, direcione o PIN do decodificador de áudio no filtro Crossbar para o pino do sintonizador de áudio.</span><span class="sxs-lookup"><span data-stu-id="c73d2-104">To preview TV audio, route the Audio Decoder pin on the crossbar filter to the Audio Tuner pin.</span></span> <span data-ttu-id="c73d2-105">Para ativar mudo do áudio, encaminhe o PIN do decodificador de áudio para-1, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c73d2-105">To mute the audio, route the Audio Decoder pin to -1, as shown in the following diagram.</span></span> <span data-ttu-id="c73d2-106">(Os filtros Crossbar são descritos em [trabalhando com Crossbars](working-with-crossbars.md).)</span><span class="sxs-lookup"><span data-stu-id="c73d2-106">(Crossbar filters are described in [Working with Crossbars](working-with-crossbars.md).)</span></span>

![Roteando o PIN do decodificador de áudio](images/vidcap07.png)

<span data-ttu-id="c73d2-108">A abordagem básica é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c73d2-108">The basic approach is as follows:</span></span>

1.  <span data-ttu-id="c73d2-109">Use o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para localizar o filtro Crossbar.</span><span class="sxs-lookup"><span data-stu-id="c73d2-109">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the crossbar filter.</span></span>
2.  <span data-ttu-id="c73d2-110">Use o método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) para enumerar os Pins de entrada e saída do filtro Crossbar.</span><span class="sxs-lookup"><span data-stu-id="c73d2-110">Use the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method to enumerate the crossbar filter's input and output pins.</span></span> <span data-ttu-id="c73d2-111">Procure um PIN de saída de decodificador de áudio e um pino de entrada do sintonizador de áudio.</span><span class="sxs-lookup"><span data-stu-id="c73d2-111">Search for an audio decoder output pin and an audio tuner input pin.</span></span>
3.  <span data-ttu-id="c73d2-112">Se você encontrar os Pins corretos, chame [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) para rotear os Pins.</span><span class="sxs-lookup"><span data-stu-id="c73d2-112">If you find the correct pins, call [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) to route the pins.</span></span> <span data-ttu-id="c73d2-113">Caso contrário, observe upstream para outro Crossbar e repita o processo.</span><span class="sxs-lookup"><span data-stu-id="c73d2-113">If not, look upstream for another crossbar and repeat the process.</span></span>
4.  <span data-ttu-id="c73d2-114">Para ativar mudo do áudio, encaminhe o PIN do decodificador de áudio para-1.</span><span class="sxs-lookup"><span data-stu-id="c73d2-114">To mute the audio, route the audio decoder pin to -1.</span></span>

<span data-ttu-id="c73d2-115">A maioria dos sintonizadores de TV usa um único filtro crossbar, mas alguns usam dois filtros Crossbar.</span><span class="sxs-lookup"><span data-stu-id="c73d2-115">Most TV tuners use a single crossbar filter, but some use two crossbar filters.</span></span> <span data-ttu-id="c73d2-116">Portanto, talvez seja necessário pesquisar por um segundo Crossbar se o primeiro falhar.</span><span class="sxs-lookup"><span data-stu-id="c73d2-116">Therefore, you might have to search for a second crossbar if the first one fails.</span></span>

> [!Note]  
> <span data-ttu-id="c73d2-117">Ao contrário do que você pode esperar, nenhum filtro de captura de áudio ou processador de áudio é necessário para visualizar o áudio, porque há uma conexão física entre a placa de sintonizador e a placa de som.</span><span class="sxs-lookup"><span data-stu-id="c73d2-117">Contrary to what you might expect, no audio capture filter or audio renderer is required to preview the audio, because there is a physical connection between the tuner card and the sound card.</span></span>

 

<span data-ttu-id="c73d2-118">O código a seguir mostra essas etapas mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="c73d2-118">The following code shows these steps in more detail.</span></span> <span data-ttu-id="c73d2-119">Primeiro, aqui está uma função auxiliar que pesquisa um filtro Crossbar para um tipo de PIN especificado:</span><span class="sxs-lookup"><span data-stu-id="c73d2-119">First, here is a helper function that searches a crossbar filter for a specified pin type:</span></span>


```C++
HRESULT FindCrossbarPin(
    IAMCrossbar *pXBar,                 // Pointer to the crossbar.
    PhysicalConnectorType PhysicalType, // Pin type to match.
    PIN_DIRECTION Dir,                  // Pin direction.
    long *pIndex)       // Receives the index of the pin, if found.
{
    BOOL bInput = (Dir == PINDIR_INPUT ? TRUE : FALSE);

    // Find out how many pins the crossbar has.
    long cOut, cIn;
    HRESULT hr = pXBar->get_PinCounts(&cOut, &cIn);
    if (FAILED(hr)) return hr;
    // Enumerate pins and look for a matching pin.
    long count = (bInput ? cIn : cOut);
    for (long i = 0; i < count; i++)
    {
        long iRelated = 0;
        long ThisPhysicalType = 0;
        hr = pXBar->get_CrossbarPinInfo(bInput, i, &iRelated,
            &ThisPhysicalType);
        if (SUCCEEDED(hr) && ThisPhysicalType == PhysicalType)
        {
            // Found a match, return the index.
            *pIndex = i;
            return S_OK;
        }
    }
    // Did not find a matching pin.
    return E_FAIL;
}
```



<span data-ttu-id="c73d2-120">A próxima função tenta ativar ou desativar o áudio, dependendo do valor do parâmetro *bActivate* .</span><span class="sxs-lookup"><span data-stu-id="c73d2-120">The next function attempts to activate or mute the audio, depending on the value of the *bActivate* parameter.</span></span> <span data-ttu-id="c73d2-121">Ele pesquisa o filtro Crossbar especificado para os Pins necessários.</span><span class="sxs-lookup"><span data-stu-id="c73d2-121">It searches the specified crossbar filter for the required pins.</span></span> <span data-ttu-id="c73d2-122">Se ele não conseguir encontrá-los, ele retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="c73d2-122">If it cannot find them, it returns an error code.</span></span>


```C++
HRESULT ConnectAudio(IAMCrossbar *pXBar, BOOL bActivate)
{
    // Look for the Audio Decoder output pin.
    long i = 0;
    HRESULT hr = FindCrossbarPin(pXBar, PhysConn_Audio_AudioDecoder,
        PINDIR_OUTPUT, &i);
    if (SUCCEEDED(hr))
    {
        if (bActivate)  // Activate the audio. 
        {
            // Look for the Audio Tuner input pin.
            long j = 0;
            hr = FindCrossbarPin(pXBar, PhysConn_Audio_Tuner, 
                PINDIR_INPUT, &j);
            if (SUCCEEDED(hr))
            {
                return pXBar->Route(i, j);
            }
        }
        else  // Mute the audio
        {
            return pXBar->Route(i, -1);
        }
    }
    return E_FAIL;
}
```



<span data-ttu-id="c73d2-123">A próxima função pesquisa o grafo de filtro em busca de um filtro Crossbar.</span><span class="sxs-lookup"><span data-stu-id="c73d2-123">The next function searches the filter graph for a crossbar filter.</span></span> <span data-ttu-id="c73d2-124">Se encontrar uma, ele tentará ativar ou desativar o áudio (usando a função anterior).</span><span class="sxs-lookup"><span data-stu-id="c73d2-124">If it finds one, it attempts to activate or mute the audio (using the previous function).</span></span> <span data-ttu-id="c73d2-125">Se essa operação falhar, o método pesquisará upstream para um segundo Crossbar e tentará novamente.</span><span class="sxs-lookup"><span data-stu-id="c73d2-125">If that operation fails, the method searches upstream for a second crossbar and tries again.</span></span> <span data-ttu-id="c73d2-126">Para obter uma abordagem mais generalizada para gerenciar vários filtros Crossbar em um grafo, consulte a classe CCrossbar no aplicativo de exemplo AmCap.</span><span class="sxs-lookup"><span data-stu-id="c73d2-126">For a more generalized approach to managing multiple crossbar filters in a graph, see the CCrossbar class in the AmCap sample application.</span></span>


```C++
HRESULT ActivateAudio(ICaptureGraphBuilder2 *pBuild, IBaseFilter *pSrc,
  BOOL bActivate)
{
    // Search upstream for a crossbar.
    IAMCrossbar *pXBar1 = NULL;
    HRESULT hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
    if (SUCCEEDED(hr)) 
    {
        hr = ConnectAudio(pXBar1, bActivate);
        if (FAILED(hr))
        {
            // Look for another crossbar.
            IBaseFilter *pF = NULL;
            hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pF);
            if (SUCCEEDED(hr)) 
            {
                // Search upstream for another one.
                IAMCrossbar *pXBar2 = NULL;
                hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pF,
                    IID_IAMCrossbar, (void**)&pXBar2);
                pF->Release();
                if (SUCCEEDED(hr))
                {
                    hr = ConnectAudio(pXBar2, bActivate);
                    pXBar2->Release();
                }
            }
        }
        pXBar1->Release();
    }
    return hr;
}
```



<span data-ttu-id="c73d2-127">O código a seguir mostra como chamar essas funções:</span><span class="sxs-lookup"><span data-stu-id="c73d2-127">The following code shows how to call these functions:</span></span>


```C++
// Build the analog TV graph (not shown).
// Activate the audio.
hr = ActivateAudio(pBuild, pCap, TRUE);
// Later, mute the audio.
hr = ActivateAudio(pBuild, pCap, FALSE);
```



<span data-ttu-id="c73d2-128">Observe que essas funções de exemplo repetem muitas das mesmas chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="c73d2-128">Note that these example functions repeat many of the same function calls.</span></span> <span data-ttu-id="c73d2-129">Por exemplo, eles enumeram os Pins Crossbar a cada vez.</span><span class="sxs-lookup"><span data-stu-id="c73d2-129">For example, they enumerate the crossbar pins each time.</span></span> <span data-ttu-id="c73d2-130">Em um aplicativo real, você pode armazenar em cache algumas dessas informações.</span><span class="sxs-lookup"><span data-stu-id="c73d2-130">In a real application, you might cache some of this information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c73d2-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c73d2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73d2-132">Áudio de televisão analógica</span><span class="sxs-lookup"><span data-stu-id="c73d2-132">Analog Television Audio</span></span>](analog-television-audio.md)
</dt> <dt>

[<span data-ttu-id="c73d2-133">Trabalhando com Crossbars</span><span class="sxs-lookup"><span data-stu-id="c73d2-133">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



