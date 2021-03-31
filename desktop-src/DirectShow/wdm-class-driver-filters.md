---
description: Filtros de driver de classe WDM
ms.assetid: 864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741
title: Filtros de driver de classe WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338e4ec4d2aaa58bdac737b58571497cad708876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827527"
---
# <a name="wdm-class-driver-filters"></a><span data-ttu-id="0e9d3-103">Filtros de driver de classe WDM</span><span class="sxs-lookup"><span data-stu-id="0e9d3-103">WDM Class Driver Filters</span></span>

<span data-ttu-id="0e9d3-104">Se um dispositivo de captura usar um driver de Windows Driver Model (WDM), o grafo poderá exigir certos filtros upstream do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-104">If a capture device uses a Windows Driver Model (WDM) driver, the graph might require certain filters upstream from the capture filter.</span></span> <span data-ttu-id="0e9d3-105">Esses filtros são chamados de filtros de driver de classe de fluxo ou filtros WDM.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-105">These filters are called stream-class driver filters or WDM filters.</span></span> <span data-ttu-id="0e9d3-106">Eles dão suporte a funcionalidades adicionais fornecidas pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-106">They support additional functionality provided by the hardware.</span></span> <span data-ttu-id="0e9d3-107">Por exemplo, um cartão sintonizador de TV tem funções para definir o canal.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-107">For example, a TV tuner card has functions for setting the channel.</span></span> <span data-ttu-id="0e9d3-108">O filtro correspondente é o filtro de [sintonizador de TV](tv-tuner-filter.md) , que expõe a interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) .</span><span class="sxs-lookup"><span data-stu-id="0e9d3-108">The corresponding filter is the [TV Tuner](tv-tuner-filter.md) filter, which exposes the [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) interface.</span></span> <span data-ttu-id="0e9d3-109">Para disponibilizar essa funcionalidade para o aplicativo, você deve conectar o filtro de sintonizador de TV ao filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-109">To make this functionality available to the application, you must connect the TV Tuner filter to the capture filter.</span></span>

<span data-ttu-id="0e9d3-110">A interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) fornece a maneira mais fácil de adicionar filtros WDM ao grafo.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-110">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface provides the easiest way to add WDM filters to the graph.</span></span> <span data-ttu-id="0e9d3-111">Em algum momento, ao criar o grafo, chame [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) ou [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="0e9d3-111">At some point while building the graph, call [**FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) or [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="0e9d3-112">Qualquer um desses métodos localizará automaticamente os filtros WDM necessários e os conectará ao filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-112">Either one of these methods will automatically locate the necessary WDM filters and connect them to the capture filter.</span></span> <span data-ttu-id="0e9d3-113">O restante desta seção descreve como adicionar filtros WDM manualmente.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-113">The rest of this section describes how to add WDM filters manually.</span></span> <span data-ttu-id="0e9d3-114">No entanto, lembre-se de que a abordagem recomendada é simplesmente chamar um desses métodos **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="0e9d3-114">However, be aware that the recommend approach is simply to call one of these **ICaptureGraphBuilder2** methods.</span></span>

