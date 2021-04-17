---
description: Como controlar os Estados de apresentação
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Como controlar os Estados de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763426"
---
# <a name="how-to-control-presentation-states"></a><span data-ttu-id="deb4c-103">Como controlar os Estados de apresentação</span><span class="sxs-lookup"><span data-stu-id="deb4c-103">How to Control Presentation States</span></span>

<span data-ttu-id="deb4c-104">A sessão de mídia fornece controle de transporte, como a alteração de Estados de apresentação (reproduzir, pausar e parar em um cenário de reprodução estilo de playlist).</span><span class="sxs-lookup"><span data-stu-id="deb4c-104">The Media Session provides transport control such as changing presentation states (Play, Pause, and Stop in a playlist-style playback scenario).</span></span> <span data-ttu-id="deb4c-105">Este tópico descreve os métodos de sessão de mídia que um aplicativo deve chamar para alterar o estado de reprodução.</span><span class="sxs-lookup"><span data-stu-id="deb4c-105">This topic describes Media Session methods that an application should call to change the playback state.</span></span>

<span data-ttu-id="deb4c-106">A tabela a seguir mostra as transições de estado de apresentação válidas.</span><span class="sxs-lookup"><span data-stu-id="deb4c-106">The following table shows the valid presentation state transitions.</span></span>



| <span data-ttu-id="deb4c-107">Transição de estado</span><span class="sxs-lookup"><span data-stu-id="deb4c-107">State transition</span></span> | <span data-ttu-id="deb4c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="deb4c-108">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb4c-109">Reproduzir > pausar</span><span class="sxs-lookup"><span data-stu-id="deb4c-109">Play -> Pause</span></span> | <span data-ttu-id="deb4c-110">O relógio de apresentação congela.</span><span class="sxs-lookup"><span data-stu-id="deb4c-110">The presentation clock freezes.</span></span>                                                            |
| <span data-ttu-id="deb4c-111">> de execução de reprodução</span><span class="sxs-lookup"><span data-stu-id="deb4c-111">Play -> Stop</span></span>  | <span data-ttu-id="deb4c-112">O relógio de apresentação é redefinido.</span><span class="sxs-lookup"><span data-stu-id="deb4c-112">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="deb4c-113">Pausar-> reproduzir</span><span class="sxs-lookup"><span data-stu-id="deb4c-113">Pause -> Play</span></span> | <span data-ttu-id="deb4c-114">O relógio de apresentação é retomado do tempo que froze durante a transição de reproduzir para pausar.</span><span class="sxs-lookup"><span data-stu-id="deb4c-114">The presentation clock resumes from the time it froze during the Play to Pause transition.</span></span> |
| <span data-ttu-id="deb4c-115">Pausar-> parar</span><span class="sxs-lookup"><span data-stu-id="deb4c-115">Pause -> Stop</span></span> | <span data-ttu-id="deb4c-116">O relógio de apresentação é redefinido.</span><span class="sxs-lookup"><span data-stu-id="deb4c-116">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="deb4c-117">Stop-> Play</span><span class="sxs-lookup"><span data-stu-id="deb4c-117">Stop -> Play</span></span>  | <span data-ttu-id="deb4c-118">O relógio de apresentação começa desde o início da apresentação.</span><span class="sxs-lookup"><span data-stu-id="deb4c-118">The presentation clock starts from the beginning of the presentation.</span></span>                      |
| <span data-ttu-id="deb4c-119">Parar > pausar</span><span class="sxs-lookup"><span data-stu-id="deb4c-119">Stop -> Pause</span></span> | <span data-ttu-id="deb4c-120">Não permitido.</span><span class="sxs-lookup"><span data-stu-id="deb4c-120">Not allowed.</span></span>                                                                               |



 

## <a name="to-change-presentation-states"></a><span data-ttu-id="deb4c-121">Para alterar os Estados de apresentação</span><span class="sxs-lookup"><span data-stu-id="deb4c-121">To change presentation states</span></span>

