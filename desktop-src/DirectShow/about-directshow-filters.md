---
description: Sobre filtros do DirectShow
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Sobre filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550850"
---
# <a name="about-directshow-filters"></a><span data-ttu-id="3e6b4-103">Sobre filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e6b4-103">About DirectShow Filters</span></span>

<span data-ttu-id="3e6b4-104">O DirectShow usa uma arquitetura modular, em que cada estágio de processamento é feito por um objeto COM chamado de filtro.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-104">DirectShow uses a modular architecture, where each stage of processing is done by a COM object called a filter.</span></span> <span data-ttu-id="3e6b4-105">O DirectShow fornece um conjunto de filtros padrão para aplicativos a serem usados, e os desenvolvedores podem escrever seus próprios filtros personalizados que estendem a funcionalidade do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-105">DirectShow provides a set of standard filters for applications to use, and developers can write their own custom filters that extend the functionality of DirectShow.</span></span> <span data-ttu-id="3e6b4-106">Para ilustrar, aqui estão as etapas necessárias para reproduzir um arquivo de vídeo AVI, juntamente com os filtros que executam cada etapa:</span><span class="sxs-lookup"><span data-stu-id="3e6b4-106">To illustrate, here are the steps needed to play an AVI video file, along with the filters that perform each step:</span></span>

-   <span data-ttu-id="3e6b4-107">Leia os dados brutos do arquivo como um fluxo de bytes (filtro de origem de arquivo).</span><span class="sxs-lookup"><span data-stu-id="3e6b4-107">Read the raw data from the file as a byte stream (File Source filter).</span></span>
-   <span data-ttu-id="3e6b4-108">Examine os cabeçalhos AVI e analise o fluxo de bytes em quadros de vídeo e amostras de áudio separados (filtro de Splitter AVI).</span><span class="sxs-lookup"><span data-stu-id="3e6b4-108">Examine the AVI headers, and parse the byte stream into separate video frames and audio samples (AVI Splitter filter).</span></span>
-   <span data-ttu-id="3e6b4-109">Decodifique os quadros de vídeo (vários filtros de decodificador, dependendo do formato de compactação).</span><span class="sxs-lookup"><span data-stu-id="3e6b4-109">Decode the video frames (various decoder filters, depending on the compression format).</span></span>
-   <span data-ttu-id="3e6b4-110">Desenhe os quadros de vídeo (filtro de processamento de vídeo).</span><span class="sxs-lookup"><span data-stu-id="3e6b4-110">Draw the video frames (Video Renderer filter).</span></span>
-   <span data-ttu-id="3e6b4-111">Envie os exemplos de áudio para a placa de som (filtro de dispositivo DirectSound padrão).</span><span class="sxs-lookup"><span data-stu-id="3e6b4-111">Send the audio samples to the sound card (Default DirectSound Device filter).</span></span>

<span data-ttu-id="3e6b4-112">Esses filtros são mostrados no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-112">These filters are shown in the following diagram.</span></span>

![gráfico de filtro para reprodução de um arquivo AVI com vídeo compactado](images/avi-filter-graph.png)

<span data-ttu-id="3e6b4-114">Como mostra o diagrama, cada filtro é conectado a um ou mais filtros.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-114">As the diagram shows, each filter is connected to one or more other filters.</span></span> <span data-ttu-id="3e6b4-115">Os pontos de conexão também são objetos COM, chamados *Pins*.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-115">The connection points are also COM objects, called *pins*.</span></span> <span data-ttu-id="3e6b4-116">Os filtros usam Pins para mover dados de um filtro para o próximo.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-116">Filters use pins to move data from one filter the next.</span></span> <span data-ttu-id="3e6b4-117">As setas no diagrama mostram a direção na qual os dados viajam.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-117">The arrows in the diagram show the direction in which the data travels.</span></span> <span data-ttu-id="3e6b4-118">No DirectShow, um conjunto de filtros é chamado de *gráfico de filtro*.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-118">In DirectShow, a set of filters is called a *filter graph*.</span></span>

<span data-ttu-id="3e6b4-119">Os filtros têm três estados possíveis: em execução, parado e em pausa.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-119">Filters have three possible states: running, stopped, and paused.</span></span> <span data-ttu-id="3e6b4-120">Quando um filtro está em execução, ele processa os dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-120">When a filter is running, it processes media data.</span></span> <span data-ttu-id="3e6b4-121">Quando ele é interrompido, ele para de processar os dados.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-121">When it is stopped, it stops processing data.</span></span> <span data-ttu-id="3e6b4-122">O estado em pausa é usado para a indicação de dados antes da execução; o fluxo de dados da seção [no gráfico de filtro](data-flow-in-the-filter-graph.md) descreve esse conceito em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-122">The paused state is used to cue data before running; the section [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) describes this concept in more detail.</span></span> <span data-ttu-id="3e6b4-123">Com exceções muito raras, as alterações de estado são coordenadas em todo o grafo de filtro; todos os filtros na opção de gráfico não são ativados.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-123">With very rare exceptions, state changes are coordinated throughout the entire filter graph; all the filters in the graph switch states in unison.</span></span> <span data-ttu-id="3e6b4-124">Assim, todo o gráfico de filtro também é considerado em execução, parado ou pausado.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-124">Thus, the entire filter graph is also said to be running, stopped, or paused.</span></span>

