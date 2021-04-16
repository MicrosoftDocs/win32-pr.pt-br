---
description: Este tópico descreve como usar a origem do Sequencer.
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: Usando a origem do sequenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765330"
---
# <a name="using-the-sequencer-source"></a><span data-ttu-id="573b1-103">Usando a origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="573b1-103">Using the Sequencer Source</span></span>

<span data-ttu-id="573b1-104">Este tópico descreve como usar a [origem do Sequencer](sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="573b1-104">This topic describes how to use the [Sequencer Source](sequencer-source.md).</span></span> <span data-ttu-id="573b1-105">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="573b1-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="573b1-106">Visão geral</span><span class="sxs-lookup"><span data-stu-id="573b1-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="573b1-107">Adicionando topologias</span><span class="sxs-lookup"><span data-stu-id="573b1-107">Adding Topologies</span></span>](#adding-topologies)
-   [<span data-ttu-id="573b1-108">Excluindo topologias</span><span class="sxs-lookup"><span data-stu-id="573b1-108">Deleting Topologies</span></span>](#deleting-topologies)
-   [<span data-ttu-id="573b1-109">Ignorando para um segmento</span><span class="sxs-lookup"><span data-stu-id="573b1-109">Skipping to a Segment</span></span>](#skipping-to-a-segment)
-   [<span data-ttu-id="573b1-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="573b1-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="573b1-111">Para obter uma visão geral da origem do sequenciador, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="573b1-111">For a general overview of the sequencer source, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

## <a name="overview"></a><span data-ttu-id="573b1-112">Visão geral</span><span class="sxs-lookup"><span data-stu-id="573b1-112">Overview</span></span>

<span data-ttu-id="573b1-113">A origem do sequenciador expõe as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="573b1-113">The sequencer source exposes the following interfaces.</span></span>



| <span data-ttu-id="573b1-114">Interface</span><span class="sxs-lookup"><span data-stu-id="573b1-114">Interface</span></span>                                                                        | <span data-ttu-id="573b1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="573b1-115">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="573b1-116">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="573b1-116">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | <span data-ttu-id="573b1-117">Expõe a funcionalidade de origem de mídia genérica.</span><span class="sxs-lookup"><span data-stu-id="573b1-117">Exposes generic media source functionality.</span></span>                                        |
| [<span data-ttu-id="573b1-118">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="573b1-118">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | <span data-ttu-id="573b1-119">Permite que o aplicativo adicione ou remova topologias.</span><span class="sxs-lookup"><span data-stu-id="573b1-119">Enables the application to add or remove topologies.</span></span>                               |
| [<span data-ttu-id="573b1-120">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="573b1-120">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | <span data-ttu-id="573b1-121">Recupera a próxima topologia a ser enfileirada na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="573b1-121">Retrieves the next topology to queue on the Media Session.</span></span>                         |
| [<span data-ttu-id="573b1-122">**IMFMediaSourcePresentationProvider**</span><span class="sxs-lookup"><span data-stu-id="573b1-122">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | <span data-ttu-id="573b1-123">Usado pela sessão de mídia para segmentos finais.</span><span class="sxs-lookup"><span data-stu-id="573b1-123">Used by the Media Session to end segments.</span></span> <span data-ttu-id="573b1-124">Os aplicativos não usam essa interface.</span><span class="sxs-lookup"><span data-stu-id="573b1-124">Applications do not use this interface.</span></span> |
| [<span data-ttu-id="573b1-125">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="573b1-125">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | <span data-ttu-id="573b1-126">Consulta a origem do sequenciador para [interfaces de serviço](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="573b1-126">Queries the sequencer source for [Service Interfaces](service-interfaces.md).</span></span>     |



 

<span data-ttu-id="573b1-127">Para reproduzir uma sequência de fontes de mídia, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="573b1-127">To play a sequence of media sources, perform the following steps:</span></span>

1.  <span data-ttu-id="573b1-128">Para criar a origem do sequenciador, chame a função [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) .</span><span class="sxs-lookup"><span data-stu-id="573b1-128">To create the sequencer source, call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function.</span></span>
2.  <span data-ttu-id="573b1-129">Para cada segmento, crie uma topologia de reprodução, conforme descrito em [criando topologias de reprodução](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="573b1-129">For each segment, create a playback topology, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="573b1-130">Para adicionar a topologia à apresentação, chame [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="573b1-130">To add the topology to the presentation, call [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span>
3.  <span data-ttu-id="573b1-131">Antes de iniciar a reprodução, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="573b1-131">Before starting playback, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the sequencer source.</span></span> <span data-ttu-id="573b1-132">Esse método retorna um ponteiro para um descritor de apresentação para o primeiro segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-132">This method returns a pointer to a presentation descriptor for the first segment.</span></span> <span data-ttu-id="573b1-133">Para obter a topologia associada a esse segmento, chame **QueryInterface** na origem do sequenciador para a interface [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) .</span><span class="sxs-lookup"><span data-stu-id="573b1-133">To get the topology associated with this segment, call **QueryInterface** on the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span> <span data-ttu-id="573b1-134">Passe o descritor de apresentação para o método [**IMFMediaSourceTopologyProvider:: GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) .</span><span class="sxs-lookup"><span data-stu-id="573b1-134">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="573b1-135">Esse método retorna um ponteiro para a topologia.</span><span class="sxs-lookup"><span data-stu-id="573b1-135">This method returns a pointer to the topology.</span></span>
4.  <span data-ttu-id="573b1-136">Passe a topologia do primeiro segmento para a sessão de mídia chamando o método [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="573b1-136">Pass the topology for the first segment to the Media Session, by calling the Media Session's [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>
5.  <span data-ttu-id="573b1-137">Inicie a reprodução chamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="573b1-137">Start playback by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>
6.  <span data-ttu-id="573b1-138">Quando a origem do sequenciador está pronta para lançar o próximo segmento, ele envia um evento [MENewPresentation](menewpresentation.md) cujos dados de evento são um ponteiro de interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="573b1-138">When the sequencer source is ready to preroll the next segment, it sends an [MENewPresentation](menewpresentation.md) event whose event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface pointer.</span></span> <span data-ttu-id="573b1-139">Novamente, obtenha a topologia para o segmento chamando [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) na origem do sequenciador e defina a topologia na sessão de mídia chamando [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="573b1-139">Again, get the topology for the segment by calling [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the sequencer source, and set the topology on the Media Session by calling [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="573b1-140">Não é necessário reiniciar a origem da mídia; Ele passará automaticamente para o próximo segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-140">It is not necessary to re-start the media source; it will automatically play through to the next segment.</span></span>
7.  <span data-ttu-id="573b1-141">Antes de o aplicativo sair, desligue a origem do sequenciador chamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="573b1-141">Before the application quits, shut down the sequencer source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>

<span data-ttu-id="573b1-142">O código a seguir mostra como obter a topologia e defini-la na sessão de mídia:</span><span class="sxs-lookup"><span data-stu-id="573b1-142">The following code shows how to get the topology and set it on the Media Session:</span></span>


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



<span data-ttu-id="573b1-143">Para obter um exemplo de código completo, consulte [código de exemplo de origem do Sequencer](sequencer-source-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="573b1-143">For a complete code example, see [Sequencer Source Example Code](sequencer-source-example-code.md).</span></span>

## <a name="adding-topologies"></a><span data-ttu-id="573b1-144">Adicionando topologias</span><span class="sxs-lookup"><span data-stu-id="573b1-144">Adding Topologies</span></span>

<span data-ttu-id="573b1-145">A origem do sequenciador mantém duas listas de topologias: a *lista de entrada* e a *lista de preversão*.</span><span class="sxs-lookup"><span data-stu-id="573b1-145">The sequencer source maintains two lists of topologies: the *input list* and the *preroll list*.</span></span>

<span data-ttu-id="573b1-146">A lista de entrada é uma coleção de topologias correspondentes aos segmentos de playlist, na ordem em que foram adicionadas pelo aplicativo chamando [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span><span class="sxs-lookup"><span data-stu-id="573b1-146">The input list is a collection of topologies corresponding to playlist segments, in the order that they were added by the application by calling [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span> <span data-ttu-id="573b1-147">Esse método atribui a cada topologia um identificador de *segmento* exclusivo do tipo **MFSequencerElementId**.</span><span class="sxs-lookup"><span data-stu-id="573b1-147">This method assigns each topology a unique *segment identifier* of the type **MFSequencerElementId**.</span></span> <span data-ttu-id="573b1-148">O identificador de segmento é definido como um atributo para todos os nós de topologia de origem.</span><span class="sxs-lookup"><span data-stu-id="573b1-148">The segment identifier is set as an attribute for all source topology nodes.</span></span> <span data-ttu-id="573b1-149">Um aplicativo pode obter o identificador de segmento a partir de um nó de origem usando o atributo [MF \_ TOPONODE \_ Sequence \_ ElementID](mf-toponode-sequence-elementid-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="573b1-149">An application can get the segment identifier from a source node by using the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute.</span></span> <span data-ttu-id="573b1-150">A lista de entrada pode ter topologias duplicadas se o aplicativo chamou **AppendTopology** na mesma topologia mais de uma vez; no entanto, elas são identificadas por seus identificadores de segmento exclusivos.</span><span class="sxs-lookup"><span data-stu-id="573b1-150">The input list can have duplicate topologies if the application called **AppendTopology** on the same topology more than once; however, they are identified by their unique segment identifiers.</span></span>

<span data-ttu-id="573b1-151">A lista de preversão é uma coleção de topologias de lista de entrada que foram inicializadas na preparação para reprodução.</span><span class="sxs-lookup"><span data-stu-id="573b1-151">The preroll list is a collection of input list topologies that have been initialized in preparation for playback.</span></span> <span data-ttu-id="573b1-152">Isso permite que a sessão de mídia seja transferida para a próxima topologia diretamente quando a topologia ativa termina.</span><span class="sxs-lookup"><span data-stu-id="573b1-152">This enables the Media Session to transition to the next topology seamlessly when the active topology ends.</span></span> <span data-ttu-id="573b1-153">O aplicativo não pode adicionar ou remover topologias diretamente da lista de preversão; Ele é gerado pela origem do sequenciador quando uma topologia da lista de entrada é selecionada para reprodução.</span><span class="sxs-lookup"><span data-stu-id="573b1-153">The application cannot directly add or remove topologies from the preroll list; it is generated by the sequencer source when a topology from the input list is selected for playback.</span></span> <span data-ttu-id="573b1-154">Isso faz com que a origem do sequenciador adicione a próxima topologia da lista de entrada à lista de preversão.</span><span class="sxs-lookup"><span data-stu-id="573b1-154">This causes the sequencer source to add the next topology from the input list to the preroll list.</span></span> <span data-ttu-id="573b1-155">Depois de fazer isso, a origem do Sequencer gera de forma assíncrona o evento [MENewPresentation](menewpresentation.md) e passa o descritor de apresentação para a topologia de preversão como dados de evento.</span><span class="sxs-lookup"><span data-stu-id="573b1-155">After doing so, the sequencer source asynchronously raises the [MENewPresentation](menewpresentation.md) event and passes the presentation descriptor for the preroll topology as event data.</span></span> <span data-ttu-id="573b1-156">O aplicativo deve escutar esse evento usando a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da sessão de mídia e enfileirar a topologia de preversão na sessão de mídia chamando [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="573b1-156">The application must listen for this event by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface and queue the preroll topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="573b1-157">Isso deve ser feito antes que a sessão de mídia conclua a reprodução da topologia ativa.</span><span class="sxs-lookup"><span data-stu-id="573b1-157">This must be done before the Media Session completes playback of the active topology.</span></span> <span data-ttu-id="573b1-158">**Settopology** informa a sessão de mídia sobre a próxima topologia que ela deve reproduzir após o término da reprodução da topologia ativa.</span><span class="sxs-lookup"><span data-stu-id="573b1-158">**SetTopology** informs the Media Session about the next topology that it must play after playback of the active topology has ended.</span></span> <span data-ttu-id="573b1-159">Para garantir um treansition contínuo, o aplicativo deve chamar **settopology** antes que a sessão de mídia conclua a execução da topologia anterior.</span><span class="sxs-lookup"><span data-stu-id="573b1-159">To ensure a seamless treansition, the application must call **SetTopology** before the Media Session completes playing the previous topology.</span></span> <span data-ttu-id="573b1-160">Caso contrário, haverá uma lacuna entre os segmentos.</span><span class="sxs-lookup"><span data-stu-id="573b1-160">Otherwise, there will be a gap between the segments.</span></span>

<span data-ttu-id="573b1-161">O evento [MENewPresentation](menewpresentation.md) é gerado contanto que haja uma topologia após a topologia ativa.</span><span class="sxs-lookup"><span data-stu-id="573b1-161">The [MENewPresentation](menewpresentation.md) event is raised as long as there is a topology following the active topology.</span></span> <span data-ttu-id="573b1-162">Consequentemente, se a lista de entrada contiver apenas uma topologia ou se a topologia ativa for a última na lista de entrada, esse evento não será gerado.</span><span class="sxs-lookup"><span data-stu-id="573b1-162">Consequently, if the input list contains only one topology, or if the active topology is the last one in the input list, this event is not raised.</span></span>

<span data-ttu-id="573b1-163">A lista de preversão é sincronizada com a lista de entrada e é atualizada toda vez que uma topologia é adicionada ou excluída da lista de entrada.</span><span class="sxs-lookup"><span data-stu-id="573b1-163">The preroll list is synchronized with the input list and is refreshed each time a topology is added to or deleted from the input list.</span></span>

## <a name="deleting-topologies"></a><span data-ttu-id="573b1-164">Excluindo topologias</span><span class="sxs-lookup"><span data-stu-id="573b1-164">Deleting Topologies</span></span>

<span data-ttu-id="573b1-165">Para remover uma topologia da origem do Sequencer, um aplicativo deve chamar o método [**IMFSequencerSource::D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) e especificar o identificador do segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-165">To remove a topology from the sequencer source, an application must call the [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) method and specify the segment identifier.</span></span>

<span data-ttu-id="573b1-166">Antes de chamar [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), o aplicativo deve garantir que a sessão de mídia não esteja usando a topologia que o aplicativo deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="573b1-166">Before calling [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), the application must make sure that Media Session is not using the topology that the application wants to delete.</span></span> <span data-ttu-id="573b1-167">Para fazer isso, os dois itens a seguir devem ocorrer antes que o aplicativo chame **DeleteTopology**:</span><span class="sxs-lookup"><span data-stu-id="573b1-167">To do this, both of the following must occur before the application calls **DeleteTopology**:</span></span>

-   <span data-ttu-id="573b1-168">O evento [MESessionTopologyStatus](mesessiontopologystatus.md) com MF \_ TOPOSTATUS \_ encerrado é recebido para a topologia para garantir que a sessão de mídia concluiu a reprodução.</span><span class="sxs-lookup"><span data-stu-id="573b1-168">[MESessionTopologyStatus](mesessiontopologystatus.md) event with MF\_TOPOSTATUS\_ENDED is received for the topology to ensure that Media Session has completed playback.</span></span>

-   <span data-ttu-id="573b1-169">[MESessionTopologyStatus](mesessiontopologystatus.md) com a \_ origem MF TOPOSTATUS \_ iniciada \_ é recebida para a próxima topologia para garantir que a sessão de mídia tenha iniciado a reprodução da próxima topologia, o evento [MESessionEnded](mesessionended.md) é recebido para garantir que a sessão de mídia seja feita com a última topologia na origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="573b1-169">[MESessionTopologyStatus](mesessiontopologystatus.md) with MF\_TOPOSTATUS\_STARTED\_SOURCE is received for the next topology to ensure that the Media Session has started playing the next topology, [MESessionEnded](mesessionended.md) event is received to ensure that Media Session is done with the last topology in the sequencer source.</span></span>

<span data-ttu-id="573b1-170">Se o segmento que está sendo excluído for a topologia ativa, a reprodução será interrompida e a origem do sequenciador gerará o evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="573b1-170">If the segment being deleted is the active topology, playback is stopped and the sequencer source raises the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span> <span data-ttu-id="573b1-171">Se a topologia ativa também for a última topologia, o evento [MEEndOfPresentation](meendofpresentation.md) será gerado.</span><span class="sxs-lookup"><span data-stu-id="573b1-171">If the active topology is also the last topology, the [MEEndOfPresentation](meendofpresentation.md) event is raised.</span></span>

## <a name="skipping-to-a-segment"></a><span data-ttu-id="573b1-172">Ignorando para um segmento</span><span class="sxs-lookup"><span data-stu-id="573b1-172">Skipping to a Segment</span></span>

<span data-ttu-id="573b1-173">Um aplicativo pode pular para um segmento específico na sequência iniciando a sessão de [mídia](media-session.md) com um deslocamento de segmento, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="573b1-173">An application can skip to a particular segment in the sequence by starting the [Media Session](media-session.md) with a segment offset, as follows:</span></span>

1.  <span data-ttu-id="573b1-174">Chame a função [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) para criar o deslocamento de segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-174">Call the [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) function to create the segment offset.</span></span> <span data-ttu-id="573b1-175">Especifique o identificador do segmento no parâmetro *dwID* .</span><span class="sxs-lookup"><span data-stu-id="573b1-175">Specify the identifier of the segment in the *dwId* parameter.</span></span> <span data-ttu-id="573b1-176">(O identificador foi retornado pelo método [**IMFSequencerSource:: AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) quando você adicionou pela primeira vez a topologia à origem do sequenciador.) O parâmetro *hnsOffset* especifica um deslocamento de tempo, em relação ao início do segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-176">(The identifier was returned by the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method when you first added the topology to the sequencer source.) The *hnsOffset* parameter specifies a time offset, relative to the start of the segment.</span></span> <span data-ttu-id="573b1-177">A reprodução será iniciada no momento.</span><span class="sxs-lookup"><span data-stu-id="573b1-177">Playback will start at this time.</span></span> <span data-ttu-id="573b1-178">Para o parâmetro *pvarSegmentOffset* , passe o endereço de um **PROPVARIANT** vazio.</span><span class="sxs-lookup"><span data-stu-id="573b1-178">For the *pvarSegmentOffset* parameter, pass in the address of an empty **PROPVARIANT**.</span></span> <span data-ttu-id="573b1-179">Quando a função retorna, esse **PROPVARIANT** contém o deslocamento de segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-179">When the function returns, this **PROPVARIANT** contains the segment offset.</span></span>

2.  <span data-ttu-id="573b1-180">Chame o método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="573b1-180">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method on the Media Session.</span></span> <span data-ttu-id="573b1-181">Para o parâmetro *pguidTimeFormat* , use o deslocamento de segmento do formato de tempo MF do valor do GUID \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="573b1-181">For the *pguidTimeFormat* parameter, use the GUID value MF\_TIME\_FORMAT\_SEGMENT\_OFFSET.</span></span> <span data-ttu-id="573b1-182">Esse valor indica a busca por deslocamento de segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-182">This value indicates seeking by segment offset.</span></span> <span data-ttu-id="573b1-183">Para o parâmetro *pvarStartPosition* , passe o endereço do **PROPVARIANT** criado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="573b1-183">For the *pvarStartPosition* parameter, pass the address of the **PROPVARIANT** created in the previous step.</span></span>

<span data-ttu-id="573b1-184">O exemplo de código a seguir mostra como pular para o início de um segmento especificado em uma sequência.</span><span class="sxs-lookup"><span data-stu-id="573b1-184">The following code example shows how to skip to the start of a specified segment in a sequence.</span></span>


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="573b1-185">Quando o aplicativo busca em segmentos, o aplicativo recebe vários eventos, pois a origem do sequenciador encerra o segmento atual e se prepara para reproduzir o novo segmento.</span><span class="sxs-lookup"><span data-stu-id="573b1-185">When the application seeks across segments, the application receives several events as the sequencer source ends the current segment and prepares to play the new segment.</span></span> <span data-ttu-id="573b1-186">Como esses eventos são recebidos de forma assíncrona, é difícil prever a sequência exata de eventos.</span><span class="sxs-lookup"><span data-stu-id="573b1-186">Because these events are received asynchronously, it is difficult to predict the exact sequence of events.</span></span> <span data-ttu-id="573b1-187">Esses eventos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="573b1-187">These events are as follows:</span></span>

-   <span data-ttu-id="573b1-188">A origem do sequenciador envia um evento [MENewPresentation](menewpresentation.md) para o novo segmento ao qual a sessão de mídia está sendo ignorada.</span><span class="sxs-lookup"><span data-stu-id="573b1-188">The sequencer source sends an [MENewPresentation](menewpresentation.md) event for the new segment to which the Media Session is skipping.</span></span>

-   <span data-ttu-id="573b1-189">Quando a origem do sequenciador encerra o segmento ativo, ele envia o evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="573b1-189">When the sequencer source ends the active segment, it sends the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span>
-   <span data-ttu-id="573b1-190">A origem do sequenciador, em seguida, cancela a topologia de preroll.</span><span class="sxs-lookup"><span data-stu-id="573b1-190">The sequencer source then cancels the preroll topology.</span></span> <span data-ttu-id="573b1-191">Isso resulta nos seguintes eventos para a topologia cancelada:</span><span class="sxs-lookup"><span data-stu-id="573b1-191">This results in the following events for the canceled topology:</span></span>

    -   <span data-ttu-id="573b1-192">Evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador MF TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="573b1-192">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span>
    -   <span data-ttu-id="573b1-193">Evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador de origem MF TOPOSTATUS \_ iniciado \_ .</span><span class="sxs-lookup"><span data-stu-id="573b1-193">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_STARTED\_SOURCE flag.</span></span>
    -   <span data-ttu-id="573b1-194">Evento [MEEndOfPresentationSegment](meendofpresentationsegment.md) com o atributo de [topologia de origem de evento MF \_ \_ \_ \_ cancelado](mf-event-source-topology-canceled-attribute.md) para indicar que a topologia foi cancelada pela origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="573b1-194">[MEEndOfPresentationSegment](meendofpresentationsegment.md) event with the [MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED](mf-event-source-topology-canceled-attribute.md) attribute to indicate that the topology was canceled by the sequencer source.</span></span>

-   <span data-ttu-id="573b1-195">Em seguida, a origem do sequenciador envia eventos para o novo segmento, incluindo vários eventos [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="573b1-195">Next, the sequencer source sends events for the new segment, including various [MESessionTopologyStatus](mesessiontopologystatus.md) events.</span></span>
-   <span data-ttu-id="573b1-196">Se o novo segmento não for o último na lista, a origem do sequenciador atualizará a lista de preversão e gerará outro [MENewPresentation](menewpresentation.md) para a nova topologia de preroll.</span><span class="sxs-lookup"><span data-stu-id="573b1-196">If the new segment is not the last on the list, the sequencer source refreshes the preroll list and raises another [MENewPresentation](menewpresentation.md) for the new preroll topology.</span></span> <span data-ttu-id="573b1-197">Para obter informações sobre topologias na lista de preversão, consulte [sobre a origem do sequenciador](about-the-sequencer-source.md).</span><span class="sxs-lookup"><span data-stu-id="573b1-197">For information about topologies in the preroll list, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="573b1-198">Mais detalhes sobre os eventos enviados pela origem do sequenciador podem ser encontrados no tópico [eventos de origem do Sequencer](sequencer-source-events.md).</span><span class="sxs-lookup"><span data-stu-id="573b1-198">More details about the events sent by the sequencer source can be found in the topic [Sequencer Source Events](sequencer-source-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="573b1-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="573b1-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="573b1-200">Como criar uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="573b1-200">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="573b1-201">Origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="573b1-201">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



