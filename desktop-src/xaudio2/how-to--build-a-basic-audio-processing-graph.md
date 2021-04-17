---
description: O requisito mínimo para permitir que o XAudio2 reproduza dados de áudio é um grafo de processamento de áudio, que é construído a partir de uma única voz de mestre e uma única voz de origem.
ms.assetid: 40f79959-23c9-4513-363b-2f2fc85e4c0a
title: 'Como: Compilar um gráfico de processamento de áudio básico'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43a11601514e3bcad5536ed1a8599178bcc52aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768374"
---
# <a name="how-to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="8f31f-103">Como: Compilar um gráfico de processamento de áudio básico</span><span class="sxs-lookup"><span data-stu-id="8f31f-103">How to: Build a Basic Audio Processing Graph</span></span>

<span data-ttu-id="8f31f-104">O requisito mínimo para permitir que o XAudio2 reproduza dados de áudio é um grafo de processamento de áudio, que é construído a partir de uma única voz de mestre e uma única voz de origem.</span><span class="sxs-lookup"><span data-stu-id="8f31f-104">The minimum requirement for enabling XAudio2 to play audio data is an audio processing graph, which is constructed from a single mastering voice and a single source voice.</span></span>

## <a name="to-build-a-basic-audio-processing-graph"></a><span data-ttu-id="8f31f-105">Para criar um grafo básico de processamento de áudio</span><span class="sxs-lookup"><span data-stu-id="8f31f-105">To build a basic audio processing graph</span></span>

1.  <span data-ttu-id="8f31f-106">Inicialize o mecanismo XAudio2 seguindo as etapas descritas em [como: inicializar o XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="8f31f-106">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="8f31f-107">Preencha uma estrutura de [**\_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) **WAVEFORMATEX** e XAudio2 seguindo as etapas descritas em [como carregar arquivos de dados de áudio no XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="8f31f-107">Populate a **WAVEFORMATEX** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
3.  <span data-ttu-id="8f31f-108">Crie uma voz de origem usando a função [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) .</span><span class="sxs-lookup"><span data-stu-id="8f31f-108">Create a source voice using the [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) function.</span></span>

    <span data-ttu-id="8f31f-109">Quando você especifica NULL para o argumento pSendList de [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), a saída da voz de origem vai para a voz de mestre criada na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="8f31f-109">When you specify NULL for the pSendList argument of [**CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), the source voice's output goes to the mastering voice created in step 1.</span></span>

    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                  0, XAUDIO2_DEFAULT_FREQ_RATIO, NULL, NULL, NULL ) ) ) return hr;
    ```

    

    <span data-ttu-id="8f31f-110">Depois de concluir esta etapa, há um gráfico de áudio simples que consiste na voz de origem, na voz de mestre e no dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="8f31f-110">After you finish this step, there is a simple audio graph consisting of the source voice, the mastering voice, and the audio device.</span></span> <span data-ttu-id="8f31f-111">As etapas restantes neste tópico de instruções mostram como iniciar os dados de áudio que fluem pelo grafo.</span><span class="sxs-lookup"><span data-stu-id="8f31f-111">The remaining steps in this how-to topic show you how to start audio data flowing through the graph.</span></span>

    <span data-ttu-id="8f31f-112">Um grafo de áudio simples</span><span class="sxs-lookup"><span data-stu-id="8f31f-112">A simple audio graph</span></span>

    ![um gráfico de áudio simples.](images/xaudio2-audio-graph.png)

4.  <span data-ttu-id="8f31f-114">Use a função [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) para enviar um [**\_ buffer XAudio2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) para a voz de origem.</span><span class="sxs-lookup"><span data-stu-id="8f31f-114">Use the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) to submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice.</span></span>

    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

5.  <span data-ttu-id="8f31f-115">Use a função [**Iniciar**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) para iniciar a voz de origem.</span><span class="sxs-lookup"><span data-stu-id="8f31f-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span>

    ```
    if ( FAILED(hr = pSourceVoice->Start( 0, XAUDIO2_COMMIT_NOW ) ) )
        return hr;
    ```

    

## <a name="related-topics"></a><span data-ttu-id="8f31f-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f31f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f31f-117">Gráficos de áudio</span><span class="sxs-lookup"><span data-stu-id="8f31f-117">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="8f31f-118">Guia de Programação em XAudio2</span><span class="sxs-lookup"><span data-stu-id="8f31f-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
