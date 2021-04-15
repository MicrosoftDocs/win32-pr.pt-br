---
description: Sobre a origem do sequenciador
ms.assetid: 0d7ce9ca-9f34-4842-bd49-9211ae4454de
title: Sobre a origem do sequenciador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d8de3e0ff46cab1e68b767294633ecd09ebc161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501842"
---
# <a name="about-the-sequencer-source"></a><span data-ttu-id="b7853-103">Sobre a origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="b7853-103">About the Sequencer Source</span></span>

<span data-ttu-id="b7853-104">A origem do sequenciador permite que um aplicativo reproduza uma coleção de [fontes de mídia](media-sources.md) sequencialmente, com transições diretas entre as fontes.</span><span class="sxs-lookup"><span data-stu-id="b7853-104">The sequencer source enables an application to play a collection of [Media Sources](media-sources.md) sequentially, with seamless transitions between the sources.</span></span> <span data-ttu-id="b7853-105">A origem do sequenciador pode ser usada para os seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="b7853-105">The sequencer source can be used for the following scenarios:</span></span>

-   <span data-ttu-id="b7853-106">Crie uma lista de reprodução que alterna diretamente de uma fonte de mídia para a próxima.</span><span class="sxs-lookup"><span data-stu-id="b7853-106">Create a playlist that switches seamlessly from one media source to the next.</span></span>
-   <span data-ttu-id="b7853-107">Reproduzir fluxos de várias fontes simultaneamente; por exemplo, reproduza o áudio de um arquivo com o vídeo de outro.</span><span class="sxs-lookup"><span data-stu-id="b7853-107">Play streams from multiple sources simultaneously; for example, play the audio from one file with the video from another.</span></span>
-   <span data-ttu-id="b7853-108">Alternar entre fluxos em diferentes fontes de mídia em entradas de playlist consecutivas; por exemplo, uma lista de reprodução pode ter entradas que compartilham a mesma fonte de vídeo enquanto cada entrada contém uma fonte de áudio diferente.</span><span class="sxs-lookup"><span data-stu-id="b7853-108">Switch between streams in different media sources in consecutive playlist entries; for example, a playlist can have entries that share the same video source while each entry contains a different audio source.</span></span>

<span data-ttu-id="b7853-109">Para cada elemento de uma lista de reprodução, o aplicativo cria uma topologia separada.</span><span class="sxs-lookup"><span data-stu-id="b7853-109">For each element of a playlist, the application creates a separate topology.</span></span> <span data-ttu-id="b7853-110">As fontes de mídia nessas topologias são chamadas de *Fontes nativas*, para distingui-las da origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="b7853-110">The media sources in these topologies are referred to as *native sources*, to distinguish them from the sequencer source.</span></span> <span data-ttu-id="b7853-111">Durante a reprodução, toda a sequência de topologias é chamada de *apresentação*, e cada topologia dentro da sequência é chamada de *segmento*.</span><span class="sxs-lookup"><span data-stu-id="b7853-111">During playback, the entire sequence of topologies is called a *presentation*, and each topology within the sequence is called a *segment*.</span></span>

<span data-ttu-id="b7853-112">A reprodução é controlada pela [sessão de mídia](media-session.md), que fornece controles de transporte, como reproduzir, pausar e parar.</span><span class="sxs-lookup"><span data-stu-id="b7853-112">Playback is controlled by the [Media Session](media-session.md), which provides transport controls, such as play, pause, and stop.</span></span> <span data-ttu-id="b7853-113">A sessão de mídia também gerencia o tempo de apresentação e envia eventos para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7853-113">The Media Session also manages the presentation time and sends events to the application.</span></span> <span data-ttu-id="b7853-114">(Os eventos da origem do sequenciador são encaminhados para o aplicativo por meio da sessão de mídia.)</span><span class="sxs-lookup"><span data-stu-id="b7853-114">(Events from the sequencer source are forwarded to the application through the Media Session.)</span></span>

<span data-ttu-id="b7853-115">Para criar uma lista de reprodução, o aplicativo cria uma ou mais topologias de reprodução e as enfileira na origem do sequenciador na ordem desejada de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b7853-115">To create a playlist, the application creates one or more playback topologies and queues them on the sequencer source in the desired order of playback.</span></span> <span data-ttu-id="b7853-116">Internamente, a origem do sequenciador modifica as topologias para que os nós de origem apontem para a origem do sequenciador em vez da fonte nativa.</span><span class="sxs-lookup"><span data-stu-id="b7853-116">Internally, the sequencer source modifies the topologies so that the source nodes point to the sequencer source instead of the native source.</span></span> <span data-ttu-id="b7853-117">O aplicativo envia essas topologias modificadas, em vez das topologias originais, para a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="b7853-117">The application sends these modified topologies, rather than the original topologies, to the Media Session.</span></span> <span data-ttu-id="b7853-118">Isso permite que a origem do sequenciador agregue as fontes nativas e se comunique com a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="b7853-118">This enables the sequencer source to aggregate the native sources and to communicate with the Media Session.</span></span>

<span data-ttu-id="b7853-119">Para obter transições diretas entre segmentos, a origem do sequenciador se registra em cada segmento.</span><span class="sxs-lookup"><span data-stu-id="b7853-119">To achieve seamless transitions between segments, the sequencer source prerolls each segment.</span></span> <span data-ttu-id="b7853-120">Enquanto um segmento está sendo reproduzido, e antes de ser a hora de reproduzir o segmento a seguir, a origem do sequenciador dispara um evento [MENewPresentation](menewpresentation.md) que contém um descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="b7853-120">While one segment is playing, and before it is time to play the following segment, the sequencer source fires an [MENewPresentation](menewpresentation.md) event that contains a presentation descriptor.</span></span> <span data-ttu-id="b7853-121">O aplicativo usa este descritor de apresentação para obter a topologia para o próximo segmento na apresentação e enfileira a topologia na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="b7853-121">The application uses this presentation descriptor to get the topology for the next segment in the presentation, and queues the topology on the Media Session.</span></span>

<span data-ttu-id="b7853-122">A ilustração a seguir mostra o fluxo de dados para entradas de playlist por meio da origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="b7853-122">The following illustration shows the data flow for playlist entries through the sequencer source.</span></span> <span data-ttu-id="b7853-123">O aplicativo usa o resolvedor de origem para criar as fontes nativas, cria topologias para cada segmento e enfileira as topologias na origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="b7853-123">The application uses the source resolver to create the native sources, builds topologies for each segment, and queues the topologies on the sequencer source.</span></span>

![diagrama mostrando o fluxo de dados dos segmentos imfmediasession, imfsequencersource e playlist que levam ao imfmediasource](images/dbf41a05-d8cc-4502-9cd3-74e5d1ce04a0.gif)

## <a name="related-topics"></a><span data-ttu-id="b7853-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7853-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7853-126">Como criar uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="b7853-126">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="b7853-127">Topologias</span><span class="sxs-lookup"><span data-stu-id="b7853-127">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="b7853-128">Usando a origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="b7853-128">Using the Sequencer Source</span></span>](using-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="b7853-129">Origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="b7853-129">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



