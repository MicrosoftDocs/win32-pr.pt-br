---
description: O MFPlay é uma API para criar aplicativos de reprodução de mídia no C++.
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: Ponto de Partida com MFPlay
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2afb0b20189501530116c252a4d11a9b3e2d8d0dff07482b1998b73400071e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063485"
---
# <a name="getting-started-with-mfplay"></a>Ponto de Partida com MFPlay

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

O MFPlay é uma API para criar aplicativos de reprodução de mídia no C++.

Este tópico contém as seguintes seções:

-   [Requirements](#requirements)
-   [Sobre o MFPlay](#about-mfplay)
-   [Como tocar um arquivo de mídia](#playing-a-media-file)
-   [Controlando a reprodução](#controlling-playback)
-   [Recebendo eventos do player](#receiving-events-from-the-player)
-   [Obter informações sobre um arquivo de mídia](#getting-information-about-a-media-file)
-   [Gerenciando a reprodução de vídeo](#managing-video-playback)
-   [Limitações do MFPlay](#limitations-of-mfplay)
-   [Tópicos relacionados](#related-topics)

## <a name="requirements"></a>Requisitos

O MFPlay requer Windows 7.

## <a name="about-mfplay"></a>Sobre o MFPlay

O MFPlay tem um modelo de programação simples, fornecendo o conjunto principal de recursos de que a maioria dos aplicativos de reprodução precisa. Um aplicativo cria um objeto *de player* que controla a reprodução. Para reproduzir um arquivo de mídia, o objeto player cria um item de *mídia*, que pode ser usado para obter informações sobre o conteúdo do arquivo de mídia. O aplicativo controla a reprodução por meio de métodos na interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) do objeto do player. Opcionalmente, o aplicativo pode obter notificações de eventos por meio de uma interface de retorno de chamada O diagrama a seguir ilustra esse processo.

![diagrama conceitual: o aplicativo e o player apontam um para o outro, ambos apontam para o item de mídia, que aponta para o arquivo de mídia](images/mfplay.png)

## <a name="playing-a-media-file"></a>Como tocar um arquivo de mídia

Para reproduzir um arquivo de mídia, chame a [**função MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)


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



A [**função MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) cria uma nova instância do objeto de player MFPlay. A função assume os seguintes parâmetros:

-   O primeiro parâmetro é a URL do arquivo a ser aberto. Pode ser um arquivo local ou um arquivo em um servidor de mídia.
-   O segundo parâmetro especifica se a reprodução é iniciada automaticamente. Ao definir esse parêntese **como TRUE,** o arquivo será reproduzida assim que o MFPlay o carregar.
-   O terceiro parâmetro define várias opções. Para as opções padrão, passe zero (0).
-   O quarto parâmetro é um ponteiro para uma interface de retorno de chamada opcional. Esse parâmetro pode ser **NULL,** conforme mostrado. O retorno de chamada é descrito na seção [Recebendo eventos do player](#receiving-events-from-the-player).
-   O quinto parâmetro é um handle para a janela do aplicativo. Se o arquivo de mídia contiver um fluxo de vídeo, o vídeo aparecerá dentro da área do cliente dessa janela. Para reprodução somente áudio, esse parâmetro pode ser **NULL.**

O último parâmetro recebe um ponteiro para a interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) do objeto do player.

Antes que o aplicativo seja desligado, certifique-se de liberar o [**ponteiro IMFPMediaPlayer.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) Você pode fazer isso no manipulador **de mensagens WM \_ CLOSE.**


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> Este exemplo usa a [função SafeRelease](saferelease.md) para liberar ponteiros de interface.

 

Para reprodução de vídeo simples, esse é todo o código de que você precisa. O restante deste tutorial mostrará como adicionar mais recursos, começando com como controlar a reprodução.

## <a name="controlling-playback"></a>Controlando a reprodução

O código mostrado na seção anterior reproduzirá o arquivo de mídia até chegar ao final do arquivo. Você pode parar e iniciar a reprodução chamando os seguintes métodos na interface [**IMFPMediaPlayer:**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)

-   [**IMFPMediaPlayer::P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pausa a reprodução. Enquanto a reprodução é pausada, o quadro de vídeo mais recente é exibido e o áudio é silencioso.
-   [**IMFPMediaPlayer::Stop interrompe**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) a reprodução. Nenhum vídeo é exibido e a posição de reprodução é redefinida para o início do arquivo.
-   [**IMFPMediaPlayer::P lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) retoma a reprodução após parar ou pausar.

O código a seguir pausa ou retoma a reprodução quando você pressiona **SPACEBAR**.


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



Este exemplo chama o método [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) para obter o estado de reprodução atual (pausado, interrompido ou reproduzindo) e pausa ou retoma de acordo.

## <a name="receiving-events-from-the-player"></a>Recebendo eventos do player

O MFPlay usa uma interface de retorno de chamada para enviar eventos para seu aplicativo. Há dois motivos para esse retorno de chamada:

-   A reprodução ocorre em um thread separado. Durante a reprodução, determinados eventos podem ocorrer, como atingir o final do arquivo. O MFPlay usa o retorno de chamada para notificar seu aplicativo do evento.
-   Muitos dos métodos [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) são assíncronos, o que significa que eles retornam antes da conclusão da operação. Métodos assíncronos permitem que você inicie uma operação do thread da interface do usuário que pode levar muito tempo para ser concluída, sem que isso faça com que sua interface do usuário bloqueie. Após a conclusão da operação, o MFPlay sinaliza o retorno de chamada.

Para receber notificações de retorno de chamada, implemente a interface [**IMFPMediaPlayerCallback.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) Essa interface herda **IUnknown** e define um único método, [**OnMediaPlayerEvent.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) Para configurar o retorno de chamada, passe um ponteiro para a implementação **de IMFPMediaPlayerCallback** no parâmetro *pCallback* da [**função MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)

Este é o primeiro exemplo deste tutorial, modificado para incluir o retorno de chamada.


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



O [**método OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) tem um único parâmetro, que é um ponteiro para a estrutura DE HEADER DE EVENTO [**\_ \_ MFP.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) O **membro eEventType** dessa estrutura informa qual evento ocorreu. Por exemplo, quando a reprodução é iniciada, o MFPlay envia o **evento MFP \_ EVENT TYPE \_ \_ PLAY.**

Cada tipo de evento tem uma estrutura de dados correspondente que contém informações para esse evento. Cada uma dessas estruturas começa com uma estrutura DE HEADER DE EVENTO [**\_ \_ MFP.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) No retorno de chamada, caste o **ponteiro \_ DO \_ HEADER DE EVENTO MFP** para a estrutura de dados específica do evento. Por exemplo, se o tipo de evento for **MFP \_ PLAY \_ EVENT**, a estrutura de dados será [**MFP \_ PLAY \_ EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event). O código a seguir mostra como manipular esse evento no retorno de chamada.


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



Este exemplo usa o [**evento MFP \_ GET PLAY \_ \_ EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) para lançar o *ponteiro pEventHeader* em uma [**estrutura MFP PLAY \_ \_ EVENT.**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) O **HRESULT** da operação que disparou o evento é armazenado no **campo hrEvent** da estrutura.

Para ver uma lista de todos os tipos de evento e as estruturas de dados correspondentes, consulte [**MFP \_ EVENT \_ TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).

Uma observação sobre o threading: por padrão, o MFPlay invoca o retorno de chamada do mesmo thread que chamou [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer). Esse thread deve ter um loop de mensagem. Como alternativa, você pode passar o sinalizador **MFP \_ OPTION FREE \_ \_ THREADED \_ CALLBACK** no parâmetro *creationOptions* **de MFPCreateMediaPlayer**. Esse sinalizador faz com que o MFPlay invoque retornos de chamada de um thread separado. Qualquer opção tem implicações para seu aplicativo. A opção padrão significa que o retorno de chamada não pode fazer nada que aguarda no loop de mensagem, como aguardar uma ação de interface do usuário, pois isso bloqueará o procedimento de janela. A opção de thread livre significa que você precisa usar seções críticas para proteger todos os dados que acessar no retorno de chamada. Na maioria dos casos, a opção padrão é mais simples.

## <a name="getting-information-about-a-media-file"></a>Obter informações sobre um arquivo de mídia

Quando você abre um arquivo de mídia no MFPlay, o player cria um objeto chamado *um item* de mídia que representa o arquivo de mídia. Esse objeto expõe a interface [**IMFPMediaItem,**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) que você pode usar para obter informações sobre o arquivo de mídia. Muitas das estruturas de evento MFPlay contêm um ponteiro para o item de mídia atual. Você também pode obter o item de mídia atual chamando [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) no player.

Dois métodos particularmente úteis são [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) e [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio). Esses métodos consultam se a fonte de mídia contém vídeo ou áudio.

Por exemplo, o código a seguir testa se o arquivo de mídia atual contém um fluxo de vídeo.


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



Se o arquivo de origem contiver um fluxo de vídeo selecionado para reprodução, *bHasVideo* e *bIsSelected* serão definidos como **TRUE.**

## <a name="managing-video-playback"></a>Gerenciando a reprodução de vídeo

Quando o MFPlay reproduz um arquivo de vídeo, ele desenha o vídeo na janela que você especificou na [**função MFPCreateMediaPlayer.**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) Isso ocorre em um thread separado pertencente ao pipeline Microsoft Media Foundation reprodução. Na maior parte do tempo, seu aplicativo não precisa gerenciar esse processo. No entanto, há duas situações em que o aplicativo deve notificar o MFPlay para atualizar o vídeo.

-   Se a reprodução for pausada ou interrompida, o MFPlay deverá ser notificado sempre que a janela de vídeo do aplicativo receber uma mensagem WM \_ PAINT. Isso permite que o MFPlay repaint a janela.
-   Se a janela for re dimensionada, o MFPlay deverá ser notificado para que possa dimensionar o vídeo para corresponder ao novo tamanho da janela.

O [**método IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) trata ambos os casos. Chame esse método dentro dos manipuladores de mensagens WM PAINT e \_ WM SIZE para a janela de \_ vídeo.

> [!IMPORTANT]
> Chame a função **BeginPaint da** GDI antes de [**chamar UpdateVideo.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)

 


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



A menos que você especifique o contrário, o MFPlay mostrará o vídeo na taxa de proporção correta, usando letterboxing, se necessário. Se você não quiser preservar a taxa de proporção, chame [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) com o sinalizador **MFVideoARMode \_ None.** Isso fará com que o MFPlay alonge o vídeo para preencher todo o retângulo, sem nenhuma caixa de texto. Normalmente, você deve usar a configuração padrão e permitir que o MFPlay faça a caixa de texto do vídeo. A cor da caixa de texto padrão é preta, mas você pode alterar isso chamando [**IMFPMediaPlayer::SetBorderColor.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor)

## <a name="limitations-of-mfplay"></a>Limitações do MFPlay

A versão atual do MFPlay tem as seguintes limitações:

-   O MFPlay não dá suporte a conteúdo protegido por DRM.
-   Por padrão, o MFPlay não dá suporte a protocolos de streaming de rede. Para obter mais informações, [**consulte IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).
-   O MFPlay não dá suporte a SSPLs (playlists do lado do servidor) ou outros tipos de origem que reproduzem mais de um segmento. Em termos técnicos, o MFPlay interrompe a reprodução após a primeira apresentação e ignora todos os eventos [MENewPresentation](menewpresentation.md) da fonte de mídia.
-   O MFPlay não dá suporte a transições perfeitas entre fontes de mídia.
-   O MFPlay não dá suporte à combinação de vários fluxos de vídeo.
-   Somente formatos de mídia com suporte nativo no Media Foundation têm suporte no MFPlay. (Isso inclui componentes de Media Foundation de terceiros que podem ser instalados no sistema.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



