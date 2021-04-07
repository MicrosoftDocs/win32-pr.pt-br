---
description: Este tópico descreve como um filtro de captura personalizado do DirectShow deve gerar dados de saída.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Produzindo dados em um filtro de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919950"
---
# <a name="producing-data-in-a-capture-filter"></a><span data-ttu-id="760ef-103">Produzindo dados em um filtro de captura</span><span class="sxs-lookup"><span data-stu-id="760ef-103">Producing Data in a Capture Filter</span></span>

<span data-ttu-id="760ef-104">Este tópico descreve como um filtro de captura personalizado do DirectShow deve gerar dados de saída.</span><span class="sxs-lookup"><span data-stu-id="760ef-104">This topic describes how a custom DirectShow capture filter should generate output data.</span></span>

## <a name="filter-state-changes"></a><span data-ttu-id="760ef-105">Filtrar alterações de estado</span><span class="sxs-lookup"><span data-stu-id="760ef-105">Filter State Changes</span></span>

<span data-ttu-id="760ef-106">Um filtro de captura deve produzir dados somente quando o filtro está em execução.</span><span class="sxs-lookup"><span data-stu-id="760ef-106">A capture filter should produce data only when the filter is running.</span></span> <span data-ttu-id="760ef-107">Não envie dados de seus PINs quando o filtro for pausado.</span><span class="sxs-lookup"><span data-stu-id="760ef-107">Do not send data from your pins when the filter is paused.</span></span> <span data-ttu-id="760ef-108">Além disso, retornar **VFW \_ S não consegue se \_ \_ Marcar** do método [**CBaseFilter:: GetState**](cbasefilter-getstate.md) quando o filtro é pausado.</span><span class="sxs-lookup"><span data-stu-id="760ef-108">Also, return **VFW\_S\_CANT\_CUE** from the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method when the filter is paused.</span></span> <span data-ttu-id="760ef-109">Esse valor de retorno informa ao Gerenciador do grafo de filtro que ele não deve esperar por nenhum dado do filtro enquanto o filtro está em pausa.</span><span class="sxs-lookup"><span data-stu-id="760ef-109">This return value informs the Filter Graph Manager that it should not wait for any data from your filter while the filter is paused.</span></span> <span data-ttu-id="760ef-110">Para obter mais informações, consulte [Filtrar Estados](filter-states.md).</span><span class="sxs-lookup"><span data-stu-id="760ef-110">For more information, see [Filter States](filter-states.md).</span></span>

