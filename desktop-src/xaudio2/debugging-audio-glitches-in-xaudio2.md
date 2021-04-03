---
description: Os problemas podem ocorrer em XAudio2, este tópico aborda como eles são relatados e algumas abordagens para corrigi-los.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Depurando falhas de áudio no XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829077"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a><span data-ttu-id="94fac-103">Depurando falhas de áudio no XAudio2</span><span class="sxs-lookup"><span data-stu-id="94fac-103">Debugging Audio Glitches in XAudio2</span></span>

<span data-ttu-id="94fac-104">Os problemas podem ocorrer em XAudio2, este tópico aborda como eles são relatados e algumas abordagens para corrigi-los.</span><span class="sxs-lookup"><span data-stu-id="94fac-104">Glitches can occur in XAudio2, this topic covers how they are reported and some approaches to fixing them.</span></span>

<span data-ttu-id="94fac-105">Esta visão geral aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="94fac-105">This overview covers the following topics:</span></span>

-   [<span data-ttu-id="94fac-106">Causas de problemas de saída de áudio ou falhas</span><span class="sxs-lookup"><span data-stu-id="94fac-106">Causes of audio output problems or glitches</span></span>](#causes-of-audio-output-problems-or-glitches)
-   [<span data-ttu-id="94fac-107">Como o XAudio2 relata problemas</span><span class="sxs-lookup"><span data-stu-id="94fac-107">How XAudio2 reports problems</span></span>](#how-xaudio2-reports-problems)
-   [<span data-ttu-id="94fac-108">Abordagens para corrigir problemas</span><span class="sxs-lookup"><span data-stu-id="94fac-108">Approaches to fixing problems</span></span>](#approaches-to-fixing-problems)
-   [<span data-ttu-id="94fac-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94fac-109">Related topics</span></span>](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a><span data-ttu-id="94fac-110">Causas de problemas de saída de áudio ou falhas</span><span class="sxs-lookup"><span data-stu-id="94fac-110">Causes of audio output problems or glitches</span></span>

<span data-ttu-id="94fac-111">As falhas podem ocorrer na saída do XAudio2 por vários motivos.</span><span class="sxs-lookup"><span data-stu-id="94fac-111">Glitches can occur in XAudio2 output for several reasons.</span></span>

-   <span data-ttu-id="94fac-112">Uma voz de origem XAudio2 está em falta.</span><span class="sxs-lookup"><span data-stu-id="94fac-112">An XAudio2 source voice is starved.</span></span> <span data-ttu-id="94fac-113">O cliente não está enviando um novo áudio para ele com rapidez suficiente.</span><span class="sxs-lookup"><span data-stu-id="94fac-113">The client is not submitting fresh audio to it fast enough.</span></span> <span data-ttu-id="94fac-114">Você obtém silêncio porque não há dados a serem reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="94fac-114">You get silence because it has no data to play.</span></span>
-   <span data-ttu-id="94fac-115">XAudio2 como um todo é sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="94fac-115">XAudio2 as a whole is overburdened.</span></span> <span data-ttu-id="94fac-116">Demora mais de *x* MS para produzir *X* MS de áudio.</span><span class="sxs-lookup"><span data-stu-id="94fac-116">It takes longer than *X* ms to produce *X* ms of audio.</span></span> <span data-ttu-id="94fac-117">Você obtém dropouts porque o XAudio2 não pode produzir dados tão rápidos quanto o dispositivo de áudio precisar.</span><span class="sxs-lookup"><span data-stu-id="94fac-117">You get dropouts because XAudio2 can't produce data as fast as the audio device needs it.</span></span> <span data-ttu-id="94fac-118">Você pode estar executando muitas vozes ou efeitos por vez, fazendo muito trabalho em retornos de chamada XAudio2 ou fazendo chamadas de API do XAudio2 com muita frequência.</span><span class="sxs-lookup"><span data-stu-id="94fac-118">You might be running too many voices or effects at a time, doing too much work in XAudio2 callbacks, or making XAudio2 API calls too frequently.</span></span>
-   <span data-ttu-id="94fac-119">O thread de processamento de áudio está paralisando porque a implementação do cliente de algum retorno de chamada do XAudio2 está fazendo coisas que podem bloquear o thread.</span><span class="sxs-lookup"><span data-stu-id="94fac-119">The audio processing thread is stalling because the client's implementation of some XAudio2 callback is doing things that can block the thread.</span></span> <span data-ttu-id="94fac-120">Por exemplo, ele pode estar acessando o disco, sincronizando com outros threads ou chamando outras funções que possam bloquear.</span><span class="sxs-lookup"><span data-stu-id="94fac-120">For example, it might be accessing the disk, synchronizing with other threads, or calling other functions that may block.</span></span> <span data-ttu-id="94fac-121">Use um thread em segundo plano de prioridade mais baixa que o retorno de chamada pode sinalizar para executar essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="94fac-121">Use a lower-priority background thread that the callback can signal to perform such tasks.</span></span>
-   <span data-ttu-id="94fac-122">O sistema como um todo está sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="94fac-122">The system as a whole is overloaded.</span></span> <span data-ttu-id="94fac-123">Outros threads em execução no mesmo ou em uma prioridade mais alta do que XAudio2 estão fazendo muito trabalho.</span><span class="sxs-lookup"><span data-stu-id="94fac-123">Other threads running at the same or higher priority than XAudio2 are doing too much work.</span></span> <span data-ttu-id="94fac-124">Eles estão competindo com o thread de áudio por tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="94fac-124">They are competing with the audio thread for CPU time.</span></span>

## <a name="how-xaudio2-reports-problems"></a><span data-ttu-id="94fac-125">Como o XAudio2 relata problemas</span><span class="sxs-lookup"><span data-stu-id="94fac-125">How XAudio2 reports problems</span></span>

<span data-ttu-id="94fac-126">O XAudio2 pode comunicar problemas na compilação da depuração de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="94fac-126">XAudio2 can communicate glitches in the debug build in several ways.</span></span>

-   <span data-ttu-id="94fac-127">Se uma voz estiver sendo privada, XAudio2 mostrará uma mensagem neste formulário.</span><span class="sxs-lookup"><span data-stu-id="94fac-127">If a voice is being starved, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   <span data-ttu-id="94fac-128">Se o thread de áudio for executado por muito tempo, o XAudio2 mostrará uma mensagem neste formulário.</span><span class="sxs-lookup"><span data-stu-id="94fac-128">If the audio thread runs for too long, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    <span data-ttu-id="94fac-129">Normalmente, essa mensagem ocorre com a próxima mensagem.</span><span class="sxs-lookup"><span data-stu-id="94fac-129">Typically, this message occurs with the next message.</span></span>

-   <span data-ttu-id="94fac-130">Se o driver de áudio não puder ser alimentado com novos dados de áudio na hora, XAudio2 mostrará uma mensagem nesse formulário.</span><span class="sxs-lookup"><span data-stu-id="94fac-130">If the audio driver can't be fed new audio data on time, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   <span data-ttu-id="94fac-131">Chamar [**IXAudio2:: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) fornece dados de desempenho de XAudio2, incluindo o número total de falhas desde que o mecanismo de XAudio2 foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="94fac-131">Calling [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) provides XAudio2 performance data, including the total number of glitches since the XAudio2 engine started.</span></span>

## <a name="approaches-to-fixing-problems"></a><span data-ttu-id="94fac-132">Abordagens para corrigir problemas</span><span class="sxs-lookup"><span data-stu-id="94fac-132">Approaches to fixing problems</span></span>

<span data-ttu-id="94fac-133">As maneiras possíveis de reduzir as falhas de áudio incluem as seguintes.</span><span class="sxs-lookup"><span data-stu-id="94fac-133">Possible ways to reduce audio glitches include the following.</span></span>

-   <span data-ttu-id="94fac-134">No caso de consumo de voz: aumente a quantidade de dados de áudio que são enfileirados antecipadamente em uma voz.</span><span class="sxs-lookup"><span data-stu-id="94fac-134">In the voice starvation case: Increase the amount of audio data that is queued ahead on a voice.</span></span> <span data-ttu-id="94fac-135">Você pode usar [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) para descobrir o número de buffers em fila a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="94fac-135">You can use [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) to discover the number of buffers queued at any moment.</span></span> <span data-ttu-id="94fac-136">Se você ainda vir erros de consumo de voz, mas não puder ouvir nenhum problema, certifique-se de que você está configurando o [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Sinalizadores** para XAudio2 \_ fim \_ do \_ fluxo no buffer final de um som.</span><span class="sxs-lookup"><span data-stu-id="94fac-136">If you still see voice starvation errors, but can't hear any glitch, make sure you are setting [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flags** to XAUDIO2\_END\_OF\_STREAM on the final buffer of a sound.</span></span> <span data-ttu-id="94fac-137">Isso informa ao XAudio2 para não esperar que mais buffers estejam disponíveis assim que isso for concluído.</span><span class="sxs-lookup"><span data-stu-id="94fac-137">This tells XAudio2 not to expect any more buffers necessarily to be available as soon as this one completes.</span></span>

    <span data-ttu-id="94fac-138">Nos outros casos:</span><span class="sxs-lookup"><span data-stu-id="94fac-138">In the other cases:</span></span>

    -   <span data-ttu-id="94fac-139">Reduza o número de vozes e efeitos ativos no grafo, especialmente efeitos caros como reverberação.</span><span class="sxs-lookup"><span data-stu-id="94fac-139">Reduce the number of active voices and effects in the graph, especially expensive effects like reverb.</span></span>
    -   <span data-ttu-id="94fac-140">Desabilite as vozes e os efeitos que você não está usando.</span><span class="sxs-lookup"><span data-stu-id="94fac-140">Disable voices and effects you're not using.</span></span>
    -   <span data-ttu-id="94fac-141">Use os sinalizadores de XAUDIO2 de \_ voz \_ NOSRC e XAudio2 \_ de voz \_ em [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="94fac-141">Use the XAUDIO2\_VOICE\_NOSRC and XAUDIO2\_VOICE\_NOPITCH flags in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), whenever possible.</span></span> <span data-ttu-id="94fac-142">A conversão de taxa de amostra é dispendiosa.</span><span class="sxs-lookup"><span data-stu-id="94fac-142">Sample rate conversion is costly.</span></span>
    -   <span data-ttu-id="94fac-143">Reduza a taxa de amostra de vozes individuais.</span><span class="sxs-lookup"><span data-stu-id="94fac-143">Reduce the sample rate of individual voices.</span></span> <span data-ttu-id="94fac-144">Por exemplo, uma voz submix que hospeda um efeito de reverberação pode ter uma taxa de amostragem mais baixa do que a voz de origem enviando a ela.</span><span class="sxs-lookup"><span data-stu-id="94fac-144">For example, a submix voice hosting a reverb effect can have a lower sample rate than the source voice sending to it.</span></span> <span data-ttu-id="94fac-145">Sons como explosões e gunshots que não precisam de alta fidelidade também podem ser registrados em taxas de exemplo mais baixas.</span><span class="sxs-lookup"><span data-stu-id="94fac-145">Sounds such as explosions and gunshots that don't need high fidelity can also be recorded at lower sample rates.</span></span>
    -   <span data-ttu-id="94fac-146">Certifique-se de que as implementações de retorno de chamada façam o mínimo de trabalho possível e nunca bloqueiem.</span><span class="sxs-lookup"><span data-stu-id="94fac-146">Ensure that callback implementations do as little work as possible and never block.</span></span>
    -   <span data-ttu-id="94fac-147">Faça menos chamadas para XAudio2.</span><span class="sxs-lookup"><span data-stu-id="94fac-147">Make fewer calls to XAudio2.</span></span> <span data-ttu-id="94fac-148">Normalmente, os parâmetros de áudio não precisam ser atualizados para cada quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="94fac-148">Audio parameters usually don't need to be updated for every video frame.</span></span> <span data-ttu-id="94fac-149">A cada 30 ms, isso é suficiente.</span><span class="sxs-lookup"><span data-stu-id="94fac-149">Every 30 ms or so is sufficient.</span></span> <span data-ttu-id="94fac-150">Você deve eliminar as chamadas redundantes, como a configuração de volume várias vezes em sucessão rápida.</span><span class="sxs-lookup"><span data-stu-id="94fac-150">You should eliminate redundant calls, such as setting volume several times in quick succession.</span></span>
    -   <span data-ttu-id="94fac-151">Reduza o uso geral da CPU do jogo.</span><span class="sxs-lookup"><span data-stu-id="94fac-151">Reduce the game's overall CPU usage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94fac-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94fac-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94fac-153">Depuração de instalações</span><span class="sxs-lookup"><span data-stu-id="94fac-153">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="94fac-154">Referência de programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="94fac-154">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