<span data-ttu-id="0e9d3-115">Os Pins em um filtro WDM dão suporte a um ou mais meios.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-115">The pins on a WDM filter support one or more mediums.</span></span> <span data-ttu-id="0e9d3-116">Um meio define um método de comunicação, como um barramento.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-116">A medium defines a method of communication, such as a bus.</span></span> <span data-ttu-id="0e9d3-117">Você deve conectar Pins que dão suporte à mesma mídia.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-117">You must connect pins that support the same medium.</span></span> <span data-ttu-id="0e9d3-118">A estrutura [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) , que é equivalente à estrutura **\_ média KSPIN** usada para drivers de streaming de kernel, define um meio no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-118">The [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structure, which is equivalent to the **KSPIN\_MEDIUM** structure used for kernel streaming drivers, defines a medium in DirectShow.</span></span> <span data-ttu-id="0e9d3-119">O membro **clsMedium** da estrutura **REGPINMEDIUM** especifica o identificador de classe (CLSID) para a mídia.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-119">The **clsMedium** member of the **REGPINMEDIUM** structure specifies the class identifier (CLSID) for the medium.</span></span> <span data-ttu-id="0e9d3-120">Para recuperar a mídia de um PIN, chame o método [**IKsPin:: KsQueryMediums**](ikspin-ksquerymediums.md) .</span><span class="sxs-lookup"><span data-stu-id="0e9d3-120">To retrieve a pin's medium, call the [**IKsPin::KsQueryMediums**](ikspin-ksquerymediums.md) method.</span></span> <span data-ttu-id="0e9d3-121">Esse método retorna um ponteiro para um bloco de memória que contém uma estrutura de [**\_ Item KSMULTIPLE**](ksmultiple-item.md) , seguida por zero ou mais estruturas **REGPINMEDIUM** .</span><span class="sxs-lookup"><span data-stu-id="0e9d3-121">This method returns a pointer to a block of memory that contains a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, followed by zero or more **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="0e9d3-122">Cada estrutura **REGPINMEDIUM** identifica um meio ao qual o PIN dá suporte.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-122">Each **REGPINMEDIUM** structure identifies a medium the pin supports.</span></span>

<span data-ttu-id="0e9d3-123">Não conecte um PIN se o meio tiver um CLSID de GUID \_ NULL ou KSMEDIUMSETID \_ standard.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-123">Do not connect a pin if the medium has a CLSID of GUID\_NULL or KSMEDIUMSETID\_Standard.</span></span> <span data-ttu-id="0e9d3-124">Esses são valores padrão que indicam que o PIN não oferece suporte a meios.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-124">These are default values indicating that the pin does not support mediums.</span></span>

<span data-ttu-id="0e9d3-125">Além disso, não conecte um PIN, a menos que o filtro exija exatamente uma instância conectada desse PIN.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-125">Also, do not connect a pin unless the filter requires exactly one connected instance of that pin.</span></span> <span data-ttu-id="0e9d3-126">Caso contrário, seu aplicativo pode tentar conectar vários Pins que não devem ter conexões, o que pode fazer com que o programa pare de responder.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-126">Otherwise, your application might try to connect various pins that shouldn't have connections, which can cause the program to stop responding.</span></span> <span data-ttu-id="0e9d3-127">Para descobrir o número de instâncias necessárias, recupere o conjunto de \_ Propriedades do KSPROPERTY PIN \_ NECESSARYINSTANCES, conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-127">To find out the number of required instances, retrieve the KSPROPERTY\_PIN\_NECESSARYINSTANCES property set, as shown in the following code example.</span></span> <span data-ttu-id="0e9d3-128">(Para fins de brevidade, este exemplo não testa nenhum código de retorno nem libera interfaces.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-128">(For brevity, this example does not test any return codes or release any interfaces.</span></span> <span data-ttu-id="0e9d3-129">O aplicativo deve fazer ambos, é claro.)</span><span class="sxs-lookup"><span data-stu-id="0e9d3-129">Your application should do both, of course.)</span></span>


```C++
// Obtain the pin factory identifier.
IKsPinFactory *pPinFactory;
hr = pPin->QueryInterface(IID_IKsPinFactory, (void **)&pPinFactory);

ULONG ulFactoryId;
hr = pPinFactory->KsPinFactory(&ulFactoryId);

// Get the "instance" property from the filter.
IKsControl *pKsControl;
hr = pFilter->QueryInterface(IID_IKsControl, (void **)&pKsControl);

KSP_PIN ksPin;
ksPin.Property.Set = KSPROPSETID_Pin;
ksPin.Property.Id = KSPROPERTY_PIN_NECESSARYINSTANCES;
ksPin.Property.Flags = KSPROPERTY_TYPE_GET;
ksPin.PinId = ulFactoryId;
ksPin.Reserved = 0; 

KSPROPERTY ksProp;
ULONG ulInstances, bytes;
pKsControl->KsProperty((PKSPROPERTY)&ksPin, sizeof(ksPin), 
    &ulInstances, sizeof(ULONG), &bytes);

if (hr == S_OK && bytes == sizeof(ULONG)) 
{
    if (ulInstances == 1) 
    {
        // Filter requires one instance of this pin.
        // This pin is OK.
    } 
}
```



<span data-ttu-id="0e9d3-130">O pseudocódigo a seguir é uma estrutura de tópicos extremamente breve que mostra como localizar e conectar os filtros WDM.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-130">The following pseudocode is an extremely brief outline showing how to find and connect the WDM filters.</span></span> <span data-ttu-id="0e9d3-131">Ele omite muitos detalhes e tem o objetivo de mostrar as etapas gerais que seu aplicativo precisaria executar.</span><span class="sxs-lookup"><span data-stu-id="0e9d3-131">It omits many details, and is only meant to show the general steps your application would need to take.</span></span>


```C++
Add supporting filters:
{
    foreach input pin:
        skip if (pin is connected)
    
        Get pin medium
        skip if (medium is GUID_NULL or KSMEDIUMSETID_Standard)
    
        Query filter for KSPROPERTY_PIN_NECESSARYINSTANCES property
        skip if (necessary instances != 1)

        Match an existing pin || Find a matching filter
}    

Match an existing pin:
{
    foreach filter in the graph
        foreach unconnected pin
            Get pin medium
            if (mediums match)
                connect the pins    
}

Find a matching filter:
{    
    Query the filter graph manager for IFilterMapper2.
    Find a filter with an output pin that matches the medium.
    Add the filter to the graph.
    Connect the pins.
    Add supporting filters. (Recursive call.)
}
```



## <a name="related-topics"></a><span data-ttu-id="0e9d3-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e9d3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e9d3-133">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="0e9d3-133">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



