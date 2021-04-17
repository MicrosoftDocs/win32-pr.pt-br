---
description: Esta visão geral apresenta alguns conceitos importantes para usar o XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Principais conceitos do XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762209"
---
# <a name="xaudio2-key-concepts"></a><span data-ttu-id="208dc-103">Principais conceitos do XAudio2</span><span class="sxs-lookup"><span data-stu-id="208dc-103">XAudio2 Key Concepts</span></span>

<span data-ttu-id="208dc-104">Esta visão geral apresenta alguns conceitos importantes para usar o XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-104">This overview introduces some key concepts for using XAudio2.</span></span>

-   [<span data-ttu-id="208dc-105">Mecanismo de XAudio2</span><span class="sxs-lookup"><span data-stu-id="208dc-105">XAudio2 Engine</span></span>](#xaudio2-engine)
-   [<span data-ttu-id="208dc-106">Vozes</span><span class="sxs-lookup"><span data-stu-id="208dc-106">Voices</span></span>](#voices)
-   [<span data-ttu-id="208dc-107">Grafo de áudio</span><span class="sxs-lookup"><span data-stu-id="208dc-107">Audio Graph</span></span>](#audio-graph)
-   [<span data-ttu-id="208dc-108">Retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="208dc-108">Callbacks</span></span>](#callbacks)
-   [<span data-ttu-id="208dc-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="208dc-109">Related Topics</span></span>](#related-topics)

## <a name="xaudio2-engine"></a><span data-ttu-id="208dc-110">Mecanismo de XAudio2</span><span class="sxs-lookup"><span data-stu-id="208dc-110">XAudio2 Engine</span></span>

<span data-ttu-id="208dc-111">A interface do [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) é o núcleo do mecanismo XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-111">The [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface is the core of the XAudio2 engine.</span></span> <span data-ttu-id="208dc-112">A criação de uma instância da interface **IXAudio2** permite que o cliente enumere os dispositivos de áudio disponíveis, configure as propriedades da API global, crie vozes e monitore o desempenho.</span><span class="sxs-lookup"><span data-stu-id="208dc-112">Creating an instance of the **IXAudio2** interface allows the client to enumerate the available audio devices, to configure global API properties, to create voices, and to monitor performance.</span></span> <span data-ttu-id="208dc-113">A função auxiliar [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) executa tarefas de instanciação e inicialização para XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-113">The [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper function performs instantiation and initialization tasks for XAudio2.</span></span>

<span data-ttu-id="208dc-114">Você pode criar instâncias do XAudio2 várias vezes em um único processo.</span><span class="sxs-lookup"><span data-stu-id="208dc-114">You can create instances of XAudio2 multiple times within a single process.</span></span> <span data-ttu-id="208dc-115">Cada objeto XAudio2 Opera de forma independente e tem seu próprio thread de processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="208dc-115">Each XAudio2 object operates independently, and has its own audio processing thread.</span></span> <span data-ttu-id="208dc-116">Somente as configurações de depuração são compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="208dc-116">Only the debug settings are shared.</span></span> <span data-ttu-id="208dc-117">Isso é importante no Windows, onde vários componentes diferentes podem ser carregados em um único processo.</span><span class="sxs-lookup"><span data-stu-id="208dc-117">This is important on Windows where several different components may be loaded in a single process.</span></span> <span data-ttu-id="208dc-118">Por exemplo, o Internet Explorer pode usar vários componentes do XAudio2 simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="208dc-118">For example, Internet Explorer might use multiple XAudio2 components simultaneously.</span></span> <span data-ttu-id="208dc-119">Embora seja possível criar vários objetos do mecanismo XAudio2 em um único aplicativo cliente, você não deve passar informações entre seus respectivos grafos.</span><span class="sxs-lookup"><span data-stu-id="208dc-119">Although it is possible to create multiple XAudio2 engine objects within a single client application, you should not pass information between their respective graphs.</span></span>

<span data-ttu-id="208dc-120">Para obter um exemplo de inicialização do mecanismo XAudio2, consulte [como: inicializar o XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="208dc-120">For an example of initializing the XAudio2 engine, see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>

## <a name="voices"></a><span data-ttu-id="208dc-121">Vozes</span><span class="sxs-lookup"><span data-stu-id="208dc-121">Voices</span></span>

<span data-ttu-id="208dc-122">As vozes são os objetos XAudio2 usados para processar, manipular e reproduzir dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="208dc-122">Voices are the objects XAudio2 use to process, to manipulate, and to play audio data.</span></span> <span data-ttu-id="208dc-123">Há três tipos de vozes em XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-123">There are three types of voices in XAudio2.</span></span>

-   [<span data-ttu-id="208dc-124">**Vozes de origem**</span><span class="sxs-lookup"><span data-stu-id="208dc-124">**Source Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    <span data-ttu-id="208dc-125">As vozes de origem representam um fluxo de dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="208dc-125">Source voices represent a stream of audio data.</span></span> <span data-ttu-id="208dc-126">As vozes de origem enviam seus dados para outros tipos de vozes.</span><span class="sxs-lookup"><span data-stu-id="208dc-126">Source voices send their data to other types of voices.</span></span>

-   [<span data-ttu-id="208dc-127">**Submix vozes**</span><span class="sxs-lookup"><span data-stu-id="208dc-127">**Submix Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    <span data-ttu-id="208dc-128">As vozes submix executam alguma manipulação dos dados de áudio recebidos.</span><span class="sxs-lookup"><span data-stu-id="208dc-128">Submix voices perform some manipulation of audio data they receive.</span></span> <span data-ttu-id="208dc-129">Um exemplo de manipulação de dados de áudio pode ser a conversão de taxa de amostra.</span><span class="sxs-lookup"><span data-stu-id="208dc-129">One example of audio data manipulation might be sample rate conversion.</span></span> <span data-ttu-id="208dc-130">Depois que uma voz submix processa dados, ela passa esses dados para outra voz submix ou para uma voz mestra.</span><span class="sxs-lookup"><span data-stu-id="208dc-130">After a submix voice processes data, it passes that data to another submix voice or to a master voice.</span></span>

-   [<span data-ttu-id="208dc-131">**Vozes de dominar**</span><span class="sxs-lookup"><span data-stu-id="208dc-131">**Mastering Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    <span data-ttu-id="208dc-132">As vozes de controle de voz recebem dados de vozes de origem e vozes submix e envia esses dados para o hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="208dc-132">Mastering voices receive data from source voices and submix voices, and sends that data to the audio hardware.</span></span>

<span data-ttu-id="208dc-133">Consulte [XAudio2 vozes](voices.md) para obter uma visão geral das vozes XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-133">See [XAudio2 Voices](voices.md) for an overview of XAudio2 voices.</span></span>

## <a name="audio-graph"></a><span data-ttu-id="208dc-134">Grafo de áudio</span><span class="sxs-lookup"><span data-stu-id="208dc-134">Audio Graph</span></span>

<span data-ttu-id="208dc-135">Um grafo de áudio é uma coleção de vozes XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-135">An audio graph is a collection of XAudio2 voices.</span></span> <span data-ttu-id="208dc-136">O áudio começa em um lado de um gráfico de áudio em vozes de origem, e opcionalmente passa por uma ou mais vozes submix e termina em uma voz de mestre.</span><span class="sxs-lookup"><span data-stu-id="208dc-136">Audio starts at one side of an audio graph in source voices, optionally passes through one or more submix voices, and ends at a mastering voice.</span></span> <span data-ttu-id="208dc-137">Um grafo de áudio conterá uma voz de origem para cada som atualmente em execução, zero ou mais vozes submix e uma voz de mestre.</span><span class="sxs-lookup"><span data-stu-id="208dc-137">An audio graph will contain a source voice for each sound currently playing, zero or more submix voices, and one mastering voice.</span></span> <span data-ttu-id="208dc-138">O grafo de áudio mais simples, e o mínimo necessário para fazer um ruído em XAudio2, é uma saída de voz de origem única diretamente para uma voz de mestre.</span><span class="sxs-lookup"><span data-stu-id="208dc-138">The simplest audio graph, and the minimum needed to make a noise in XAudio2, is a single source voice outputting directly to a mastering voice.</span></span> <span data-ttu-id="208dc-139">Consulte [como: reproduzir um som com XAudio2](how-to--play-a-sound-with-xaudio2.md) para obter um exemplo das etapas mínimas necessárias para tocar um som com XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-139">See [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md) for an example of the minimum steps need to play a sound with XAudio2.</span></span>

<span data-ttu-id="208dc-140">Consulte [grafo de áudio XAudio2](audio-graphs.md) para obter uma visão geral dos grafos de áudio do XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-140">See [XAudio2 Audio Graph](audio-graphs.md) for an overview of XAudio2 audio graphs.</span></span>

## <a name="callbacks"></a><span data-ttu-id="208dc-141">Retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="208dc-141">Callbacks</span></span>

<span data-ttu-id="208dc-142">Os retornos de chamada são o mecanismo que o XAudio2 usa para sinalizar o código do cliente que ocorreu algum evento em uma voz ou no objeto do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="208dc-142">Callbacks are the mechanism XAudio2 uses to signal client code that some event has occurred in a voice or in the engine object.</span></span> <span data-ttu-id="208dc-143">Como a reprodução de áudio é assíncrona no mecanismo de XAudio2, os retornos de chamada fornecem a única maneira de determinar quando um som acaba sendo executado.</span><span class="sxs-lookup"><span data-stu-id="208dc-143">Because audio playback is asynchronous in the XAudio2 engine, callbacks provide the only way to determine when a sound is finished playing.</span></span>

<span data-ttu-id="208dc-144">Consulte [retornos de chamada do XAudio2](callbacks.md) para obter uma visão geral dos retornos de chamada do XAudio2.</span><span class="sxs-lookup"><span data-stu-id="208dc-144">See [XAudio2 Callbacks](callbacks.md) for an overview of XAudio2 callbacks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="208dc-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="208dc-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="208dc-146">Introdução</span><span class="sxs-lookup"><span data-stu-id="208dc-146">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="208dc-147">Versões do XAudio2</span><span class="sxs-lookup"><span data-stu-id="208dc-147">XAudio2 Versions</span></span>](xaudio2-versions.md)
</dt> <dt>

[<span data-ttu-id="208dc-148">Como: Inicializar o XAudio2</span><span class="sxs-lookup"><span data-stu-id="208dc-148">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="208dc-149">Como: tocar um som com XAudio2</span><span class="sxs-lookup"><span data-stu-id="208dc-149">How to: Play a sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



