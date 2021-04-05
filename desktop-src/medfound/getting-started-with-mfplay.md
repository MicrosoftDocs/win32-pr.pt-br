---
description: MFPlay é uma API para criar aplicativos de reprodução de mídia em C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Introdução com MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457210"
---
# <a name="getting-started-with-mfplay"></a><span data-ttu-id="75012-103">Introdução com MFPlay</span><span class="sxs-lookup"><span data-stu-id="75012-103">Getting Started with MFPlay</span></span>

<span data-ttu-id="75012-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="75012-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="75012-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="75012-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="75012-106">\]</span><span class="sxs-lookup"><span data-stu-id="75012-106">\]</span></span>

<span data-ttu-id="75012-107">MFPlay é uma API para criar aplicativos de reprodução de mídia em C++.</span><span class="sxs-lookup"><span data-stu-id="75012-107">MFPlay is an API for creating media playback applications in C++.</span></span>

<span data-ttu-id="75012-108">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="75012-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="75012-109">Requirements</span><span class="sxs-lookup"><span data-stu-id="75012-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="75012-110">Sobre o MFPlay</span><span class="sxs-lookup"><span data-stu-id="75012-110">About MFPlay</span></span>](#about-mfplay)
-   [<span data-ttu-id="75012-111">Reprodução de um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="75012-111">Playing a Media File</span></span>](#playing-a-media-file)
-   [<span data-ttu-id="75012-112">Controlando a reprodução</span><span class="sxs-lookup"><span data-stu-id="75012-112">Controlling Playback</span></span>](#controlling-playback)
-   [<span data-ttu-id="75012-113">Recebendo eventos do Player</span><span class="sxs-lookup"><span data-stu-id="75012-113">Receiving Events From the Player</span></span>](#receiving-events-from-the-player)
-   [<span data-ttu-id="75012-114">Obtendo informações sobre um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="75012-114">Getting Information About a Media File</span></span>](#getting-information-about-a-media-file)
-   [<span data-ttu-id="75012-115">Gerenciando a reprodução de vídeo</span><span class="sxs-lookup"><span data-stu-id="75012-115">Managing Video Playback</span></span>](#managing-video-playback)
-   [<span data-ttu-id="75012-116">Limitações do MFPlay</span><span class="sxs-lookup"><span data-stu-id="75012-116">Limitations of MFPlay</span></span>](#limitations-of-mfplay)
-   [<span data-ttu-id="75012-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75012-117">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="75012-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75012-118">Requirements</span></span>

<span data-ttu-id="75012-119">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="75012-119">MFPlay requires Windows 7.</span></span>

## <a name="about-mfplay"></a><span data-ttu-id="75012-120">Sobre o MFPlay</span><span class="sxs-lookup"><span data-stu-id="75012-120">About MFPlay</span></span>

<span data-ttu-id="75012-121">O MFPlay tem um modelo de programação simples, ao mesmo tempo em que fornece o conjunto principal de recursos de que a maioria dos aplicativos de reprodução precisa.</span><span class="sxs-lookup"><span data-stu-id="75012-121">MFPlay has a simple programming model, while providing the core set of features that most playback applications need.</span></span> <span data-ttu-id="75012-122">Um aplicativo cria um objeto de *jogador* que controla a reprodução.</span><span class="sxs-lookup"><span data-stu-id="75012-122">An application creates a *player* object that controls playback.</span></span> <span data-ttu-id="75012-123">Para reproduzir um arquivo de mídia, o objeto Player cria um *item de mídia*, que pode ser usado para obter informações sobre o conteúdo do arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="75012-123">To play a media file, the player object creates a *media item*, which can be used to get information about the contents of the media file.</span></span> <span data-ttu-id="75012-124">O aplicativo controla a reprodução por meio de métodos na interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) do objeto de jogador.</span><span class="sxs-lookup"><span data-stu-id="75012-124">The application controls playback through methods on the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="75012-125">Opcionalmente, o aplicativo pode obter notificações de eventos por meio de uma interface de retorno de chamada. o diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="75012-125">Optionally, the application can get event notifications through a callback interface The following diagram illustrates this process.</span></span>

![diagrama conceitual: o aplicativo e o ponto do Player entre si, ambos apontam para o item de mídia, que aponta para o arquivo de mídia](images/mfplay.png)

## <a name="playing-a-media-file"></a><span data-ttu-id="75012-127">Reprodução de um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="75012-127">Playing a Media File</span></span>

<span data-ttu-id="75012-128">Para reproduzir um arquivo de mídia, chame a função [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="75012-128">To play a media file, call the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="75012-129">A função [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) cria uma nova instância do objeto MFPlay Player.</span><span class="sxs-lookup"><span data-stu-id="75012-129">The [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function creates a new instance of the MFPlay player object.</span></span> <span data-ttu-id="75012-130">A função usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="75012-130">The function takes the following parameters:</span></span>

-   <span data-ttu-id="75012-131">O primeiro parâmetro é a URL do arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="75012-131">The first parameter is the URL of the file to open.</span></span> <span data-ttu-id="75012-132">Pode ser um arquivo local ou um arquivo em um servidor de mídia.</span><span class="sxs-lookup"><span data-stu-id="75012-132">This can be a local file or a file on a media server.</span></span>
-   <span data-ttu-id="75012-133">O segundo parâmetro especifica se a reprodução é iniciada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="75012-133">The second parameter specifies whether playback starts automatically.</span></span> <span data-ttu-id="75012-134">Ao definir essa paremeter como **true**, o arquivo será reproduzido assim que MFPlay o carregar.</span><span class="sxs-lookup"><span data-stu-id="75012-134">By setting this paremeter to **TRUE**, the file will play as soon as MFPlay loads it.</span></span>
-   <span data-ttu-id="75012-135">O terceiro parâmetro define várias opções.</span><span class="sxs-lookup"><span data-stu-id="75012-135">The third parameter sets various options.</span></span> <span data-ttu-id="75012-136">Para as opções padrão, passe zero (0).</span><span class="sxs-lookup"><span data-stu-id="75012-136">For the default options, pass zero (0).</span></span>
-   <span data-ttu-id="75012-137">O quarto parâmetro é um ponteiro para uma interface de retorno de chamada opcional.</span><span class="sxs-lookup"><span data-stu-id="75012-137">The fourth parameter is a pointer to an optional callback interface.</span></span> <span data-ttu-id="75012-138">Esse parâmetro pode ser **nulo**, conforme mostrado.</span><span class="sxs-lookup"><span data-stu-id="75012-138">This parameter can be **NULL**, as shown.</span></span> <span data-ttu-id="75012-139">O retorno de chamada é descrito na seção [recebendo eventos do Player](#receiving-events-from-the-player).</span><span class="sxs-lookup"><span data-stu-id="75012-139">The callback is described in the section [Receiving Events From the Player](#receiving-events-from-the-player).</span></span>
-   <span data-ttu-id="75012-140">O quinto parâmetro é um identificador para a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75012-140">The fifth parameter is a handle to the application window.</span></span> <span data-ttu-id="75012-141">Se o arquivo de mídia contiver um fluxo de vídeo, o vídeo aparecerá dentro da área do cliente desta janela.</span><span class="sxs-lookup"><span data-stu-id="75012-141">If the media file contains a video stream, the video will appear inside the client area of this window.</span></span> <span data-ttu-id="75012-142">Para reprodução somente de áudio, esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="75012-142">For audio-only playback, this parameter can be **NULL**.</span></span>

<span data-ttu-id="75012-143">O último parâmetro recebe um ponteiro para a interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) do objeto de jogador.</span><span class="sxs-lookup"><span data-stu-id="75012-143">The last parameter receives a pointer to the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span>

<span data-ttu-id="75012-144">Antes de o aplicativo ser desligado, certifique-se de liberar o ponteiro [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="75012-144">Before the application shuts down, be sure to release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) pointer.</span></span> <span data-ttu-id="75012-145">Você pode fazer isso no manipulador de mensagens de **\_ fechamento do WM** .</span><span class="sxs-lookup"><span data-stu-id="75012-145">You can do this in your **WM\_CLOSE** message handler.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> <span data-ttu-id="75012-146">Este exemplo usa a função [SafeRelease](saferelease.md) para liberar ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="75012-146">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="75012-147">Para reprodução de vídeo simples, esse é todo o código de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="75012-147">For simple video playback, that's all the code you need.</span></span> <span data-ttu-id="75012-148">O restante deste tutorial mostrará como adicionar mais recursos, começando com como controlar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="75012-148">The rest of this tutorial will show how to add more features, starting with how to control playback.</span></span>

## <a name="controlling-playback"></a><span data-ttu-id="75012-149">Controlando a reprodução</span><span class="sxs-lookup"><span data-stu-id="75012-149">Controlling Playback</span></span>

<span data-ttu-id="75012-150">O código mostrado na seção anterior reproduzirá o arquivo de mídia até atingir o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="75012-150">The code shown in the previous section will play the media file until it reaches the end of the file.</span></span> <span data-ttu-id="75012-151">Você pode parar e iniciar a reprodução chamando os seguintes métodos na interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) :</span><span class="sxs-lookup"><span data-stu-id="75012-151">You can stop and start playback by calling the following methods on the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface:</span></span>

-   <span data-ttu-id="75012-152">[**IMFPMediaPlayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pausa a reprodução.</span><span class="sxs-lookup"><span data-stu-id="75012-152">[**IMFPMediaPlayer::Pause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pauses playback.</span></span> <span data-ttu-id="75012-153">Enquanto a reprodução é pausada, o quadro de vídeo mais recente é exibido e o áudio é silencioso.</span><span class="sxs-lookup"><span data-stu-id="75012-153">While playback is paused, the most recent video frame is displayed, and audio is silent.</span></span>
-   <span data-ttu-id="75012-154">[**IMFPMediaPlayer:: Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) interrompe a reprodução.</span><span class="sxs-lookup"><span data-stu-id="75012-154">[**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) stops playback.</span></span> <span data-ttu-id="75012-155">Nenhum vídeo é exibido e a posição de reprodução é redefinida para o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="75012-155">No video is displayed, and the playback position resets to the start of the file.</span></span>
-   <span data-ttu-id="75012-156">[**IMFPMediaPlayer::P o Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) retoma a reprodução após parar ou pausar.</span><span class="sxs-lookup"><span data-stu-id="75012-156">[**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) resumes playback after stopping or pausing.</span></span>

<span data-ttu-id="75012-157">O código a seguir pausa ou retoma a reprodução quando você pressiona a **barra de espaços**.</span><span class="sxs-lookup"><span data-stu-id="75012-157">The following code pauses or resumes playback when you press the **SPACEBAR**.</span></span>


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



<span data-ttu-id="75012-158">Este exemplo chama o método [**IMFPMediaPlayer:: GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) para obter o estado de reprodução atual (em pausa, parado ou em execução) e pausa ou retomada de acordo.</span><span class="sxs-lookup"><span data-stu-id="75012-158">This example calls the [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) method to get the current playback state (paused, stopped, or playing) and pauses or resumes accordingly.</span></span>

## <a name="receiving-events-from-the-player"></a><span data-ttu-id="75012-159">Recebendo eventos do Player</span><span class="sxs-lookup"><span data-stu-id="75012-159">Receiving Events From the Player</span></span>

<span data-ttu-id="75012-160">O MFPlay usa uma interface de retorno de chamada para enviar eventos para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75012-160">MFPlay uses a callback interface to send events to your application.</span></span> <span data-ttu-id="75012-161">Há dois motivos para esse retorno de chamada:</span><span class="sxs-lookup"><span data-stu-id="75012-161">There are two reasons for this callback:</span></span>

-   <span data-ttu-id="75012-162">A reprodução ocorre em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="75012-162">Playback occurs on a separate thread.</span></span> <span data-ttu-id="75012-163">Durante a reprodução, determinados eventos podem ocorrer, como chegar ao final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="75012-163">During playback, certain events might occur, such as reaching the end of the file.</span></span> <span data-ttu-id="75012-164">O MFPlay usa o retorno de chamada para notificar seu aplicativo do evento.</span><span class="sxs-lookup"><span data-stu-id="75012-164">MFPlay uses the callback to notify your application of the event.</span></span>
-   <span data-ttu-id="75012-165">Muitos dos métodos [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) são assíncronos, o que significa que eles retornam antes da conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="75012-165">Many of the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) methods are asynchronous, meaning they return before the operation completes.</span></span> <span data-ttu-id="75012-166">Os métodos assíncronos permitem que você inicie uma operação do seu thread de interface do usuário que pode levar muito tempo para ser concluída, sem que a interface do usuário seja bloqueada.</span><span class="sxs-lookup"><span data-stu-id="75012-166">Asynchronous methods let you start an operation from your UI thread that might take a long time to complete, without it causing your UI to block.</span></span> <span data-ttu-id="75012-167">Após a conclusão da operação, MFPlay sinaliza o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="75012-167">After the operation completes, MFPlay signals the callback.</span></span>

<span data-ttu-id="75012-168">Para receber notificações de retorno de chamada, implemente a interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="75012-168">To receive callback notifications, implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="75012-169">Essa interface herda **IUnknown** e define um único método, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="75012-169">This interface inherits **IUnknown** and defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="75012-170">Para configurar o retorno de chamada, passe um ponteiro para a implementação de **IMFPMediaPlayerCallback** no parâmetro *PCallback* da função [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="75012-170">To set up the callback, pass a pointer to your **IMFPMediaPlayerCallback** implementation in the *pCallback* parameter of the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>

<span data-ttu-id="75012-171">Este é o primeiro exemplo deste tutorial, modificado para incluir o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="75012-171">Here is the first example from this tutorial, modified to include the callback.</span></span>


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



<span data-ttu-id="75012-172">O método [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) tem um único parâmetro, que é um ponteiro para a estrutura do [**\_ \_ cabeçalho do evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="75012-172">The [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method has a single parameter, which is a pointer to the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="75012-173">O membro **eEventType** dessa estrutura informa qual evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="75012-173">The **eEventType** member of this structure tells you which event occurred.</span></span> <span data-ttu-id="75012-174">Por exemplo, quando a reprodução é iniciada, o MFPlay envia o evento de **\_ reprodução do \_ tipo \_ de evento MFP** .</span><span class="sxs-lookup"><span data-stu-id="75012-174">For example, when playback starts, MFPlay sends the **MFP\_EVENT\_TYPE\_PLAY** event.</span></span>

<span data-ttu-id="75012-175">Cada tipo de evento tem uma estrutura de dados correspondente que contém informações para esse evento.</span><span class="sxs-lookup"><span data-stu-id="75012-175">Each event type has a corresponding data structure that contains information for that event.</span></span> <span data-ttu-id="75012-176">Cada uma dessas estruturas começa com uma estrutura de [**\_ \_ cabeçalho de evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="75012-176">Each of these structures starts with an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="75012-177">No retorno de chamada, converta o ponteiro do **\_ \_ cabeçalho do evento MFP** na estrutura de dados específica do evento.</span><span class="sxs-lookup"><span data-stu-id="75012-177">In your callback, cast the **MFP\_EVENT\_HEADER** pointer to the event-specific data structure.</span></span> <span data-ttu-id="75012-178">Por exemplo, se o tipo de evento for o **\_ \_ evento de reprodução da MFP**, a estrutura de dados será o [**\_ \_ evento de reprodução da MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span><span class="sxs-lookup"><span data-stu-id="75012-178">For example, if the event type is **MFP\_PLAY\_EVENT**, the data structure is [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span></span> <span data-ttu-id="75012-179">O código a seguir mostra como tratar esse evento no retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="75012-179">The following code shows how to handle this event in the callback.</span></span>


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



<span data-ttu-id="75012-180">Este exemplo usa o evento de [**\_ \_ \_ evento MFP Get Play**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) para converter o ponteiro *pEventHeader* em uma estrutura de [**evento de \_ reprodução \_ de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) .</span><span class="sxs-lookup"><span data-stu-id="75012-180">This example uses the [**MFP\_GET\_PLAY\_EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) event to cast the *pEventHeader* pointer to an [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) structure.</span></span> <span data-ttu-id="75012-181">O **HRESULT** da operação que disparou o evento é armazenado no campo **hrEvent** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="75012-181">The **HRESULT** from the operation that triggered the event is stored in the **hrEvent** field of the structure.</span></span>

<span data-ttu-id="75012-182">Para obter uma lista de todos os tipos de eventos e as estruturas de dados correspondentes, consulte [**\_ \_ tipo de evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span><span class="sxs-lookup"><span data-stu-id="75012-182">For a list of all the event types and the corresponding data structures, see [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span></span>

<span data-ttu-id="75012-183">Uma observação sobre Threading: por padrão, MFPlay invoca o retorno de chamada do mesmo thread que chamou [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span><span class="sxs-lookup"><span data-stu-id="75012-183">A note about threading: By default, MFPlay invokes the callback from the same thread that called [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span></span> <span data-ttu-id="75012-184">Esse thread deve ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="75012-184">This thread must have a message loop.</span></span> <span data-ttu-id="75012-185">Como alternativa, você pode passar a **opção MFP sinalizador de \_ \_ retorno de \_ \_ chamada segmentado sem thread** no parâmetro *creationOptions* de **MFPCreateMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="75012-185">Alternatively, you can pass the **MFP\_OPTION\_FREE\_THREADED\_CALLBACK** flag in the *creationOptions* parameter of **MFPCreateMediaPlayer**.</span></span> <span data-ttu-id="75012-186">Esse sinalizador faz com que o MFPlay invoque retornos de chamada de um thread separado.</span><span class="sxs-lookup"><span data-stu-id="75012-186">This flag causes MFPlay to invoke callbacks from a separate thread.</span></span> <span data-ttu-id="75012-187">Qualquer opção tem implicações para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75012-187">Either option has implications for your application.</span></span> <span data-ttu-id="75012-188">A opção padrão significa que o retorno de chamada não pode fazer nada que aguarde em seu loop de mensagem, como aguardar uma ação de interface do usuário, porque isso bloqueará o procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="75012-188">The default option means your callback cannot do anything that waits on your message loop, such as waiting for a UI action, because that will block your window procedure.</span></span> <span data-ttu-id="75012-189">A opção de thread livre significa que você precisa usar seções críticas para proteger quaisquer dados que você acessar em seu retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="75012-189">The free-threaded option means you need to use critical sections to protect any data that you access in your callback.</span></span> <span data-ttu-id="75012-190">Na maioria dos casos, a opção padrão é mais simples.</span><span class="sxs-lookup"><span data-stu-id="75012-190">In most cases, the default option is simplest.</span></span>

## <a name="getting-information-about-a-media-file"></a><span data-ttu-id="75012-191">Obtendo informações sobre um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="75012-191">Getting Information About a Media File</span></span>

<span data-ttu-id="75012-192">Quando você abre um arquivo de mídia no MFPlay, o Player cria um objeto chamado *item de mídia* que representa o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="75012-192">When you open a media file in MFPlay, the player creates an object called a *media item* that represents the media file.</span></span> <span data-ttu-id="75012-193">Esse objeto expõe a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que pode ser usada para obter informações sobre o arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="75012-193">This object exposes the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which you can use to get information about the media file.</span></span> <span data-ttu-id="75012-194">Muitas das estruturas de evento MFPlay contêm um ponteiro para o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="75012-194">Many of the MFPlay event structures contain a pointer to the current media item.</span></span> <span data-ttu-id="75012-195">Você também pode obter o item de mídia atual chamando [**IMFPMediaPlayer:: GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) no Player.</span><span class="sxs-lookup"><span data-stu-id="75012-195">You can also get the current media item by calling [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) on the player.</span></span>

<span data-ttu-id="75012-196">Dois métodos particularmente úteis são [**IMFPMediaItem:: HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) e [**IMFPMediaItem:: HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span><span class="sxs-lookup"><span data-stu-id="75012-196">Two particularly useful methods are [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) and [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span></span> <span data-ttu-id="75012-197">Esses métodos consultam se a origem da mídia contém vídeo ou áudio.</span><span class="sxs-lookup"><span data-stu-id="75012-197">These methods query whether the media source contains video or audio.</span></span>

<span data-ttu-id="75012-198">Por exemplo, o código a seguir testa se o arquivo de mídia atual contém um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75012-198">For example, the following code tests whether the current media file contains a video stream.</span></span>


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



<span data-ttu-id="75012-199">Se o arquivo de origem contiver um fluxo de vídeo selecionado para reprodução, *bHasVideo* e *bIsSelected* serão definidos como **true**.</span><span class="sxs-lookup"><span data-stu-id="75012-199">If the source file contains a video stream that is selected for playback, *bHasVideo* and *bIsSelected* are both set to **TRUE**.</span></span>

## <a name="managing-video-playback"></a><span data-ttu-id="75012-200">Gerenciando a reprodução de vídeo</span><span class="sxs-lookup"><span data-stu-id="75012-200">Managing Video Playback</span></span>

<span data-ttu-id="75012-201">Quando o MFPlay reproduz um arquivo de vídeo, ele desenha o vídeo na janela que você especificou na função [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="75012-201">When MFPlay plays a video file, it draws the video in the window that you specified in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span> <span data-ttu-id="75012-202">Isso ocorre em um thread separado de Propriedade do pipeline de reprodução de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="75012-202">This occurs on a separate thread owned by the Microsoft Media Foundation playback pipeline.</span></span> <span data-ttu-id="75012-203">Para a maior parte, seu aplicativo não precisa gerenciar esse processo.</span><span class="sxs-lookup"><span data-stu-id="75012-203">For the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="75012-204">No entanto, há duas situações em que o aplicativo deve notificar o MFPlay para atualizar o vídeo.</span><span class="sxs-lookup"><span data-stu-id="75012-204">However, there are two situations where the application must notify MFPlay to update the video.</span></span>

-   <span data-ttu-id="75012-205">Se a reprodução for pausada ou interrompida, MFPlay deverá ser notificado sempre que a janela de vídeo do aplicativo receber uma mensagem de pintura do WM \_ .</span><span class="sxs-lookup"><span data-stu-id="75012-205">If playback is paused or stopped, MFPlay must be notified whenever the application's video window receives a WM\_PAINT message.</span></span> <span data-ttu-id="75012-206">Isso permite que o MFPlay repinte a janela.</span><span class="sxs-lookup"><span data-stu-id="75012-206">This allows MFPlay to repaint the window.</span></span>
-   <span data-ttu-id="75012-207">Se a janela for redimensionada, MFPlay deverá ser notificado para que possa dimensionar o vídeo para corresponder ao novo tamanho da janela.</span><span class="sxs-lookup"><span data-stu-id="75012-207">If the window is resized, MFPlay must be notified so that it can scale the video to match the new window size.</span></span>

<span data-ttu-id="75012-208">O método [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) lida com ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="75012-208">The [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method handles both cases.</span></span> <span data-ttu-id="75012-209">Chame esse método dentro dos \_ manipuladores de mensagens de tamanho do WM Paint e \_ do WM para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75012-209">Call this method inside both the WM\_PAINT and WM\_SIZE message handlers for the video window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75012-210">Chame a função **BEGINPAINT** GDI antes de chamar [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="75012-210">Call the GDI **BeginPaint** function before calling [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span>

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="75012-211">A menos que você especifique o contrário, o MFPlay mostra o vídeo na taxa de proporção correta, usando formato Letterbox, se necessário.</span><span class="sxs-lookup"><span data-stu-id="75012-211">Unless you specify otherwise, MFPlay shows the video at the correct aspect ratio, using letterboxing if needed.</span></span> <span data-ttu-id="75012-212">Se você não quiser preservar a taxa de proporção, chame [**IMFPMediaPlayer:: SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) com o sinalizador **MFVideoARMode \_ None** .</span><span class="sxs-lookup"><span data-stu-id="75012-212">If you do not want to preserve the aspect ratio, call [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) with the **MFVideoARMode\_None** flag.</span></span> <span data-ttu-id="75012-213">Isso fará com que o MFPlay alongue o vídeo para preencher o retângulo inteiro, sem formato letterbox.</span><span class="sxs-lookup"><span data-stu-id="75012-213">This will cause MFPlay to stretch the video to fill the entire rectangle, with no letterboxing.</span></span> <span data-ttu-id="75012-214">Normalmente, você deve usar a configuração padrão e deixar MFPlay Letterbox o vídeo.</span><span class="sxs-lookup"><span data-stu-id="75012-214">Typically you should use the default setting and let MFPlay letterbox the video.</span></span> <span data-ttu-id="75012-215">A cor padrão do Letterbox é preta, mas você pode alterá-la chamando [**IMFPMediaPlayer:: setbordercolor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span><span class="sxs-lookup"><span data-stu-id="75012-215">The default letterbox color is black, but you can change this by calling [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span></span>

## <a name="limitations-of-mfplay"></a><span data-ttu-id="75012-216">Limitações do MFPlay</span><span class="sxs-lookup"><span data-stu-id="75012-216">Limitations of MFPlay</span></span>

<span data-ttu-id="75012-217">A versão atual do MFPlay tem as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="75012-217">The current version of MFPlay has the following limitations:</span></span>

-   <span data-ttu-id="75012-218">MFPlay não oferece suporte a conteúdo protegido por DRM.</span><span class="sxs-lookup"><span data-stu-id="75012-218">MFPlay does not support DRM-protected content.</span></span>
-   <span data-ttu-id="75012-219">Por padrão, o MFPlay não dá suporte a protocolos de streaming de rede.</span><span class="sxs-lookup"><span data-stu-id="75012-219">By default, MFPlay does not support network streaming protocols.</span></span> <span data-ttu-id="75012-220">Para obter mais informações, consulte [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span><span class="sxs-lookup"><span data-stu-id="75012-220">For more information, see [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span>
-   <span data-ttu-id="75012-221">MFPlay não oferece suporte a listas de reprodução do lado do servidor (SSPLs) ou outros tipos de origem que reproduzem mais de um segmento.</span><span class="sxs-lookup"><span data-stu-id="75012-221">MFPlay does not support server-side playlists (SSPLs) or other types of source that play more than one segment.</span></span> <span data-ttu-id="75012-222">Em termos técnicos, MFPlay interrompe a reprodução após a primeira apresentação e ignora todos os eventos [MENewPresentation](menewpresentation.md) da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="75012-222">In technical terms, MFPlay stops playback after the first presentation, and ignores any [MENewPresentation](menewpresentation.md) events from the media source.</span></span>
-   <span data-ttu-id="75012-223">MFPlay não dá suporte a transições diretas entre as fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="75012-223">MFPlay does not support seamless transitions between media sources.</span></span>
-   <span data-ttu-id="75012-224">MFPlay não dá suporte à combinação de vários fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75012-224">MFPlay does not support mixing multiple video streams.</span></span>
-   <span data-ttu-id="75012-225">Somente os formatos de mídia com suporte nativo no Media Foundation são suportados pelo MFPlay.</span><span class="sxs-lookup"><span data-stu-id="75012-225">Only media formats supported natively in Media Foundation are supported by MFPlay.</span></span> <span data-ttu-id="75012-226">(Isso inclui componentes de Media Foundation de terceiros que podem ser instalados no sistema.)</span><span class="sxs-lookup"><span data-stu-id="75012-226">(This includes third-party Media Foundation components that might be installed on the system.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="75012-227">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="75012-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75012-228">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="75012-228">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