<span data-ttu-id="760ef-111">O código a seguir mostra como implementar o método [**IMediaFilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :</span><span class="sxs-lookup"><span data-stu-id="760ef-111">The following code shows how to implement the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method:</span></span>


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a><span data-ttu-id="760ef-112">Controlando fluxos individuais</span><span class="sxs-lookup"><span data-stu-id="760ef-112">Controlling Individual Streams</span></span>

<span data-ttu-id="760ef-113">Os Pins de saída de um filtro de captura devem dar suporte à interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , para que um aplicativo possa ativar ou desativar cada PIN individualmente.</span><span class="sxs-lookup"><span data-stu-id="760ef-113">A capture filter's output pins should support the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, so that an application can turn each pin on or off individually.</span></span> <span data-ttu-id="760ef-114">Por exemplo, um aplicativo pode ser visualizado sem capturar e, em seguida, alternar para o modo de captura sem recriar o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="760ef-114">For example, an application can preview without capturing, and then switch to capture mode without rebuilding the filter graph.</span></span> <span data-ttu-id="760ef-115">Você pode usar a classe [**CBaseStreamControl**](cbasestreamcontrol.md) para implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="760ef-115">You can use the [**CBaseStreamControl**](cbasestreamcontrol.md) class to implement this interface.</span></span>

## <a name="time-stamps"></a><span data-ttu-id="760ef-116">Carimbos de Data/Hora</span><span class="sxs-lookup"><span data-stu-id="760ef-116">Time Stamps</span></span>

<span data-ttu-id="760ef-117">Quando o filtro captura um exemplo, o carimbo de data/hora é o exemplo com a hora atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="760ef-117">When the filter captures a sample, time stamp the sample with the current stream time.</span></span> <span data-ttu-id="760ef-118">A hora de término é a hora de início mais a duração.</span><span class="sxs-lookup"><span data-stu-id="760ef-118">The end time is the start time plus the duration.</span></span> <span data-ttu-id="760ef-119">Por exemplo, se o filtro estiver capturando em dez amostras por segundo, e a hora do fluxo for de 200 milhões unidades quando o filtro capturar o exemplo, os carimbos de data/hora deverão ser 200 milhões e 201 milhões.</span><span class="sxs-lookup"><span data-stu-id="760ef-119">For example, if the filter is capturing at ten samples per second, and the stream time is 200,000,000 units when the filter captures the sample, the time stamps should be 200000000 and 201000000.</span></span> <span data-ttu-id="760ef-120">(Há 10 milhões unidades por segundo.)</span><span class="sxs-lookup"><span data-stu-id="760ef-120">(There are 10,000,000 units per second.)</span></span>

<span data-ttu-id="760ef-121">Para calcular a hora do fluxo, chame o método [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) para obter o tempo de referência atual e, em seguida, substract a hora de início original.</span><span class="sxs-lookup"><span data-stu-id="760ef-121">To calculate the stream time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method to get the current reference time, and then substract the original start time.</span></span> <span data-ttu-id="760ef-122">Como alternativa, chame o método [**CBaseFilter:: streamtime**](cbasefilter-streamtime.md) , que executa o mesmo cálculo.</span><span class="sxs-lookup"><span data-stu-id="760ef-122">Alternatively, call the [**CBaseFilter::StreamTime**](cbasefilter-streamtime.md) method, which performs the same calculation.</span></span> <span data-ttu-id="760ef-123">Para definir o carimbo de data/hora em um exemplo, chame o método [**IMediaSample:: SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="760ef-123">To set the time stamp on a sample, call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

<span data-ttu-id="760ef-124">No entanto, se o filtro tiver um PIN de visualização, os exemplos do pino de visualização não deverão ter carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="760ef-124">If the filter has a preview pin, however, samples from the preview pin should not have time stamps.</span></span> <span data-ttu-id="760ef-125">O motivo é que os exemplos sempre alcançarão um pouco o processador após o momento da captura.</span><span class="sxs-lookup"><span data-stu-id="760ef-125">The reason is that samples will always reach the renderer slightly after the time of capture.</span></span> <span data-ttu-id="760ef-126">Se os exemplos estiverem com carimbo de data/hora, o renderizador os tratará como atrasado e poderá tentar se acumular descartando amostras.</span><span class="sxs-lookup"><span data-stu-id="760ef-126">If the samples are time stamped, the renderer will treat them as late, and it may try to catch up by dropping samples.</span></span> <span data-ttu-id="760ef-127">(Para obter mais informações, consulte [filtros de captura de vídeo do DirectShow](directshow-video-capture-filters.md).) Observe que a interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) exige que o PIN acompanhe os tempos de amostragem.</span><span class="sxs-lookup"><span data-stu-id="760ef-127">(For more information, see [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Note that the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface requires the pin to keep track of sample times.</span></span> <span data-ttu-id="760ef-128">Para um PIN de visualização, talvez seja necessário modificar a implementação para que ela não dependa de carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="760ef-128">For a preview pin, you might need to modify the implementation so that it does not rely on time stamps.</span></span>

<span data-ttu-id="760ef-129">Os carimbos de data/hora sempre devem aumentar de um exemplo para o próximo.</span><span class="sxs-lookup"><span data-stu-id="760ef-129">Time stamps must always increase from one sample to the next.</span></span> <span data-ttu-id="760ef-130">Isso é verdadeiro mesmo quando o filtro é pausado.</span><span class="sxs-lookup"><span data-stu-id="760ef-130">This is true even when the filter pauses.</span></span> <span data-ttu-id="760ef-131">Se o filtro for executado, pausar e executar novamente, o primeiro exemplo após a pausa deverá ter um carimbo de data/hora maior do que o último exemplo antes da pausa.</span><span class="sxs-lookup"><span data-stu-id="760ef-131">If the filter runs, pauses, and then runs again, the first sample after the pause must have a larger time stamp than the last sample before the pause.</span></span>

<span data-ttu-id="760ef-132">Dependendo dos dados que você está capturando, pode ser apropriado definir o tempo de mídia nos exemplos.</span><span class="sxs-lookup"><span data-stu-id="760ef-132">Depending on the data you are capturing, it might be appropriate to set the media time on the samples.</span></span>

<span data-ttu-id="760ef-133">Para obter mais informações, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="760ef-133">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="760ef-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="760ef-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="760ef-135">Filtros de captura de vídeo do DirectShow</span><span class="sxs-lookup"><span data-stu-id="760ef-135">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="760ef-136">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="760ef-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="760ef-137">Gravando filtros de captura</span><span class="sxs-lookup"><span data-stu-id="760ef-137">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



