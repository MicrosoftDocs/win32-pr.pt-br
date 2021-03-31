---
description: Este tutorial apresenta um aplicativo completo que reproduz vídeo usando o MFPlay.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'Tutorial do MFPlay: reprodução de vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bbadae22e72799c64a42d09b6eed904b56a60d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661830"
---
# <a name="mfplay-tutorial-video-playback"></a>Tutorial do MFPlay: reprodução de vídeo

\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. \]

Este tutorial apresenta um aplicativo completo que reproduz vídeo usando o MFPlay. Ele se baseia no exemplo do SDK do [SimplePlay](simpleplay-sample.md) .

Este tutorial contém as seguintes seções:

-   [Requisitos](#requirements)
-   [Arquivos de cabeçalho e biblioteca](#header-and-library-files)
-   [Variáveis globais](#global-variables)
-   [Declarar a classe de retorno de chamada](#declare-the-callback-class)
-   [Declarar a função SafeRelease](#declare-the-saferelease-function)
-   [Abrir um arquivo de mídia](#open-a-media-file)
-   [Manipuladores de mensagens de janelas](#window-message-handlers)
-   [Implementar o método de retorno de chamada](#implement-the-callback-method)
-   [Implementar WinMain](#implement-winmain)
-   [Tópicos relacionados](#related-topics)

Para obter uma discussão mais detalhada sobre a API do MFPlay, consulte [introdução com MFPlay](getting-started-with-mfplay.md).

## <a name="requirements"></a>Requisitos

O MFPlay requer o Windows 7.

## <a name="header-and-library-files"></a>Arquivos de cabeçalho e biblioteca

Inclua os seguintes arquivos de cabeçalho em seu projeto:


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <new>
#include <windows.h>
#include <windowsx.h>
#include <mfplay.h>
#include <mferror.h>
#include <shobjidl.h>   // defines IFileOpenDialog
#include <strsafe.h>
#include <Shlwapi.h>
```



Link para as seguintes bibliotecas de código:

-   mfplay. lib
-   shlwapi. lib

## <a name="global-variables"></a>Variáveis globais

Declare as seguintes variáveis globais:


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



Essas variáveis serão usadas da seguinte maneira:

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ HWND*
</dt> <dd>

Um identificador para a janela do aplicativo.

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*
</dt> <dd>

Um valor booliano que controla se o vídeo está sendo reproduzido.

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*
</dt> <dd>

Um ponteiro para a interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) . Essa interface é usada para controlar a reprodução.

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*
</dt> <dd>

Um ponteiro para a interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . O aplicativo implementa essa interface de retorno de chamada para obter notificações do objeto Player.

</dd> </dl>

## <a name="declare-the-callback-class"></a>Declarar a classe de retorno de chamada

Para obter notificações de eventos do objeto Player, o aplicativo deve implementar a interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . O código a seguir declara uma classe que implementa a interface. A única variável de membro é *m \_ cRef*, que armazena a contagem de referência.

Os métodos **IUnknown** são implementados em linha. A implementação do método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) é mostrada posteriormente; consulte [implementar o método de retorno de chamada](#implement-the-callback-method).


```C++
// Implements the callback interface for MFPlay events.

class MediaPlayerCallback : public IMFPMediaPlayerCallback
{
    long m_cRef; // Reference count

public:

    MediaPlayerCallback() : m_cRef(1)
    {
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(MediaPlayerCallback, IMFPMediaPlayerCallback),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    // IMFPMediaPlayerCallback methods
    IFACEMETHODIMP_(void) OnMediaPlayerEvent(MFP_EVENT_HEADER *pEventHeader);
};
```



## <a name="declare-the-saferelease-function"></a>Declarar a função SafeRelease

Ao longo deste tutorial, a função [SafeRelease](saferelease.md) é usada para liberar ponteiros de interface:


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="open-a-media-file"></a>Abrir um arquivo de mídia

A `PlayMediaFile` função abre um arquivo de mídia, da seguinte maneira:

1.  Se *g \_ PPlayer* for **NULL**, a função chamará [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para criar uma nova instância do objeto do Media Player. Os parâmetros de entrada para **MFPCreateMediaPlayer** incluem um ponteiro para a interface de retorno de chamada e um identificador para a janela de vídeo.
2.  Para abrir o arquivo de mídia, a função chama [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passando a URL do arquivo. Esse método é concluído de forma assíncrona. Quando concluído, o método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) do aplicativo é chamado.


```C++
HRESULT PlayMediaFile(HWND hwnd, PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    // Create the MFPlayer object.
    if (g_pPlayer == NULL)
    {
        g_pPlayerCB = new (std::nothrow) MediaPlayerCallback();

        if (g_pPlayerCB == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFPCreateMediaPlayer(
            NULL,
            FALSE,          // Start playback automatically?
            0,              // Flags
            g_pPlayerCB,    // Callback pointer
            hwnd,           // Video window
            &g_pPlayer
            );
    }

    // Create a new media item for this URL.

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromURL(pszURL, FALSE, 0, NULL);
    }

    // The CreateMediaItemFromURL method completes asynchronously.
    // The application will receive an MFP_EVENT_TYPE_MEDIAITEM_CREATED
    // event. See MediaPlayerCallback::OnMediaPlayerEvent().

    return hr;
}
```



A `OnFileOpen` função exibe a caixa de diálogo arquivo comum, que permite ao usuário selecionar um arquivo para reprodução. A interface **IFileOpenDialog** é usada para exibir a caixa de diálogo arquivo comum. Essa interface faz parte das APIs do shell do Windows; Ele foi introduzido no Windows Vista como uma substituição para a função **GetOpenFileName** mais antiga. Depois que o usuário seleciona um arquivo, `OnFileOpen` chama `PlayMediaFile` para iniciar a reprodução.


```C++
void OnFileOpen(HWND hwnd)
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;
    PWSTR pwszFilePath = NULL;

    // Create the FileOpenDialog object.
    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL,
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->SetTitle(L"Select a File to Play");
    }

    // Show the file-open dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(hwnd);
    }

    if (hr == HRESULT_FROM_WIN32(ERROR_CANCELLED))
    {
        // User canceled.
        SafeRelease(&pFileOpen);
        return;
    }

    // Get the file name from the dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pItem->GetDisplayName(SIGDN_URL, &pwszFilePath);
    }

    // Open the media file.
    if (SUCCEEDED(hr))
    {
        hr = PlayMediaFile(hwnd, pwszFilePath);
    }

    if (FAILED(hr))
    {
        ShowErrorMessage(L"Could not open file.", hr);
    }

    CoTaskMemFree(pwszFilePath);

    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
}
```



## <a name="window-message-handlers"></a>Manipuladores de mensagens de janelas

Em seguida, declare manipuladores de mensagens para as seguintes mensagens de janela:

-   **pintura do WM \_**
-   **tamanho do WM \_**
-   **fechar o WM \_**

Para a mensagem do **WM \_ Paint** , você deve controlar se o vídeo está sendo reproduzido no momento. Nesse caso, chame o método [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) . Esse método faz com que o objeto Player Redesenhe o quadro de vídeo mais recente.

Se não houver vídeo, o aplicativo será responsável por pintar a janela. Para este tutorial, o aplicativo simplesmente chama a função **FillRect** do GDI para preencher toda a área do cliente.


```C++
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_bHasVideo)
    {
        // Playback has started and there is video.

        // Do not draw the window background, because the video
        // frame fills the entire client area.

        g_pPlayer->UpdateVideo();
    }
    else
    {
        // There is no video stream, or playback has not started.
        // Paint the entire client area.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}
```



Para a mensagem de **\_ tamanho do WM** , chame [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo). Esse método faz com que o objeto Player reajuste o vídeo para corresponder ao tamanho atual da janela. Observe que **UpdateVideo** é usado tanto para o WM como para o **\_ tamanho** do WM. **\_**


```C++
void OnSize(HWND /*hwnd*/, UINT state, int /*cx*/, int /*cy*/)
{
    if (state == SIZE_RESTORED)
    {
        if (g_pPlayer)
        {
            // Resize the video.
            g_pPlayer->UpdateVideo();
        }
    }
}
```



Para a mensagem de **\_ fechamento do WM** , libere os ponteiros [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) e [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>Implementar o método de retorno de chamada

A interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) define um método único, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Esse método notifica o aplicativo sempre que um evento ocorre durante a reprodução. O método usa um parâmetro, um ponteiro para uma estrutura de [**\_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . O membro **eEventType** da estrutura especifica o evento que ocorreu.

A estrutura do [**\_ \_ cabeçalho do evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pode ser seguida por dados adicionais. Para cada tipo de evento, é definida uma macro que converte o ponteiro do **\_ \_ cabeçalho do evento MFP** em uma estrutura específica do evento. (Consulte [**\_ \_ tipo de evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)

Para este tutorial, dois eventos são significativos:



| Evento                                    | Descrição                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **\_tipo de evento MFP \_ \_ MEDIAITEM \_ criado** | Enviado quando o [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) é concluído. |
| **\_conjunto de eventos do tipo de evento MFP \_ \_ MEDIAITEM \_**     | Enviado quando o [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) é concluído.                         |



 

O código a seguir mostra como converter o ponteiro do [**\_ \_ cabeçalho do evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) para a estrutura específica do evento.


```C++
void MediaPlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    if (FAILED(pEventHeader->hrEvent))
    {
        ShowErrorMessage(L"Playback error", pEventHeader->hrEvent);
        return;
    }

    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_MEDIAITEM_CREATED:
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET:
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader));
        break;
    }
}
```



O evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ created** notifica o aplicativo que o método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) foi concluído. A estrutura de eventos contém um ponteiro para a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que representa o item de mídia criado a partir da URL. Para enfileirar o item para reprodução, passe este ponteiro para o método [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    // The media item was created successfully.

    if (g_pPlayer)
    {
        BOOL    bHasVideo = FALSE;
        BOOL    bIsSelected = FALSE;

        // Check if the media item contains video.
        HRESULT hr = pEvent->pMediaItem->HasVideo(&bHasVideo, &bIsSelected);
        if (SUCCEEDED(hr))
        {
            g_bHasVideo = bHasVideo && bIsSelected;

            // Set the media item on the player. This method completes
            // asynchronously.
            hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
        }

        if (FAILED(hr))
        {
            ShowErrorMessage(L"Error playing this file.", hr);
        }
   }
}
```



O evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** notifica o aplicativo que o [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) foi concluído. Chame [**IMFPMediaPlayer::P deite**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar a reprodução:


```C++
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT * /*pEvent*/)
{
    HRESULT hr = g_pPlayer->Play();
    if (FAILED(hr))
    {
        ShowErrorMessage(L"IMFPMediaPlayer::Play failed.", hr);
    }
}
```



## <a name="implement-winmain"></a>Implementar WinMain

No restante deste tutorial, não há chamadas para Media Foundation APIs. O código a seguir mostra o procedimento de janela:


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        HANDLE_MSG(hwnd, WM_CLOSE,   OnClose);
        HANDLE_MSG(hwnd, WM_PAINT,   OnPaint);
        HANDLE_MSG(hwnd, WM_COMMAND, OnCommand);
        HANDLE_MSG(hwnd, WM_SIZE,    OnSize);

    case WM_ERASEBKGND:
        return 1;

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam);
    }
}
```



A `InitializeWindow` função registra a classe Window do aplicativo e cria a janela.


```C++
BOOL InitializeWindow(HWND *pHwnd)
{
    const wchar_t CLASS_NAME[]  = L"MFPlay Window Class";
    const wchar_t WINDOW_NAME[] = L"MFPlay Sample Application";

    WNDCLASS wc = {};

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = GetModuleHandle(NULL);
    wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wc.lpszClassName = CLASS_NAME;
    wc.lpszMenuName  = MAKEINTRESOURCE(IDR_MENU1);

    RegisterClass(&wc);

    HWND hwnd = CreateWindow(
        CLASS_NAME, WINDOW_NAME, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,
        NULL, NULL, GetModuleHandle(NULL), NULL);

    if (!hwnd)
    {
        return FALSE;
    }

    ShowWindow(hwnd, SW_SHOWDEFAULT);
    UpdateWindow(hwnd);

    *pHwnd = hwnd;

    return TRUE;
}
```



Por fim, implemente o ponto de entrada do aplicativo:


```C++
int WINAPI wWinMain(HINSTANCE, HINSTANCE, PWSTR, int)
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    HRESULT hr = CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        return 0;
    }

    HWND hwnd = NULL;
    if (InitializeWindow(&hwnd))
    {
        // Message loop
        MSG msg = {};
        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }

        DestroyWindow(hwnd);
    }
    CoUninitialize();

    return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o MFPlay para reprodução de áudio/vídeo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



