---
description: Exemplo de filtro de sintetizador
ms.assetid: 2d087967-3734-463f-bc5e-9552290ddc0b
title: Exemplo de filtro de sintetizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd569091df92eca3fbff4d8cb200150d6e6bfdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837139"
---
# <a name="synth-filter-sample"></a><span data-ttu-id="9e4a6-103">Exemplo de filtro de sintetizador</span><span class="sxs-lookup"><span data-stu-id="9e4a6-103">Synth Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="9e4a6-104">Description</span><span class="sxs-lookup"><span data-stu-id="9e4a6-104">Description</span></span>

<span data-ttu-id="9e4a6-105">O filtro de sintetizador é um filtro de origem que gera ondas de áudio.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-105">The Synth filter is a source filter that generates audio waveforms.</span></span>

<span data-ttu-id="9e4a6-106">Esse filtro ilustra a criação dinâmica de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-106">This filter illustrates dynamic graph building.</span></span> <span data-ttu-id="9e4a6-107">Ele pode alternar entre o áudio PCM não compactado e o formato compactado MS \_ ADPCM (modulação de código de pulso Delta da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="9e4a6-107">It can switch between uncompressed PCM audio and compressed MS\_ADPCM (Microsoft Adaptive Delta Pulse Code Modulation) format.</span></span>

<span data-ttu-id="9e4a6-108">Esse filtro aparece em GraphEdit como "filtro de sintetizador de áudio".</span><span class="sxs-lookup"><span data-stu-id="9e4a6-108">This filter appears in GraphEdit as "Audio Synthesizer Filter."</span></span>

