---
description: Este tópico descreve como criar uma topologia para reprodução de áudio ou vídeo.
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: Criando topologias de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763281"
---
# <a name="creating-playback-topologies"></a><span data-ttu-id="d5f26-103">Criando topologias de reprodução</span><span class="sxs-lookup"><span data-stu-id="d5f26-103">Creating Playback Topologies</span></span>

<span data-ttu-id="d5f26-104">Este tópico descreve como criar uma topologia para reprodução de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-104">This topic describes how to create a topology for audio or video playback.</span></span> <span data-ttu-id="d5f26-105">Para a reprodução básica, você pode criar uma topologia parcial, na qual os nós de origem estão conectados diretamente aos nós de saída.</span><span class="sxs-lookup"><span data-stu-id="d5f26-105">For basic playback, you can create a partial topology, in which the source nodes are connected directly to the output nodes.</span></span> <span data-ttu-id="d5f26-106">Você não precisa inserir nenhum nó para as transformações intermediárias, como decodificadores ou conversores de cor.</span><span class="sxs-lookup"><span data-stu-id="d5f26-106">You do not need to insert any nodes for the intermediate transforms, such as decoders or color converters.</span></span> <span data-ttu-id="d5f26-107">A sessão de mídia usará o carregador de topologia para resolver a topologia e o carregador de topologia irá inserir as transformações necessárias.</span><span class="sxs-lookup"><span data-stu-id="d5f26-107">The Media Session will use the topology loader to resolve the topology, and the topology loader will insert the transforms that are required.</span></span>

