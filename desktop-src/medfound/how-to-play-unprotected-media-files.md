---
description: Este tutorial mostra como reproduzir arquivos de mídia usando o objeto de sessão de mídia.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Como reproduzir arquivos de mídia com Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104553771"
---
# <a name="how-to-play-media-files-with-media-foundation"></a><span data-ttu-id="dd378-103">Como reproduzir arquivos de mídia com Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd378-103">How to Play Media Files with Media Foundation</span></span>

<span data-ttu-id="dd378-104">Este tutorial mostra como reproduzir arquivos de mídia usando o objeto de [sessão de mídia](media-session.md) .</span><span class="sxs-lookup"><span data-stu-id="dd378-104">This tutorial shows how to play media files using the [Media Session](media-session.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dd378-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="dd378-105">Prerequisites</span></span>

<span data-ttu-id="dd378-106">Antes de ler este tópico, você deve estar familiarizado com os seguintes conceitos de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="dd378-106">Before reading this topic, you should be familiar with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="dd378-107">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-107">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="dd378-108">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="dd378-108">Source Resolver</span></span>](source-resolver.md)
-   [<span data-ttu-id="dd378-109">Topologias</span><span class="sxs-lookup"><span data-stu-id="dd378-109">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="dd378-110">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-110">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="dd378-111">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="dd378-111">Presentation Descriptors</span></span>](presentation-descriptors.md)

> [!Note]  
> <span data-ttu-id="dd378-112">Este tópico não descreve como reproduzir arquivos protegidos pelo DRM (gerenciamento de direitos digitais).</span><span class="sxs-lookup"><span data-stu-id="dd378-112">This topic does not describe how to play files that are protected by digital rights management (DRM).</span></span> <span data-ttu-id="dd378-113">Para obter informações sobre DRM em Microsoft Media Foundation, consulte [como reproduzir arquivos de mídia protegidos](how-to-play-protected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="dd378-113">For information about DRM in Microsoft Media Foundation, see [How to Play Protected Media Files](how-to-play-protected-media-files.md).</span></span>

 

## <a name="overview"></a><span data-ttu-id="dd378-114">Visão geral</span><span class="sxs-lookup"><span data-stu-id="dd378-114">Overview</span></span>

<span data-ttu-id="dd378-115">Os seguintes objetos são usados para reproduzir um arquivo de mídia com a sessão de mídia:</span><span class="sxs-lookup"><span data-stu-id="dd378-115">The following objects are used to play a media file with the Media Session:</span></span>

-   <span data-ttu-id="dd378-116">Uma *origem de mídia* é um objeto que analisa um arquivo de mídia ou outra fonte de dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-116">A *media source* is an object that parses a media file or other source of media data.</span></span> <span data-ttu-id="dd378-117">A origem de mídia cria objetos de *fluxo* para cada fluxo de áudio ou vídeo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd378-117">The media source creates *stream* objects for each audio or video stream in the file.</span></span> <span data-ttu-id="dd378-118">Os *decodificadores* convertem dados de mídia codificados em vídeo e áudio descompactados.</span><span class="sxs-lookup"><span data-stu-id="dd378-118">*Decoders* convert encoded media data into uncompressed video and audio.</span></span>
-   <span data-ttu-id="dd378-119">O *resolvedor de origem* cria uma origem de mídia a partir de uma URL.</span><span class="sxs-lookup"><span data-stu-id="dd378-119">The *Source Resolver* creates a media source from a URL.</span></span>
-   <span data-ttu-id="dd378-120">O [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) renderiza o vídeo na tela.</span><span class="sxs-lookup"><span data-stu-id="dd378-120">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) renders video to the screen.</span></span>
-   <span data-ttu-id="dd378-121">O SAR ( [processamento de áudio de streaming](streaming-audio-renderer.md) ) renderiza o áudio para um alto-falante ou outro dispositivo de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="dd378-121">The [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) renders audio to a speaker or other audio output device.</span></span>
-   <span data-ttu-id="dd378-122">Uma *topologia* define o fluxo de dados da origem de mídia para o EVR e o SAR.</span><span class="sxs-lookup"><span data-stu-id="dd378-122">A *topology* defines the flow of data from the media source to the EVR and SAR.</span></span>
-   <span data-ttu-id="dd378-123">A *sessão de mídia* controla o fluxo de dados e envia eventos de status para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dd378-123">The *Media Session* controls the data flow and sends status events to the application.</span></span> <span data-ttu-id="dd378-124">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="dd378-124">The following diagram illustrates this process.</span></span>

![diagrama mostrando a reprodução usando a sessão de mídia](images/session-playback.gif)

<span data-ttu-id="dd378-126">Veja a seguir uma descrição geral das etapas necessárias para reproduzir um arquivo de mídia usando a sessão de mídia:</span><span class="sxs-lookup"><span data-stu-id="dd378-126">The following is a general outline of the steps needed to play a media file using the Media Session:</span></span>

1.  <span data-ttu-id="dd378-127">Chame a função [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) para inicializar a plataforma de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dd378-127">Call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="dd378-128">Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar uma nova instância da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-128">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="dd378-129">Use o resolvedor de origem para criar uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-129">Use the source resolver to create a media source.</span></span> <span data-ttu-id="dd378-130">Para obter mais informações, consulte [usando o resolvedor de origem](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="dd378-130">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>
4.  <span data-ttu-id="dd378-131">Crie uma topologia que conecta a origem de mídia ao EVR e SAR.</span><span class="sxs-lookup"><span data-stu-id="dd378-131">Create a topology that connects the media source to the EVR and SAR.</span></span> <span data-ttu-id="dd378-132">Nesta etapa, o aplicativo cria uma topologia *parcial* que não inclui os decodificadores.</span><span class="sxs-lookup"><span data-stu-id="dd378-132">In this step, the application creates a *partial* topology that does not include the decoders.</span></span> <span data-ttu-id="dd378-133">Para obter mais informações, consulte [criando topologias de reprodução](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="dd378-133">For more information, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="dd378-134">Chame [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-134">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
6.  <span data-ttu-id="dd378-135">Use a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) para obter eventos da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-135">Use the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface to get events from the Media Session.</span></span>
7.  <span data-ttu-id="dd378-136">Chame [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="dd378-136">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start playback.</span></span> <span data-ttu-id="dd378-137">Depois que a reprodução é iniciada, você pode pausá-la chamando [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou pará-la chamando [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="dd378-137">After playback starts, you can pause it by calling [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or stop it by calling [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
8.  <span data-ttu-id="dd378-138">Quando o aplicativo for encerrado, libere os recursos:</span><span class="sxs-lookup"><span data-stu-id="dd378-138">When the application exits, release resources:</span></span>

    1.  <span data-ttu-id="dd378-139">Chame [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-139">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span> <span data-ttu-id="dd378-140">Esse método é assíncrono.</span><span class="sxs-lookup"><span data-stu-id="dd378-140">This method is asynchronous.</span></span> <span data-ttu-id="dd378-141">Quando for concluído, a sessão de mídia enviará um evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="dd378-141">When it completes, the Media Session sends an [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="dd378-142">Em seguida, é seguro executar as etapas restantes.</span><span class="sxs-lookup"><span data-stu-id="dd378-142">Then it is safe to perform the remaining steps.</span></span>
    2.  <span data-ttu-id="dd378-143">Chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para desligar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-143">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
    3.  <span data-ttu-id="dd378-144">Chame [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) para desligar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="dd378-144">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) to shut down the Media Session.</span></span>
    4.  <span data-ttu-id="dd378-145">Chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) para desligar a plataforma Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dd378-145">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>

<span data-ttu-id="dd378-146">As seções a seguir mostram um exemplo de código completo:</span><span class="sxs-lookup"><span data-stu-id="dd378-146">The following sections show a complete code example:</span></span>

-   [<span data-ttu-id="dd378-147">Etapa 1: declarar a classe CPlayer</span><span class="sxs-lookup"><span data-stu-id="dd378-147">Step 1: Declare the CPlayer Class</span></span>](step-1--declare-the-cplayer-class.md)
-   [<span data-ttu-id="dd378-148">Etapa 2: criar o objeto CPlayer</span><span class="sxs-lookup"><span data-stu-id="dd378-148">Step 2: Create the CPlayer Object</span></span>](step-2--create-the-cplayer-object.md)
-   [<span data-ttu-id="dd378-149">Etapa 3: abrir um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-149">Step 3: Open a Media File</span></span>](step-3--open-a-media-file.md)
-   [<span data-ttu-id="dd378-150">Etapa 4: criar a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-150">Step 4: Create the Media Session</span></span>](step-4--create-the-media-session.md)
-   [<span data-ttu-id="dd378-151">Etapa 5: manipular eventos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-151">Step 5: Handle Media Session Events</span></span>](step-5--handle-media-session-events.md)
-   [<span data-ttu-id="dd378-152">Etapa 6: controle de reprodução</span><span class="sxs-lookup"><span data-stu-id="dd378-152">Step 6: Control Playback</span></span>](step-6--control-playback.md)
-   [<span data-ttu-id="dd378-153">Etapa 7: desligar a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-153">Step 7: Shut Down the Media Session</span></span>](step-7--shut-down-the-media-session.md)
-   [<span data-ttu-id="dd378-154">Exemplo de reprodução de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-154">Media Session Playback Example</span></span>](media-session-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="dd378-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd378-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd378-156">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="dd378-156">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="dd378-157">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="dd378-157">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