<span data-ttu-id="9e4a6-109">Para obter mais informações sobre a criação de grafo dinâmico, consulte [criação de grafo dinâmico](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="9e4a6-109">For more information about dynamic graph building, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="usage"></a><span data-ttu-id="9e4a6-110">Uso</span><span class="sxs-lookup"><span data-stu-id="9e4a6-110">Usage</span></span>

<span data-ttu-id="9e4a6-111">O filtro sintetizador permite que o usuário defina a forma de onda, a frequência, o número de canais e outras propriedades por meio da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-111">The Synth filter enables the user to set the waveform, frequency, number of channels, and other properties through the property page.</span></span> <span data-ttu-id="9e4a6-112">Para definir o ponto de extremidade superior ou inferior do intervalo de frequência de removido, mantenha pressionada a tecla SHIFT enquanto ajusta o controle deslizante de frequência.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-112">To set either the upper or lower endpoint of the swept frequency range, hold down SHIFT while adjusting the frequency slider.</span></span> <span data-ttu-id="9e4a6-113">O filtro também dá suporte a uma interface personalizada, ISynth2, para definir essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-113">The filter also supports a custom interface, ISynth2, for setting these properties.</span></span>

<span data-ttu-id="9e4a6-114">Para demonstrar o recurso de criação de gráfico dinâmico, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9e4a6-114">To demonstrate the dynamic graph building feature, do the following:</span></span>

1.  <span data-ttu-id="9e4a6-115">Crie o filtro e registre-o com o utilitário regsvr32.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-115">Build the filter and register it with the Regsvr32 utility.</span></span>
2.  <span data-ttu-id="9e4a6-116">Inicie o GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-116">Launch GraphEdit.</span></span>
3.  <span data-ttu-id="9e4a6-117">Insira o filtro sintetizador de áudio.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-117">Insert the Audio Synthesizer filter.</span></span> <span data-ttu-id="9e4a6-118">Ele aparece na categoria filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-118">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="9e4a6-119">Renderizar o pino de saída do filtro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-119">Render the filter's output pin.</span></span>
5.  <span data-ttu-id="9e4a6-120">Clique no botão **reproduzir** .</span><span class="sxs-lookup"><span data-stu-id="9e4a6-120">Click the **Play** button.</span></span>
6.  <span data-ttu-id="9e4a6-121">Abra a página de propriedades do filtro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-121">Open the filter's property page.</span></span>
7.  <span data-ttu-id="9e4a6-122">Na área formato de saída, selecione PCM ou Microsoft ADPCM.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-122">In the Output Format area, select PCM or Microsoft ADPCM.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="9e4a6-123">Notas de programação</span><span class="sxs-lookup"><span data-stu-id="9e4a6-123">Programming Notes</span></span>

<span data-ttu-id="9e4a6-124">Este exemplo contém os seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="9e4a6-124">This sample contains the following files:</span></span>

-   <span data-ttu-id="9e4a6-125">Dynsrc. h, dynsrc. cpp: contém duas classes base para filtros de origem que dão suporte à criação de grafo dinâmico, CDynamicSource e CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-125">Dynsrc.h, Dynsrc.cpp: Contains two base classes for source filters that support dynamic graph building, CDynamicSource and CDynamicSourceStream.</span></span>
-   <span data-ttu-id="9e4a6-126">ISynth. h: declara a interface ISynth2 personalizada para definir propriedades no filtro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-126">ISynth.h: Declares the custom ISynth2 interface for setting properties on the filter.</span></span>
-   <span data-ttu-id="9e4a6-127">Resource. h: contém constantes de recurso.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-127">Resource.h: Contains resource constants.</span></span>
-   <span data-ttu-id="9e4a6-128">Sintetizador. def: exporta as funções de DLL necessárias para a biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-128">Synth.def: Exports the DLL functions needed by the COM library.</span></span>
-   <span data-ttu-id="9e4a6-129">Sintetizador. h, sintetizador. cpp: contém a classe CAudioSynth, que gera os dados de áudio e a classe CSynthFilter, que implementa o filtro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-129">Synth.h, Synth.cpp: Contains the CAudioSynth class, which generates the audio data, and the CSynthFilter class, which implements the filter.</span></span>
-   <span data-ttu-id="9e4a6-130">Sintetizador. rc: contém recursos usados pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-130">Synth.rc: Contains resources used by the filter.</span></span>
-   <span data-ttu-id="9e4a6-131">Synthprp. h, Synthprp. cpp: implementa a página de propriedades do filtro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-131">Synthprp.h, Synthprp.cpp: Implements the filter's property page.</span></span>

<span data-ttu-id="9e4a6-132">A classe CDynamicSource é adaptada da classe base [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="9e4a6-132">The CDynamicSource class is adapted from the [**CSource**](csource.md) base class.</span></span> <span data-ttu-id="9e4a6-133">Ele usa um ou mais Pins de saída derivados da classe CDynamicSourceStream.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-133">It uses one or more output pins derived from the CDynamicSourceStream class.</span></span> <span data-ttu-id="9e4a6-134">A classe CDynamicSourceStream é adaptada da classe [**CSourceStream**](csourcestream.md) , mas deriva da classe [**CDynamicOutputPin**](cdynamicoutputpin.md) em vez da classe [**CBaseOutputPin**](cbaseoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="9e4a6-134">The CDynamicSourceStream class is adapted from the [**CSourceStream**](csourcestream.md) class, but derives from the [**CDynamicOutputPin**](cdynamicoutputpin.md) class rather than the [**CBaseOutputPin**](cbaseoutputpin.md) class.</span></span>

<span data-ttu-id="9e4a6-135">A classe CDynamicSource tem os seguintes métodos não encontrados em [**CSource**](csource.md):</span><span class="sxs-lookup"><span data-stu-id="9e4a6-135">The CDynamicSource class has the following methods not found in [**CSource**](csource.md):</span></span>

-   <span data-ttu-id="9e4a6-136">Stop: sinaliza o evento de parada ([**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)) e desliga o thread de trabalho para todos os Pins não conectados.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-136">Stop: Signals the stop event ([**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md)), and shuts down the worker thread for all unconnected pins.</span></span> <span data-ttu-id="9e4a6-137">Em um PIN conectado, o método inativo do PIN desligará o thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-137">On a connected pin, the pin's Inactive method will shut down the worker thread.</span></span>
-   <span data-ttu-id="9e4a6-138">Pausa: redefine o evento de parada.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-138">Pause: Resets the stop event.</span></span>
-   <span data-ttu-id="9e4a6-139">JoinFilterGraph: chama o método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) em cada PIN.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-139">JoinFilterGraph: Calls the [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) method on each pin.</span></span>

<span data-ttu-id="9e4a6-140">A classe CDynamicSourceStream tem os seguintes métodos não encontrados em [**CSourceStream**](csourcestream.md):</span><span class="sxs-lookup"><span data-stu-id="9e4a6-140">The CDynamicSourceStream class has the following methods not found in [**CSourceStream**](csourcestream.md):</span></span>

-   <span data-ttu-id="9e4a6-141">DestroySourceThread: desliga o thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-141">DestroySourceThread: Shuts down the worker thread.</span></span>
-   <span data-ttu-id="9e4a6-142">FatalError: sinaliza um erro para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-142">FatalError: Signals an error to the filter graph manager.</span></span>
-   <span data-ttu-id="9e4a6-143">OutputPinNeedsToBeReconnected: sinaliza que o pino de saída deve ser reconectado.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-143">OutputPinNeedsToBeReconnected: Signals that the output pin should be reconnected.</span></span> <span data-ttu-id="9e4a6-144">Quando esse método é chamado, o thread de trabalho chama o método [**CDynamicOutputPin::D ynamicreconnect**](cdynamicoutputpin-dynamicreconnect.md) para reconectar o PIN.</span><span class="sxs-lookup"><span data-stu-id="9e4a6-144">When this method is called, the worker thread calls the [**CDynamicOutputPin::DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md) method to reconnect the pin.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="9e4a6-145">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="9e4a6-145">Downloading the Sample</span></span>

<span data-ttu-id="9e4a6-146">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e4a6-146">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="9e4a6-147">Este exemplo é instalado no seguinte caminho: exemplo de *\[ raiz \] do SDK* \\ exemplos de multimídia do DirectShow de \\ Multimedia \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="9e4a6-147">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Synth.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e4a6-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e4a6-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e4a6-149">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="9e4a6-149">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