<span data-ttu-id="3e6b4-125">Os filtros podem ser agrupados em várias categorias amplas:</span><span class="sxs-lookup"><span data-stu-id="3e6b4-125">Filters can be grouped into several broad categories:</span></span>

-   <span data-ttu-id="3e6b4-126">Um filtro de *origem* introduz dados no grafo.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-126">A *source* filter introduces data into the graph.</span></span> <span data-ttu-id="3e6b4-127">Os dados podem vir de um arquivo, uma rede, uma câmera ou qualquer outro lugar.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-127">The data might come from a file, a network, a camera, or anywhere else.</span></span> <span data-ttu-id="3e6b4-128">Cada filtro de origem manipula um tipo diferente de fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-128">Each source filter handles a different type of data source.</span></span>
-   <span data-ttu-id="3e6b4-129">Um filtro de *transformação* usa um fluxo de entrada, processa os dados e cria um fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-129">A *transform* filter takes an input stream, processes the data, and creates an output stream.</span></span> <span data-ttu-id="3e6b4-130">Codificadores e decodificadores são exemplos de filtros de transformação.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-130">Encoders and decoders are examples of transform filters.</span></span>
-   <span data-ttu-id="3e6b4-131">Os filtros de *renderização* ficam no final da cadeia.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-131">*Renderer* filters sit at the end of the chain.</span></span> <span data-ttu-id="3e6b4-132">Eles recebem dados e apresentam a ele o usuário.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-132">They receive data and present it to the user.</span></span> <span data-ttu-id="3e6b4-133">Por exemplo, um processador de vídeo desenha quadros de vídeo na tela; um processador de áudio envia dados de áudio para a placa de som; e um filtro de gravador de arquivo grava dados em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-133">For example, a video renderer draws video frames on the display; an audio renderer sends audio data to the sound card; and a file-writer filter writes data to a file.</span></span>
-   <span data-ttu-id="3e6b4-134">Um filtro de *divisão* divide um fluxo de entrada em duas ou mais saídas, normalmente analisando o fluxo de entrada ao longo do caminho.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-134">A *splitter* filter splits an input stream into two or more outputs, typically parsing the input stream along the way.</span></span> <span data-ttu-id="3e6b4-135">Por exemplo, o divisor AVI analisa um fluxo de bytes em fluxos de áudio e vídeo separados.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-135">For example, the AVI Splitter parses a byte stream into separate video and audio streams.</span></span>
-   <span data-ttu-id="3e6b4-136">Um filtro *MUX* usa várias entradas e as combina em um único fluxo.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-136">A *mux* filter takes multiple inputs and combines them into a single stream.</span></span> <span data-ttu-id="3e6b4-137">Por exemplo, o AVI Mux executa a operação inversa do divisor AVI.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-137">For example, the AVI Mux performs the inverse operation of the AVI Splitter.</span></span> <span data-ttu-id="3e6b4-138">Ele usa fluxos de áudio e vídeo e produz um fluxo de bytes formatado em AVI.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-138">It takes audio and video streams and produces an AVI-formatted byte stream.</span></span>

<span data-ttu-id="3e6b4-139">As distinções entre essas categorias não são absolutas.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-139">The distinctions between these categories are not absolute.</span></span> <span data-ttu-id="3e6b4-140">Por exemplo, o filtro de leitor de ASF atua como um filtro de origem e um filtro de divisão.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-140">For example, the ASF Reader filter acts as both a source filter and a splitter filter.</span></span>

<span data-ttu-id="3e6b4-141">Todos os filtros do DirectShow expõem a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e todos os Pins expõem a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="3e6b4-141">All DirectShow filters expose the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, and all pins expose the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="3e6b4-142">O DirectShow também define muitas outras interfaces que dão suporte a uma funcionalidade mais específica.</span><span class="sxs-lookup"><span data-stu-id="3e6b4-142">DirectShow also defines many other interfaces that support more specific functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e6b4-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e6b4-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e6b4-144">Sobre o Gerenciador do grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="3e6b4-144">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)
</dt> <dt>

[<span data-ttu-id="3e6b4-145">Fluxo de dados no grafo de filtro</span><span class="sxs-lookup"><span data-stu-id="3e6b4-145">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="3e6b4-146">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e6b4-146">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