-   [<span data-ttu-id="d5f26-108">Criando a topologia</span><span class="sxs-lookup"><span data-stu-id="d5f26-108">Creating the Topology</span></span>](#creating-the-topology)
-   [<span data-ttu-id="d5f26-109">Conectando fluxos a coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="d5f26-109">Connecting Streams to Media Sinks</span></span>](#connecting-streams-to-media-sinks)
-   [<span data-ttu-id="d5f26-110">Criando o coletor de mídia</span><span class="sxs-lookup"><span data-stu-id="d5f26-110">Creating the Media Sink</span></span>](#creating-the-media-sink)
-   [<span data-ttu-id="d5f26-111">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d5f26-111">Next Steps</span></span>](#next-steps)
-   [<span data-ttu-id="d5f26-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5f26-112">Related topics</span></span>](#related-topics)

## <a name="creating-the-topology"></a><span data-ttu-id="d5f26-113">Criando a topologia</span><span class="sxs-lookup"><span data-stu-id="d5f26-113">Creating the Topology</span></span>

<span data-ttu-id="d5f26-114">Aqui estão as etapas gerais para criar uma topologia de reprodução parcial de uma fonte de mídia:</span><span class="sxs-lookup"><span data-stu-id="d5f26-114">Here are the overall steps for creating a partial playback topology from a media source:</span></span>

1.  <span data-ttu-id="d5f26-115">Crie a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-115">Create the media source.</span></span> <span data-ttu-id="d5f26-116">Na maioria dos casos, você usará o resolvedor de origem para criar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-116">In most cases, you will use the source resolver to create the media source.</span></span> <span data-ttu-id="d5f26-117">Para obter mais informações, consulte [resolvedor de origem](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-117">For more information, see [Source Resolver](source-resolver.md).</span></span>
2.  <span data-ttu-id="d5f26-118">Obtenha o descritor de apresentação da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-118">Get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="d5f26-119">Crie uma topologia vazia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-119">Create an empty topology.</span></span>
4.  <span data-ttu-id="d5f26-120">Use o descritor de apresentação para enumerar os descritores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-120">Use the presentation descriptor to enumerate the stream descriptors.</span></span> <span data-ttu-id="d5f26-121">Para cada descritor de fluxo:</span><span class="sxs-lookup"><span data-stu-id="d5f26-121">For each stream descriptor:</span></span>
    1.  <span data-ttu-id="d5f26-122">Obtenha o tipo de mídia principal do fluxo, como áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-122">Get the stream's major media type, such as audio or video.</span></span>
    2.  <span data-ttu-id="d5f26-123">Verifique se o fluxo está selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="d5f26-123">Check if the stream is currently selected.</span></span> <span data-ttu-id="d5f26-124">(Opcionalmente, você pode selecionar ou desmarcar um fluxo, com base no tipo de mídia.)</span><span class="sxs-lookup"><span data-stu-id="d5f26-124">(Optionally, you can select or deselect a stream, based on the media type.)</span></span>
    3.  <span data-ttu-id="d5f26-125">Se o fluxo for selecionado, crie um objeto de ativação para o coletor de mídia, com base no tipo de mídia do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-125">If the stream is selected, create an activation object for the media sink, based on the stream's media type.</span></span>
    4.  <span data-ttu-id="d5f26-126">Adicione um nó de origem para o fluxo e um nó de saída para o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-126">Add a source node for the stream and an output node for the media sink.</span></span>
    5.  <span data-ttu-id="d5f26-127">Conecte o nó de origem ao nó de saída.</span><span class="sxs-lookup"><span data-stu-id="d5f26-127">Connect the source node to the output node.</span></span>

<span data-ttu-id="d5f26-128">Para facilitar o acompanhamento desse processo, o código de exemplo neste tópico é organizado em várias funções.</span><span class="sxs-lookup"><span data-stu-id="d5f26-128">To make this process easier to follow, the example code in this topic is organized into several functions.</span></span> <span data-ttu-id="d5f26-129">A função de nível superior é denominada `CreatePlaybackTopology` .</span><span class="sxs-lookup"><span data-stu-id="d5f26-129">The top-level function is named `CreatePlaybackTopology`.</span></span> <span data-ttu-id="d5f26-130">São necessários três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d5f26-130">It takes three parameters:</span></span>

-   <span data-ttu-id="d5f26-131">Um ponteiro para uma interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-131">A pointer to a [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="d5f26-132">Um ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="d5f26-132">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span> <span data-ttu-id="d5f26-133">Obtenha esse ponteiro chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="d5f26-133">Get this pointer by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="d5f26-134">Para fontes com várias apresentações, os descritores de apresentação das apresentações subsequentes são entregues no evento [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="d5f26-134">For sources with multiple presentations, the presentation descriptors for subsequent presentations are delivered in the [MENewPresentation](menewpresentation.md) event.</span></span>
-   <span data-ttu-id="d5f26-135">Um identificador para uma janela de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-135">A handle to an application window.</span></span> <span data-ttu-id="d5f26-136">Se a fonte tiver um fluxo de vídeo, o vídeo será exibido nessa janela.</span><span class="sxs-lookup"><span data-stu-id="d5f26-136">If the source has a video stream, the video will be displayed in this window.</span></span>

<span data-ttu-id="d5f26-137">A função retorna um ponteiro para uma topologia de reprodução parcial no parâmetro *ppTopology* .</span><span class="sxs-lookup"><span data-stu-id="d5f26-137">The function returns a pointer to a partial playback topology in the *ppTopology* parameter.</span></span>


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="d5f26-138">Esta função realiza as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d5f26-138">This function performs the following steps:</span></span>

1.  <span data-ttu-id="d5f26-139">Chame [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) para criar a topologia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-139">Call [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) to create the topology.</span></span> <span data-ttu-id="d5f26-140">Inicialmente, a topologia não contém nenhum nó.</span><span class="sxs-lookup"><span data-stu-id="d5f26-140">Initially, the topology does not contain any nodes.</span></span>
2.  <span data-ttu-id="d5f26-141">Chame [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obter o número de fluxos na apresentação.</span><span class="sxs-lookup"><span data-stu-id="d5f26-141">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the presentation.</span></span>
3.  <span data-ttu-id="d5f26-142">Para cada fluxo, chame a função definida pelo aplicativo `AddBranchToPartialTopology` para uma ramificação na topologia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-142">For each stream, call the application-defined `AddBranchToPartialTopology` function to a branch in the topology.</span></span> <span data-ttu-id="d5f26-143">Essa função é mostrada na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="d5f26-143">This function is shown in the next section.</span></span>

## <a name="connecting-streams-to-media-sinks"></a><span data-ttu-id="d5f26-144">Conectando fluxos a coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="d5f26-144">Connecting Streams to Media Sinks</span></span>

<span data-ttu-id="d5f26-145">Para cada fluxo selecionado, adicione um nó de origem e um nó de saída e conecte os dois nós.</span><span class="sxs-lookup"><span data-stu-id="d5f26-145">For each selected stream, add a source node and an output node, then connect the two nodes.</span></span> <span data-ttu-id="d5f26-146">O nó de origem representa o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-146">The source node represents the stream.</span></span> <span data-ttu-id="d5f26-147">O nó de saída representa o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) ou o [renderizador de áudio de streaming](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="d5f26-147">The output node represents either the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) or the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

<span data-ttu-id="d5f26-148">A `AddBranchToPartialTopology` função, mostrada no próximo exemplo, usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="d5f26-148">The `AddBranchToPartialTopology` function, shown in the next example, takes the following parameters:</span></span>

-   <span data-ttu-id="d5f26-149">Um ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-149">A pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span>
-   <span data-ttu-id="d5f26-150">Um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-150">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="d5f26-151">Um ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="d5f26-151">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span>
-   <span data-ttu-id="d5f26-152">O índice de base zero do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-152">The zero-based index of the stream.</span></span>
-   <span data-ttu-id="d5f26-153">Um identificador para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-153">A handle to the video window.</span></span> <span data-ttu-id="d5f26-154">Esse identificador é usado apenas para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-154">This handle is used only for the video stream.</span></span>


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



<span data-ttu-id="d5f26-155">A função faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d5f26-155">The function does the following:</span></span>

1.  <span data-ttu-id="d5f26-156">Chama [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passa o índice de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-156">Calls [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and passes in the stream index.</span></span> <span data-ttu-id="d5f26-157">Esse método retorna um ponteiro para o descritor de fluxo para esse fluxo, juntamente com um valor booliano que indica se o fluxo está selecionado.</span><span class="sxs-lookup"><span data-stu-id="d5f26-157">This method returns a pointer to the stream descriptor for that stream, along with a Boolean value indicating whether the stream is selected.</span></span>
2.  <span data-ttu-id="d5f26-158">Se o fluxo não estiver selecionado, a função será encerrada e retornará S \_ OK, pois o aplicativo não precisa criar uma ramificação de topologia para um fluxo, a menos que esteja selecionado.</span><span class="sxs-lookup"><span data-stu-id="d5f26-158">If the stream is not selected, the function exits and returns S\_OK, because the application does not need to create a topology branch for a stream unless it is selected.</span></span>
3.  <span data-ttu-id="d5f26-159">Se o fluxo for selecionado, a função concluirá a ramificação de topologia da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5f26-159">If the stream is selected, the function completes the topology branch as follows:</span></span>
    1.  <span data-ttu-id="d5f26-160">Cria um objeto de ativação para o coletor, chamando a função CreateMediaSinkActivate definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-160">Creates an activation object for the sink, by calling the application-defined CreateMediaSinkActivate function.</span></span> <span data-ttu-id="d5f26-161">Essa função é mostrada na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="d5f26-161">This function is shown in the next section.</span></span>
    2.  <span data-ttu-id="d5f26-162">Adiciona um nó de origem à topologia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-162">Adds a source node to the topology.</span></span> <span data-ttu-id="d5f26-163">O código para essa etapa é mostrado no tópico [criando nós de origem](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-163">Code for this step is shown in the topic [Creating Source Nodes](creating-source-nodes.md).</span></span>
    3.  <span data-ttu-id="d5f26-164">Adiciona um nó de saída à topologia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-164">Adds an output node to the topology.</span></span> <span data-ttu-id="d5f26-165">O código para essa etapa é mostrado no tópico [criando nós de saída](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-165">Code for this step is shown in the topic [Creating Output Nodes](creating-output-nodes.md).</span></span>
    4.  <span data-ttu-id="d5f26-166">Conecta os dois nós chamando [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) no nó de origem.</span><span class="sxs-lookup"><span data-stu-id="d5f26-166">Connects the two nodes by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the source node.</span></span> <span data-ttu-id="d5f26-167">Conectando os nós, o aplicativo indica que o nó upstream deve entregar dados ao nó downstream.</span><span class="sxs-lookup"><span data-stu-id="d5f26-167">By connecting the nodes, the application indicates that the upstream node should deliver data to the downstream node.</span></span> <span data-ttu-id="d5f26-168">Um nó de origem tem uma saída e um nó de saída tem uma entrada, portanto os dois índices de fluxo são zero.</span><span class="sxs-lookup"><span data-stu-id="d5f26-168">A source node has one output, and an output node has one input, so both stream indexes are zero.</span></span>

<span data-ttu-id="d5f26-169">Aplicativos mais avançados podem selecionar ou desmarcar fluxos, em vez de usar a configuração padrão da origem.</span><span class="sxs-lookup"><span data-stu-id="d5f26-169">More advanced applications can select or deselect streams, instead of using the source's default configuration.</span></span> <span data-ttu-id="d5f26-170">Uma origem pode ter vários fluxos e qualquer um deles pode ser selecionado por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5f26-170">A source could have multiple streams, and any of them might be selected by default.</span></span> <span data-ttu-id="d5f26-171">O descritor de apresentação da origem de mídia tem um conjunto padrão de seleções de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-171">The media source's presentation descriptor has a default set of stream selections.</span></span> <span data-ttu-id="d5f26-172">Em um arquivo de vídeo simples com um fluxo de áudio único e fluxo de vídeo, a origem da mídia geralmente seleciona os dois fluxos por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5f26-172">In a simple video file with a single audio stream and video stream, the media source will usually select both streams by default.</span></span> <span data-ttu-id="d5f26-173">No entanto, um arquivo pode ter vários fluxos de áudio para diferentes idiomas ou vários fluxos de vídeo codificados em diferentes taxas de bits.</span><span class="sxs-lookup"><span data-stu-id="d5f26-173">However, a file might have multiple audio streams for different languages, or multiple video streams encoded at different bit rates.</span></span> <span data-ttu-id="d5f26-174">Nesse caso, alguns dos fluxos serão desmarcados por padrão.</span><span class="sxs-lookup"><span data-stu-id="d5f26-174">In that case, some of the streams will be unselected by default.</span></span> <span data-ttu-id="d5f26-175">O aplicativo pode alterar a seleção chamando [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) e [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) no descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="d5f26-175">The application can change the selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) on the presentation descriptor.</span></span>

## <a name="creating-the-media-sink"></a><span data-ttu-id="d5f26-176">Criando o coletor de mídia</span><span class="sxs-lookup"><span data-stu-id="d5f26-176">Creating the Media Sink</span></span>

<span data-ttu-id="d5f26-177">A função Next cria um objeto de ativação para o coletor de mídia EVR ou SAR.</span><span class="sxs-lookup"><span data-stu-id="d5f26-177">The next function creates an activation object for the EVR or SAR media sink.</span></span>


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



<span data-ttu-id="d5f26-178">Esta função realiza as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d5f26-178">This function performs the following steps:</span></span>

1.  <span data-ttu-id="d5f26-179">Chama [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-179">Calls [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span> <span data-ttu-id="d5f26-180">Esse método retorna um ponteiro de interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="d5f26-180">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface pointer.</span></span>

2.  <span data-ttu-id="d5f26-181">Chama [**IMFMediaTypeHandler:: Getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="d5f26-181">Calls [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="d5f26-182">Esse método retorna o GUID de tipo principal para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-182">This method returns the major type GUID for the stream.</span></span>

3.  <span data-ttu-id="d5f26-183">Se o tipo de fluxo for áudio, a função chamará [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) para criar o objeto de ativação do processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="d5f26-183">If the stream type is audio, the function calls [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) to create the audio renderer activation object.</span></span> <span data-ttu-id="d5f26-184">Se o tipo de fluxo for vídeo, a função chamará [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar o objeto de ativação do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-184">If the stream type is video, the function calls [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the video renderer activation object.</span></span> <span data-ttu-id="d5f26-185">Ambas as funções retornam um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="d5f26-185">Both of these functions return a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="d5f26-186">Esse ponteiro é usado para inicializar o nó de saída para o coletor, conforme mostrado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="d5f26-186">This pointer is used to initialize the output node for the sink, as shown previously.</span></span>

<span data-ttu-id="d5f26-187">Para qualquer outro tipo de fluxo, este exemplo retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="d5f26-187">For any other stream type, this example returns an error code.</span></span> <span data-ttu-id="d5f26-188">Como alternativa, você poderia simplesmente anular a seleção do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d5f26-188">Alternatively, you could simply deselect the stream.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d5f26-189">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d5f26-189">Next Steps</span></span>

<span data-ttu-id="d5f26-190">Para reproduzir um arquivo de mídia de cada vez, enfileirar a topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="d5f26-190">To play one media file at a time, queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="d5f26-191">A sessão de mídia usará o carregador de topologia para resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="d5f26-191">The Media Session will use the topology loader to resolve the topology.</span></span> <span data-ttu-id="d5f26-192">Para obter um exemplo completo, consulte [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="d5f26-192">For a complete example, see [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5f26-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5f26-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f26-194">Como reproduzir arquivos de mídia desprotegidos</span><span class="sxs-lookup"><span data-stu-id="d5f26-194">How to Play Unprotected Media Files</span></span>](how-to-play-unprotected-media-files.md)
</dt> <dt>

[<span data-ttu-id="d5f26-195">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d5f26-195">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="d5f26-196">Topologias</span><span class="sxs-lookup"><span data-stu-id="d5f26-196">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



