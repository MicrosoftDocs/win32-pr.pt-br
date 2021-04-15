---
description: Este tópico descreve como usar a origem da sequência para reproduzir uma sequência de arquivos.
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: Como criar uma lista de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502201"
---
# <a name="how-to-create-a-playlist"></a><span data-ttu-id="d0d97-103">Como criar uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="d0d97-103">How to Create a Playlist</span></span>

<span data-ttu-id="d0d97-104">Este tópico descreve como usar a origem da sequência para reproduzir uma sequência de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d0d97-104">This topic describes how to use the Sequence Source to play a sequence of files.</span></span>

## <a name="overview"></a><span data-ttu-id="d0d97-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="d0d97-105">Overview</span></span>

<span data-ttu-id="d0d97-106">Para reproduzir arquivos de mídia em uma sequência, o aplicativo deve adicionar topologias em uma sequência para criar uma lista de reprodução e enfileirar essas topologias na sessão de mídia para reprodução.</span><span class="sxs-lookup"><span data-stu-id="d0d97-106">To play media files in a sequence, the application must add topologies in a sequence to create a playlist, and queue these topologies on the Media Session for playback.</span></span>

<span data-ttu-id="d0d97-107">A origem do sequenciador garante a reprodução contínua inicializando e carregando a próxima topologia antes que a sessão de mídia comece a reproduzir a topologia atual.</span><span class="sxs-lookup"><span data-stu-id="d0d97-107">The sequencer source ensures seamless playback by initializing and loading the next topology before the Media Session starts playing the current topology.</span></span> <span data-ttu-id="d0d97-108">Isso permite que o aplicativo inicie a próxima topologia rapidamente sempre que for necessário.</span><span class="sxs-lookup"><span data-stu-id="d0d97-108">This enables the application to start the next topology quickly whenever it is required.</span></span>

<span data-ttu-id="d0d97-109">A sessão de mídia é responsável por alimentar dados para os coletores e reproduzir as topologias na origem da sequência.</span><span class="sxs-lookup"><span data-stu-id="d0d97-109">The Media Session is responsible for feeding data to the sinks and playing the topologies in the sequence source.</span></span> <span data-ttu-id="d0d97-110">Além disso, a sessão de mídia gerencia o tempo de apresentação dos segmentos.</span><span class="sxs-lookup"><span data-stu-id="d0d97-110">In addition, the Media Session manages the presentation time for the segments.</span></span>

<span data-ttu-id="d0d97-111">Para obter mais informações sobre como a origem do Sequencer gerencia topologias, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-111">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="d0d97-112">Este passo a passo contém as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d0d97-112">This walk-through contains the following steps:</span></span>

