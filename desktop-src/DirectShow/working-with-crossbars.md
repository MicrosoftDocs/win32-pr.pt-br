---
description: Trabalhando com Crossbars
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Trabalhando com Crossbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105792541"
---
# <a name="working-with-crossbars"></a><span data-ttu-id="80675-103">Trabalhando com Crossbars</span><span class="sxs-lookup"><span data-stu-id="80675-103">Working with Crossbars</span></span>

<span data-ttu-id="80675-104">Se um cartão de captura de vídeo tiver mais de uma entrada física ou der suporte a mais de um caminho de hardware para os dados, o grafo de filtro poderá conter o [filtro Crossbar de vídeo analógico](analog-video-crossbar-filter.md).</span><span class="sxs-lookup"><span data-stu-id="80675-104">If a video capture card has more than one physical input, or supports more than one hardware path for data, then the filter graph may contain the [Analog Video Crossbar Filter](analog-video-crossbar-filter.md).</span></span> <span data-ttu-id="80675-105">O construtor do grafo de captura adiciona automaticamente esse filtro quando necessário; Ele será upstream do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="80675-105">The Capture Graph Builder automatically adds this filter when needed; it will be upstream from the capture filter.</span></span> <span data-ttu-id="80675-106">Dependendo do hardware, o grafo de filtro pode conter mais de uma instância do filtro Crossbar.</span><span class="sxs-lookup"><span data-stu-id="80675-106">Depending on the hardware, the filter graph might contain more than one instance of the crossbar filter.</span></span>

<span data-ttu-id="80675-107">O filtro Crossbar expõe a interface [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , que você pode usar para rotear uma entrada específica para uma saída específica.</span><span class="sxs-lookup"><span data-stu-id="80675-107">The crossbar filter exposes the [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) interface, which you can use to route a particular input to a particular output.</span></span> <span data-ttu-id="80675-108">Por exemplo, uma placa de vídeo pode ter um conector coaxial e uma entrada de S-Video.</span><span class="sxs-lookup"><span data-stu-id="80675-108">For example, a video card might have a coaxial connector and an S-Video input.</span></span> <span data-ttu-id="80675-109">Eles seriam representados como Pins de entrada no filtro Crossbar.</span><span class="sxs-lookup"><span data-stu-id="80675-109">These would be represented as input pins on the crossbar filter.</span></span> <span data-ttu-id="80675-110">Para selecionar uma entrada, encaminhe o pino de entrada correspondente para o pino de saída do crossbar, usando o método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="80675-110">To select an input, route the corresponding input pin to the crossbar's output pin, using the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

<span data-ttu-id="80675-111">Para localizar filtros Crossbar no grafo, você pode usar o método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) para procurar filtros que dão suporte a **IAMCrossbar**.</span><span class="sxs-lookup"><span data-stu-id="80675-111">To locate crossbar filters in the graph, you can use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to search for filters that support **IAMCrossbar**.</span></span> <span data-ttu-id="80675-112">Por exemplo, o código a seguir procura dois Crossbars:</span><span class="sxs-lookup"><span data-stu-id="80675-112">For example, the following code searches for two crossbars:</span></span>


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



<span data-ttu-id="80675-113">Para obter uma abordagem mais generalizada, consulte a classe CCrossbar no [exemplo AMCAP](amcap-sample.md).</span><span class="sxs-lookup"><span data-stu-id="80675-113">For a more generalized approach, see the CCrossbar class in the [AmCap Sample](amcap-sample.md).</span></span>

<span data-ttu-id="80675-114">Depois de ter um ponteiro para a interface **IAMCrossbar** , você pode obter informações sobre o filtro crossbar, incluindo o tipo físico de cada PIN e a matriz da qual os Pins de entrada podem ser roteados para os Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="80675-114">Once you have a pointer to the **IAMCrossbar** interface, you can get information about the crossbar filter, including the physical type of each pin, and the matrix of which input pins can be routed to which output pins.</span></span>