-   <span data-ttu-id="deb4c-122">Chame o método [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) para pausar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="deb4c-122">Call the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method to pause playback.</span></span>

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    <span data-ttu-id="deb4c-123">Antes de chamar esse método, o aplicativo deve chamar o método [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) para descobrir se a origem da mídia dá suporte ao estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="deb4c-123">Before calling this method, the application must call the [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) method to discover whether the media source supports the Pause state.</span></span> <span data-ttu-id="deb4c-124">Se tiver, esse método retornará **MFSESSIONCAP \_ Pause** no parâmetro *pdwCaps* .</span><span class="sxs-lookup"><span data-stu-id="deb4c-124">If it does, this method returns **MFSESSIONCAP\_PAUSE** in the *pdwCaps* parameter.</span></span>

    <span data-ttu-id="deb4c-125">Pause interrompe temporariamente a sessão de mídia, o relógio de apresentação e o coletor de fluxo para a apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="deb4c-125">Pause temporarily stops the Media Session, the presentation clock, and the stream sink for the current presentation.</span></span> <span data-ttu-id="deb4c-126">Depois que a chamada for concluída com êxito, o aplicativo receberá um evento [MESessionPaused](mesessionpaused.md) .</span><span class="sxs-lookup"><span data-stu-id="deb4c-126">After the call completes successfully, the application receives a [MESessionPaused](mesessionpaused.md) event.</span></span>

-   <span data-ttu-id="deb4c-127">Chame o método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) para parar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="deb4c-127">Call the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method to stop playback.</span></span>

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    <span data-ttu-id="deb4c-128">Esse método interrompe a sessão de mídia interrompendo a origem da mídia, os relógios correspondentes e os coletores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="deb4c-128">This method stops the Media Session by stopping the media source, the corresponding clocks, and stream sinks.</span></span> <span data-ttu-id="deb4c-129">Se a sessão de mídia estiver controlando a [origem do sequenciador](sequencer-source.md), as fontes nativas subjacentes serão interrompidas pela origem do sequenciador.</span><span class="sxs-lookup"><span data-stu-id="deb4c-129">If the Media Session is controlling the [Sequencer Source](sequencer-source.md), the underlying native sources are stopped by the sequencer source.</span></span> <span data-ttu-id="deb4c-130">Depois que a sessão de mídia for interrompida, o aplicativo receberá um evento [MESessionStopped](mesessionstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="deb4c-130">After the Media Session is stopped, the application receives a [MESessionStopped](mesessionstopped.md) event.</span></span>

-   <span data-ttu-id="deb4c-131">Chame o método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar a reprodução ou buscar uma nova posição.</span><span class="sxs-lookup"><span data-stu-id="deb4c-131">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method to start playback or seek to a new position.</span></span>

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    <span data-ttu-id="deb4c-132">Esse método inicia a sessão de mídia dos Estados de pausa e parada.</span><span class="sxs-lookup"><span data-stu-id="deb4c-132">This method starts the Media Session from Pause and Stop states.</span></span> <span data-ttu-id="deb4c-133">A sessão de mídia é responsável por configurar o fluxo de dados no pipeline.</span><span class="sxs-lookup"><span data-stu-id="deb4c-133">The Media Session is responsible for setting up the data flow in the pipeline.</span></span> <span data-ttu-id="deb4c-134">Esse método instrui a sessão de mídia a iniciar o relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="deb4c-134">This method instructs the Media Session to start the presentation clock.</span></span> <span data-ttu-id="deb4c-135">Após essa chamada, a sessão de mídia envia um evento [MESessionStarted](mesessionstarted.md) para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="deb4c-135">After this call, Media Session sends a [MESessionStarted](mesessionstarted.md) event to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="deb4c-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="deb4c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deb4c-137">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="deb4c-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