1.  [<span data-ttu-id="d0d97-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d0d97-113">Prerequisites</span></span>](#prerequisites)
2.  [<span data-ttu-id="d0d97-114">Inicializando Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0d97-114">Initializing Media Foundation</span></span>](#initializing-media-foundation)
3.  [<span data-ttu-id="d0d97-115">Criando objetos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0d97-115">Creating Media Foundation Objects</span></span>](#creating-media-foundation-objects)
4.  [<span data-ttu-id="d0d97-116">Criando a origem da mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-116">Creating the Media Source</span></span>](#creating-the-media-source)
5.  [<span data-ttu-id="d0d97-117">Criando topologias parciais</span><span class="sxs-lookup"><span data-stu-id="d0d97-117">Creating Partial Topologies</span></span>](#creating-partial-topologies)
6.  [<span data-ttu-id="d0d97-118">Adicionando topologias à origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="d0d97-118">Adding Topologies to the Sequencer Source</span></span>](#adding-topologies-to-the-sequencer-source)
7.  [<span data-ttu-id="d0d97-119">Definindo a primeira topologia na sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-119">Setting the First Topology on the Media Session</span></span>](#setting-the-first-topology-on-the-media-session)
8.  [<span data-ttu-id="d0d97-120">Enfileirando a próxima topologia na sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-120">Queuing the Next Topology on the Media Session</span></span>](#queuing-the-next-topology-on-the-media-session)
9.  [<span data-ttu-id="d0d97-121">Liberando a origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="d0d97-121">Releasing the Sequencer Source</span></span>](#releasing-the-sequencer-source)

<span data-ttu-id="d0d97-122">Os exemplos de código mostrados neste tópico são trechos do [código de exemplo de origem do sequenciador](sequencer-source-example-code.md)de tópico, que contém o código de exemplo completo.</span><span class="sxs-lookup"><span data-stu-id="d0d97-122">The code examples shown this topic are excerpts from the topic [Sequencer Source Example Code](sequencer-source-example-code.md), which contains the complete example code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d0d97-123">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="d0d97-123">Prerequisites</span></span>

<span data-ttu-id="d0d97-124">Antes de iniciar este passo a passo, familiarize-se com os seguintes conceitos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="d0d97-124">Before starting this walk-through, familiarize yourself with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="d0d97-125">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-125">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="d0d97-126">Topologias</span><span class="sxs-lookup"><span data-stu-id="d0d97-126">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="d0d97-127">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-127">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="d0d97-128">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="d0d97-128">Presentation Descriptors</span></span>](presentation-descriptors.md)

<span data-ttu-id="d0d97-129">Leia também [como reproduzir arquivos de mídia com Media Foundation](how-to-play-unprotected-media-files.md), pois o código de exemplo shwon aqui se expande no código desse tópico.</span><span class="sxs-lookup"><span data-stu-id="d0d97-129">Also read [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), because the example code shwon here expands on the code in that topic.</span></span>

## <a name="initializing-media-foundation"></a><span data-ttu-id="d0d97-130">Inicializando Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0d97-130">Initializing Media Foundation</span></span>

<span data-ttu-id="d0d97-131">Antes de poder usar qualquer Media Foundation interfaces ou métodos, inicialize Media Foundation chamando a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-131">Before you can use any Media Foundation interfaces or methods, initialize Media Foundation by calling the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="d0d97-132">Para obter mais informações, consulte [inicializando Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-132">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a><span data-ttu-id="d0d97-133">Criando objetos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0d97-133">Creating Media Foundation Objects</span></span>

<span data-ttu-id="d0d97-134">Em seguida, crie os seguintes objetos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="d0d97-134">Next, create the following Media Foundation objects:</span></span>

-   <span data-ttu-id="d0d97-135">Sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-135">Media session.</span></span> <span data-ttu-id="d0d97-136">Esse objeto expõe a interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) , que fornece métodos para reproduzir, pausar e parar a topologia atual.</span><span class="sxs-lookup"><span data-stu-id="d0d97-136">This object exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface, which provides methods to play, pause, and stop the current topology.</span></span>
-   <span data-ttu-id="d0d97-137">Origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="d0d97-137">Sequencer source.</span></span> <span data-ttu-id="d0d97-138">Esse objeto expõe a interface [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) , que fornece métodos para adicionar, atualizar e excluir topologias em uma sequência.</span><span class="sxs-lookup"><span data-stu-id="d0d97-138">This object exposes the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface, which provides methods to add, update, and delete topologies in a sequence.</span></span>

1.  <span data-ttu-id="d0d97-139">Chame a função [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-139">Call the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function to create the Media Session.</span></span>
2.  <span data-ttu-id="d0d97-140">Chame [**IMFMediaEventQueue:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) para solicitar o primeiro evento da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-140">Call [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) to request the first event from the Media Session.</span></span>
3.  <span data-ttu-id="d0d97-141">Chame a função [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) para criar a origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="d0d97-141">Call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function to create the sequencer source.</span></span>

<span data-ttu-id="d0d97-142">O código a seguir cria a sessão de mídia e solicita o primeiro evento:</span><span class="sxs-lookup"><span data-stu-id="d0d97-142">The following code creates the Media Session and requests the first event:</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a><span data-ttu-id="d0d97-143">Criando a origem da mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-143">Creating the Media Source</span></span>

<span data-ttu-id="d0d97-144">Em seguida, crie uma fonte de mídia para o primeiro segmento de playlist.</span><span class="sxs-lookup"><span data-stu-id="d0d97-144">Next, create a media source for the first playlist segment.</span></span> <span data-ttu-id="d0d97-145">Use o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia a partir de uma URL.</span><span class="sxs-lookup"><span data-stu-id="d0d97-145">Use the [Source Resolver](source-resolver.md) to create a media source from a URL.</span></span> <span data-ttu-id="d0d97-146">Para fazer isso, chame a função [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) para criar um resolvedor de origem e, em seguida, chame o método [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) para criar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-146">To do this, call the [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) function to create a source resolver and then call the [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method to create the media source.</span></span>

<span data-ttu-id="d0d97-147">Para obter informações sobre fontes de mídia, consulte [fontes de mídia](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-147">For information about media sources, see [Media Sources](media-sources.md).</span></span>

## <a name="creating-partial-topologies"></a><span data-ttu-id="d0d97-148">Criando topologias parciais</span><span class="sxs-lookup"><span data-stu-id="d0d97-148">Creating Partial Topologies</span></span>

<span data-ttu-id="d0d97-149">Cada segmento na origem do sequenciador tem sua própria topologia parcial.</span><span class="sxs-lookup"><span data-stu-id="d0d97-149">Each segment in the sequencer source has its own partial topology.</span></span> <span data-ttu-id="d0d97-150">Em seguida, crie topologias parciais para fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-150">Next, create partial topologies for media sources.</span></span> <span data-ttu-id="d0d97-151">Para uma topologia parcial, os nós de origem da topologia são conectados diretamente aos nós de saída, sem especificar transformações intermediárias.</span><span class="sxs-lookup"><span data-stu-id="d0d97-151">For a partial topology, the topology source nodes are connected directly to the output nodes, without specifying any intermediate transforms.</span></span> <span data-ttu-id="d0d97-152">A sessão de mídia usa o objeto de carregador de topologia para resolver a topologia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-152">The Media Session uses the topology loader object to resolve the topology.</span></span> <span data-ttu-id="d0d97-153">Depois que uma topologia é resolvida, os decodificadores necessários e outros nós de transformação são adicionados.</span><span class="sxs-lookup"><span data-stu-id="d0d97-153">After a topology is resolved, the required decoders and other transform nodes are added.</span></span> <span data-ttu-id="d0d97-154">A origem do sequenciador também pode conter topologias completas.</span><span class="sxs-lookup"><span data-stu-id="d0d97-154">The sequencer source can also contain full topologies.</span></span>

<span data-ttu-id="d0d97-155">Para criar o objeto de topologia, use a função [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) e, em seguida, use a interface [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) para criar nós de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d0d97-155">To create the topology object, use the [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) function and then use the [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface to create stream nodes.</span></span>

<span data-ttu-id="d0d97-156">Para obter instruções completas sobre como usar esses elementos de programação para criar topologias, consulte [criando topologias de reprodução](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-156">For complete instructions on using these programming elements to create topologies, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="d0d97-157">Um aplicativo pode reproduzir uma parte selecionada da fonte nativa Configurando o nó de origem.</span><span class="sxs-lookup"><span data-stu-id="d0d97-157">An application can play a selected portion of the native source by configuring the source node.</span></span> <span data-ttu-id="d0d97-158">Para fazer isso, defina o atributo [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) e o atributo [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) na topologia MF nós de topologia de **\_ \_ \_ nó SOURCESTREAM** .</span><span class="sxs-lookup"><span data-stu-id="d0d97-158">To do this, set the [**MF\_TOPONODE\_MEDIASTART**](mf-toponode-mediastart-attribute.md) attribute and the [**MF\_TOPONODE\_MEDIASTOP**](mf-toponode-mediastop-attribute.md) attribute on **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** topology nodes.</span></span> <span data-ttu-id="d0d97-159">Especifique a hora de início da mídia e a hora de parada da mídia em relação ao início da origem nativa como tipos de **UINT64** .</span><span class="sxs-lookup"><span data-stu-id="d0d97-159">Specify the media start time and the media stop time relative to the start of the native source as **UINT64** types.</span></span>

## <a name="adding-topologies-to-the-sequencer-source"></a><span data-ttu-id="d0d97-160">Adicionando topologias à origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="d0d97-160">Adding Topologies to the Sequencer Source</span></span>

<span data-ttu-id="d0d97-161">Em seguida, adicione à origem do Sequencer as topologias parciais que você criou.</span><span class="sxs-lookup"><span data-stu-id="d0d97-161">Next, add to the sequencer source the partial topologies that you created.</span></span> <span data-ttu-id="d0d97-162">Cada elemento Sequence, chamado *Segment*, é atribuído a um identificador **MFSequencerElementId** .</span><span class="sxs-lookup"><span data-stu-id="d0d97-162">Each sequence element, called a *segment*, is assigned an **MFSequencerElementId** identifier.</span></span> <span data-ttu-id="d0d97-163">Para obter mais informações sobre como a origem do Sequencer gerencia topologias, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-163">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="d0d97-164">Depois que todas as topologias são adicionadas à origem do sequenciador, o aplicativo deve sinalizar o último segmento na sequência para encerrar a reprodução no pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0d97-164">After all of the topologies are added to the sequencer source, the application must flag the last segment in the sequence to end playback in the pipeline.</span></span> <span data-ttu-id="d0d97-165">Sem esse sinalizador, a origem do sequenciador espera que mais topologias sejam adicionadas.</span><span class="sxs-lookup"><span data-stu-id="d0d97-165">Without this flag, the sequencer source expects more topologies to be added.</span></span>

1.  <span data-ttu-id="d0d97-166">Chame o método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) para adicionar uma topologia específica à origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="d0d97-166">Call the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method to add a specific topology to the sequencer source.</span></span>

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    <span data-ttu-id="d0d97-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adiciona a topologia especificada à sequência.</span><span class="sxs-lookup"><span data-stu-id="d0d97-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adds the specified topology to the sequence.</span></span> <span data-ttu-id="d0d97-168">Esse método retorna o identificador de segmento no parâmetro *pdwId* .</span><span class="sxs-lookup"><span data-stu-id="d0d97-168">This method returns the segment identifier in the *pdwId* parameter.</span></span>

    <span data-ttu-id="d0d97-169">Se a topologia for a última na origem do sequenciador, passe SequencerTopologyFlags \_ por último no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="d0d97-169">If the topology is the last one in the sequencer source, pass SequencerTopologyFlags\_Last in the *dwFlags* parameter.</span></span> <span data-ttu-id="d0d97-170">Esse valor é definido na enumeração [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-170">This value is defined in the [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) enumeration.</span></span>

2.  <span data-ttu-id="d0d97-171">Chame [**IMFSequencerSource:: UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) para atualizar os sinalizadores para a topologia associada ao identificador de segmento na lista de entrada.</span><span class="sxs-lookup"><span data-stu-id="d0d97-171">Call [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) to update the flags for the topology associated with the segment identifier in the input list.</span></span> <span data-ttu-id="d0d97-172">Nesse caso, a chamada indica que o segmento especificado é o último segmento no Sequencer.</span><span class="sxs-lookup"><span data-stu-id="d0d97-172">In this case, the call indicates that the specified segment is the last segment in the sequencer.</span></span> <span data-ttu-id="d0d97-173">(Essa chamada será opcional se a última topologia for especificada na chamada [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) .)</span><span class="sxs-lookup"><span data-stu-id="d0d97-173">(This call is optional if the last topology is specified in the [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) call.)</span></span>

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

<span data-ttu-id="d0d97-174">O aplicativo pode substituir a topologia de um segmento por outra topologia chamando o [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) e passando a nova topologia em *pTopology*.</span><span class="sxs-lookup"><span data-stu-id="d0d97-174">The application can replace a segment's topology with another topology by calling the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) and passing the new topology in *pTopology*.</span></span> <span data-ttu-id="d0d97-175">Se houver novas fontes nativas na nova topologia, as fontes serão adicionadas ao cache de origem.</span><span class="sxs-lookup"><span data-stu-id="d0d97-175">If there are new native sources in the new topology, the sources are added to the source cache.</span></span> <span data-ttu-id="d0d97-176">A lista de preversão também é atualizada.</span><span class="sxs-lookup"><span data-stu-id="d0d97-176">The preroll list is also refreshed.</span></span>

## <a name="setting-the-first-topology-on-the-media-session"></a><span data-ttu-id="d0d97-177">Definindo a primeira topologia na sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-177">Setting the First Topology on the Media Session</span></span>

<span data-ttu-id="d0d97-178">Em seguida, enfileirar a primeira topologia na origem da sequência na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-178">Next, queue the first topology in the sequence source on the Media Session.</span></span> <span data-ttu-id="d0d97-179">Para obter a primeira topologia da origem do Sequencer, o aplicativo deve chamar o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-179">To get the first topology from the sequencer source, the application must call the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="d0d97-180">Esse método retorna a topologia parcial, que é resolvida pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-180">This method returns the partial topology, which is resolved by the Media Session.</span></span>

<span data-ttu-id="d0d97-181">Para obter informações sobre topologias parciais, consulte [about topologias](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-181">For information about partial topologies, see [About Topologies](about-topologies.md).</span></span>

1.  <span data-ttu-id="d0d97-182">Recupere a origem de mídia nativa para a primeira topologia da origem da sequência.</span><span class="sxs-lookup"><span data-stu-id="d0d97-182">Retrieve the native media source for the first topology of the sequence source.</span></span>
2.  <span data-ttu-id="d0d97-183">Crie um descritor de apresentação para a origem da mídia chamando o método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-183">Create a presentation descriptor for the media source by calling the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>
3.  <span data-ttu-id="d0d97-184">Recupere a topologia associada para a apresentação chamando o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-184">Retrieve the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
4.  <span data-ttu-id="d0d97-185">Defina a primeira topologia na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="d0d97-185">Set the first topology on the Media Session by Calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

    <span data-ttu-id="d0d97-186">Chame [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) com o parâmetro *DwSetTopologyFlags* definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d0d97-186">Call [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the *dwSetTopologyFlags* parameter set to **NULL**.</span></span> <span data-ttu-id="d0d97-187">Isso instrui a sessão de mídia a iniciar a topologia especificada quando a topologia atual for concluída.</span><span class="sxs-lookup"><span data-stu-id="d0d97-187">This instructs the Media Session to start the specified topology when the current topology has been completed.</span></span> <span data-ttu-id="d0d97-188">Como nesse caso, a topologia especificada é a primeira topologia e não há apresentação atual, a sessão de mídia inicia a nova apresentação imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d0d97-188">Because in this case, the specified topology is the first topology and there is no current presentation, the Media Session starts the new presentation immediately.</span></span>

    <span data-ttu-id="d0d97-189">O valor **nulo** também indica que a sessão de mídia deve resolver a topologia porque a topologia retornada pelo provedor de topologia é sempre uma topologia parcial.</span><span class="sxs-lookup"><span data-stu-id="d0d97-189">The **NULL** value also indicates that Media Session must resolve the topology because the topology returned by the topology provider is always a partial topology.</span></span>


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



## <a name="queuing-the-next-topology-on-the-media-session"></a><span data-ttu-id="d0d97-190">Enfileirando a próxima topologia na sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="d0d97-190">Queuing the Next Topology on the Media Session</span></span>

<span data-ttu-id="d0d97-191">Em seguida, o aplicativo precisa manipular o evento [MENewPresentation](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-191">Next, the application needs to handle the [MENewPresentation](menewpresentation.md) event.</span></span>

<span data-ttu-id="d0d97-192">A origem do Sequencer gera [MENewPresentation](menewpresentation.md) quando a sessão de mídia começa a reproduzir um segmento que tem outro segmento após ele.</span><span class="sxs-lookup"><span data-stu-id="d0d97-192">Sequencer source raises [MENewPresentation](menewpresentation.md) when the Media Session starts playing a segment that has another segment following it.</span></span> <span data-ttu-id="d0d97-193">Esse evento informa o aplicativo sobre a próxima topologia na origem da sequência, fornecendo o descritor de apresentação para o próximo segmento na lista de preversão.</span><span class="sxs-lookup"><span data-stu-id="d0d97-193">This event informs the application about the next topology in the sequence source by providing the presentation descriptor for the next segment in the preroll list.</span></span> <span data-ttu-id="d0d97-194">O aplicativo deve recuperar a topologia associada, usando o provedor de topologia e enfileirando-a na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-194">The application must retrieve the associated topology, by using the topology provider, and queue it on the Media Session.</span></span> <span data-ttu-id="d0d97-195">Em seguida, a origem do Sequencer então reverte essa topologia, o que garante uma transição tranqüila entre as apresentações.</span><span class="sxs-lookup"><span data-stu-id="d0d97-195">The sequencer source then prerolls this topology, which ensures a seamless transition between presentations.</span></span>

<span data-ttu-id="d0d97-196">Quando o aplicativo busca em segmentos, o aplicativo recebe vários eventos [MENewPresentation](menewpresentation.md) , pois a origem do sequenciador atualiza a lista de preversão e configura a topologia correta.</span><span class="sxs-lookup"><span data-stu-id="d0d97-196">When the application seeks across segments, the application receives several [MENewPresentation](menewpresentation.md) events as the sequencer source refreshes the preroll list and sets up the correct topology.</span></span> <span data-ttu-id="d0d97-197">O aplicativo deve tratar cada evento e enfileirar a topologia retornada nos dados do evento, na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="d0d97-197">The application must handle each event and queue the topology returned in the event data, on the Media Session.</span></span> <span data-ttu-id="d0d97-198">Para obter informações sobre como ignorar segmentos, consulte [usando a origem do sequenciador](using-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-198">For information about skipping segments, see [Using the Sequencer Source](using-the-sequencer-source.md).</span></span>

<span data-ttu-id="d0d97-199">Para obter informações sobre como obter notificações de origem do Sequencer, consulte [eventos de origem do Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="d0d97-199">For information about getting sequencer source notifications, see [Sequencer Source Events](sequencer-source-events.md).</span></span>

1.  <span data-ttu-id="d0d97-200">No manipulador de eventos [MENewPresentation](menewpresentation.md) , recupere o descritor de apresentação para o próximo segmento dos dados de evento.</span><span class="sxs-lookup"><span data-stu-id="d0d97-200">In the [MENewPresentation](menewpresentation.md) event handler, retrieve the presentation descriptor for the next segment from the event data.</span></span>
2.  <span data-ttu-id="d0d97-201">Obtenha a topologia associada para a apresentação chamando o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-201">Get the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
3.  <span data-ttu-id="d0d97-202">Defina a topologia na sessão de mídia chamando o método [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) .</span><span class="sxs-lookup"><span data-stu-id="d0d97-202">Set the topology on the Media Session by calling the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>

    <span data-ttu-id="d0d97-203">A sessão de mídia inicia a nova apresentação quando a apresentação atual é concluída.</span><span class="sxs-lookup"><span data-stu-id="d0d97-203">The Media Session starts the new presentation when the current presentation has been completed.</span></span>


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a><span data-ttu-id="d0d97-204">Liberando a origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="d0d97-204">Releasing the Sequencer Source</span></span>

<span data-ttu-id="d0d97-205">Por fim, desligue a origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="d0d97-205">Finally, shut down the sequencer source.</span></span> <span data-ttu-id="d0d97-206">Para fazer isso, chame o método [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) na origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="d0d97-206">To do so, call the [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) method on the sequencer source.</span></span> <span data-ttu-id="d0d97-207">Essa chamada desliga todas as fontes de mídia nativas subjacentes na origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="d0d97-207">This call shuts down all of the underlying native media sources in the sequencer source.</span></span>

<span data-ttu-id="d0d97-208">Depois de liberar a origem do sequenciador, o aplicativo deve fechar e desligar a sessão de mídia chamando [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) e [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), nessa ordem.</span><span class="sxs-lookup"><span data-stu-id="d0d97-208">After releasing the sequencer source, the application should close and shut down the Media Session by calling [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) and [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in that order.</span></span>

<span data-ttu-id="d0d97-209">Para evitar vazamentos de memória, o aplicativo deve liberar ponteiros para Media Foundation interfaces quando eles não forem mais necessários.</span><span class="sxs-lookup"><span data-stu-id="d0d97-209">To avoid memory leaks, the application must release pointers to Media Foundation interfaces when they are no longer needed.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d0d97-210">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="d0d97-210">Next Steps</span></span>

<span data-ttu-id="d0d97-211">Este guia passo a passo ilustra como criar uma lista de reprodução básica usando a origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="d0d97-211">This walk-through illustrated how to create a basic playlist by using the sequencer source.</span></span> <span data-ttu-id="d0d97-212">Depois de criar a lista de reprodução, talvez você queira adicionar recursos avançados, como ignorar o segmento, alterar o estado de reprodução e procurar dentro de um segmento.</span><span class="sxs-lookup"><span data-stu-id="d0d97-212">After creating the playlist, you might want to add advanced features such as segment skipping, changing the playback state, and seeking within a segment.</span></span> <span data-ttu-id="d0d97-213">A lista a seguir fornece links para os tópicos relacionados:</span><span class="sxs-lookup"><span data-stu-id="d0d97-213">The following list provides links to the related topics:</span></span>

-   <span data-ttu-id="d0d97-214">[Como controlar os Estados de apresentação](how-to-control-presentation-states.md): a origem do sequenciador depende da sessão de mídia para fornecer controle de transporte como, reproduzir, pausar e parar.</span><span class="sxs-lookup"><span data-stu-id="d0d97-214">[How to Control Presentation States](how-to-control-presentation-states.md): The sequencer source relies on the Media Session to provide transport control such as, Play, Pause, and Stop.</span></span>
-   <span data-ttu-id="d0d97-215">[Como executar a depuração](how-to-perform-scrubbing.md) descreve as etapas necessárias para buscar uma posição específica em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="d0d97-215">[How to Perform Scrubbing](how-to-perform-scrubbing.md) describes the steps required to seek to a specific position in a stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0d97-216">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0d97-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0d97-217">Origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="d0d97-217">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