-   <span data-ttu-id="80675-115">Para determinar o tipo de conector físico ao qual um PIN corresponde, chame o método [**IAMCrossbar:: get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) .</span><span class="sxs-lookup"><span data-stu-id="80675-115">To determine the type of physical connector to which a pin corresponds, call the [**IAMCrossbar::get\_CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) method.</span></span> <span data-ttu-id="80675-116">O método retorna um membro da enumeração [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) .</span><span class="sxs-lookup"><span data-stu-id="80675-116">The method returns a member of the [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) enumeration.</span></span> <span data-ttu-id="80675-117">Por exemplo, um PIN de S-Video retorna o valor PhysConn \_ vídeo \_ SVIDEO.</span><span class="sxs-lookup"><span data-stu-id="80675-117">For example, an S-Video pin returns the value PhysConn\_Video\_SVideo.</span></span>

    <span data-ttu-id="80675-118">O método **Get \_ CrossbarInfo** também indica se dois Pins estão relacionados entre si.</span><span class="sxs-lookup"><span data-stu-id="80675-118">The **get\_CrossbarInfo** method also indicates whether two pins are related to each other.</span></span> <span data-ttu-id="80675-119">Por exemplo, um pino de sintonizador de vídeo pode estar relacionado a um pino de sintonizador de áudio.</span><span class="sxs-lookup"><span data-stu-id="80675-119">For example, a video tuner pin might be related to an audio tuner pin.</span></span> <span data-ttu-id="80675-120">Os Pins relacionados têm a mesma direção do PIN e, normalmente, fazem parte da mesma tomada ou conector físico no cartão.</span><span class="sxs-lookup"><span data-stu-id="80675-120">Related pins have the same pin direction, and are typically part of the same physical jack or connector on the card.</span></span>

-   <span data-ttu-id="80675-121">Para determinar se você pode rotear um PIN de entrada para um PIN de saída específico, chame o método [**IAMCrossbar:: canroute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .</span><span class="sxs-lookup"><span data-stu-id="80675-121">To determine whether you can route an input pin to a particular output pin, call the [**IAMCrossbar::CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) method.</span></span>
-   <span data-ttu-id="80675-122">Para determinar o roteamento atual entre os Pins, chame o método [**IAMCrossbar:: get \_ isrouteto**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .</span><span class="sxs-lookup"><span data-stu-id="80675-122">To determine the current routing between pins, call the [**IAMCrossbar::get\_IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) method.</span></span>

<span data-ttu-id="80675-123">Todos os métodos anteriores especificam Pins por número de índice, com Pins de saída e Pins de entrada, ambos indexados de zero.</span><span class="sxs-lookup"><span data-stu-id="80675-123">The previous methods all specify pins by index number, with output pins and input pins both indexed from zero.</span></span> <span data-ttu-id="80675-124">Chame o método **IAMCrossbar:: get \_ PinCounts** para localizar o número de Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="80675-124">Call the **IAMCrossbar::get\_PinCounts** method to find the number of pins on the filter.</span></span>

<span data-ttu-id="80675-125">Por exemplo, o código a seguir exibe informações sobre um filtro Crossbar na janela do console:</span><span class="sxs-lookup"><span data-stu-id="80675-125">For example, the following code displays information about a crossbar filter to the console window:</span></span>


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



<span data-ttu-id="80675-126">Para um cartão hipotético, essa função pode produzir a seguinte saída:</span><span class="sxs-lookup"><span data-stu-id="80675-126">For a hypothetical card, this function might produce the following output:</span></span>


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



<span data-ttu-id="80675-127">No lado da saída, o S-Video e o sintonizador de vídeo estão relacionados ao decodificador de áudio.</span><span class="sxs-lookup"><span data-stu-id="80675-127">On the output side, the S-Video and the video tuner are both related to the audio decoder.</span></span> <span data-ttu-id="80675-128">No lado da entrada, o sintonizador de vídeo está relacionado ao sintonizador de áudio e o S-Video está relacionado à linha de áudio no.</span><span class="sxs-lookup"><span data-stu-id="80675-128">On the input side, the video tuner is related to the audio tuner, and the S-Video is related to the audio line in.</span></span> <span data-ttu-id="80675-129">A entrada S-Video é roteada para a saída S-Video; e a entrada do sintonizador de vídeo é roteada para a saída do sintonizador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="80675-129">The S-Video input is routed to the S-Video output; and the video tuner input is routed to the video tuner output.</span></span> <span data-ttu-id="80675-130">No momento, nada é roteado para o decodificador de áudio, mas a linha de áudio no ou o sintonizador de áudio pode ser roteado para ele.</span><span class="sxs-lookup"><span data-stu-id="80675-130">Currently nothing is routed to the audio decoder, but either the audio line in or the audio tuner could be routed to it.</span></span>

<span data-ttu-id="80675-131">Você pode alterar o roteamento existente chamando o método [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .</span><span class="sxs-lookup"><span data-stu-id="80675-131">You can change the existing routing by calling the [**IAMCrossbar::Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) method.</span></span>

 

 



