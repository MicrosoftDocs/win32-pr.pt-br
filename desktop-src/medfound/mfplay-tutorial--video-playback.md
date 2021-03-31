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
# <a name="mfplay-tutorial-video-playback"></a><span data-ttu-id="bb874-103">Tutorial do MFPlay: reprodução de vídeo</span><span class="sxs-lookup"><span data-stu-id="bb874-103">MFPlay Tutorial: Video Playback</span></span>

<span data-ttu-id="bb874-104">\[O MFPlay está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="bb874-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bb874-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="bb874-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bb874-106">\]</span><span class="sxs-lookup"><span data-stu-id="bb874-106">\]</span></span>

<span data-ttu-id="bb874-107">Este tutorial apresenta um aplicativo completo que reproduz vídeo usando o MFPlay.</span><span class="sxs-lookup"><span data-stu-id="bb874-107">This tutorial presents a complete application that plays video using MFPlay.</span></span> <span data-ttu-id="bb874-108">Ele se baseia no exemplo do SDK do [SimplePlay](simpleplay-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="bb874-108">It is based on the [SimplePlay](simpleplay-sample.md) SDK sample.</span></span>

<span data-ttu-id="bb874-109">Este tutorial contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="bb874-109">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="bb874-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb874-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bb874-111">Arquivos de cabeçalho e biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb874-111">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="bb874-112">Variáveis globais</span><span class="sxs-lookup"><span data-stu-id="bb874-112">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="bb874-113">Declarar a classe de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="bb874-113">Declare the Callback Class</span></span>](#declare-the-callback-class)
-   [<span data-ttu-id="bb874-114">Declarar a função SafeRelease</span><span class="sxs-lookup"><span data-stu-id="bb874-114">Declare the SafeRelease Function</span></span>](#declare-the-saferelease-function)
-   [<span data-ttu-id="bb874-115">Abrir um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="bb874-115">Open a Media File</span></span>](#open-a-media-file)
-   [<span data-ttu-id="bb874-116">Manipuladores de mensagens de janelas</span><span class="sxs-lookup"><span data-stu-id="bb874-116">Window Message Handlers</span></span>](#window-message-handlers)
-   [<span data-ttu-id="bb874-117">Implementar o método de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="bb874-117">Implement the Callback Method</span></span>](#implement-the-callback-method)
-   [<span data-ttu-id="bb874-118">Implementar WinMain</span><span class="sxs-lookup"><span data-stu-id="bb874-118">Implement WinMain</span></span>](#implement-winmain)
-   [<span data-ttu-id="bb874-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb874-119">Related topics</span></span>](#related-topics)

<span data-ttu-id="bb874-120">Para obter uma discussão mais detalhada sobre a API do MFPlay, consulte [introdução com MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="bb874-120">For a more detailed discussion of the MFPlay API, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb874-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb874-121">Requirements</span></span>

<span data-ttu-id="bb874-122">O MFPlay requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb874-122">MFPlay requires Windows 7.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="bb874-123">Arquivos de cabeçalho e biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb874-123">Header and Library Files</span></span>

<span data-ttu-id="bb874-124">Inclua os seguintes arquivos de cabeçalho em seu projeto:</span><span class="sxs-lookup"><span data-stu-id="bb874-124">Include the following header files in your project:</span></span>


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



<span data-ttu-id="bb874-125">Link para as seguintes bibliotecas de código:</span><span class="sxs-lookup"><span data-stu-id="bb874-125">Link to the following code libraries:</span></span>

-   <span data-ttu-id="bb874-126">mfplay. lib</span><span class="sxs-lookup"><span data-stu-id="bb874-126">mfplay.lib</span></span>
-   <span data-ttu-id="bb874-127">shlwapi. lib</span><span class="sxs-lookup"><span data-stu-id="bb874-127">shlwapi.lib</span></span>

## <a name="global-variables"></a><span data-ttu-id="bb874-128">Variáveis globais</span><span class="sxs-lookup"><span data-stu-id="bb874-128">Global Variables</span></span>

<span data-ttu-id="bb874-129">Declare as seguintes variáveis globais:</span><span class="sxs-lookup"><span data-stu-id="bb874-129">Declare the following global variables:</span></span>


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



<span data-ttu-id="bb874-130">Essas variáveis serão usadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bb874-130">These variables will be used as follows:</span></span>

<dl> <dt>

<span data-ttu-id="bb874-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ HWND*</span><span class="sxs-lookup"><span data-stu-id="bb874-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g\_hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="bb874-132">Um identificador para a janela do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bb874-132">A handle to the application window.</span></span>

</dd> <dt>

<span data-ttu-id="bb874-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*</span><span class="sxs-lookup"><span data-stu-id="bb874-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g\_bVideo*</span></span>
</dt> <dd>

<span data-ttu-id="bb874-134">Um valor booliano que controla se o vídeo está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="bb874-134">A Boolean value that tracks whether video is playing.</span></span>

</dd> <dt>

<span data-ttu-id="bb874-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*</span><span class="sxs-lookup"><span data-stu-id="bb874-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g\_pPlayer*</span></span>
</dt> <dd>

<span data-ttu-id="bb874-136">Um ponteiro para a interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="bb874-136">A pointer to the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="bb874-137">Essa interface é usada para controlar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="bb874-137">This interface is used to control playback.</span></span>

</dd> <dt>

<span data-ttu-id="bb874-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*</span><span class="sxs-lookup"><span data-stu-id="bb874-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g\_pCallback*</span></span>
</dt> <dd>

<span data-ttu-id="bb874-139">Um ponteiro para a interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="bb874-139">A pointer to the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="bb874-140">O aplicativo implementa essa interface de retorno de chamada para obter notificações do objeto Player.</span><span class="sxs-lookup"><span data-stu-id="bb874-140">The application implements this callback interface to get notifications from the player object.</span></span>

</dd> </dl>

## <a name="declare-the-callback-class"></a><span data-ttu-id="bb874-141">Declarar a classe de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="bb874-141">Declare the Callback Class</span></span>

<span data-ttu-id="bb874-142">Para obter notificações de eventos do objeto Player, o aplicativo deve implementar a interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="bb874-142">To get event notifications from the player object, the application must implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="bb874-143">O código a seguir declara uma classe que implementa a interface.</span><span class="sxs-lookup"><span data-stu-id="bb874-143">The following code declares a class that implements the interface.</span></span> <span data-ttu-id="bb874-144">A única variável de membro é *m \_ cRef*, que armazena a contagem de referência.</span><span class="sxs-lookup"><span data-stu-id="bb874-144">The only member variable is *m\_cRef*, which stores the reference count.</span></span>

<span data-ttu-id="bb874-145">Os métodos **IUnknown** são implementados em linha.</span><span class="sxs-lookup"><span data-stu-id="bb874-145">The **IUnknown** methods are implemented inline.</span></span> <span data-ttu-id="bb874-146">A implementação do método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) é mostrada posteriormente; consulte [implementar o método de retorno de chamada](#implement-the-callback-method).</span><span class="sxs-lookup"><span data-stu-id="bb874-146">The implementation of the [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is shown later; see [Implement the Callback Method](#implement-the-callback-method).</span></span>


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



## <a name="declare-the-saferelease-function"></a><span data-ttu-id="bb874-147">Declarar a função SafeRelease</span><span class="sxs-lookup"><span data-stu-id="bb874-147">Declare the SafeRelease Function</span></span>

<span data-ttu-id="bb874-148">Ao longo deste tutorial, a função [SafeRelease](saferelease.md) é usada para liberar ponteiros de interface:</span><span class="sxs-lookup"><span data-stu-id="bb874-148">Throughout this tutorial, the [SafeRelease](saferelease.md) function is used to release interface pointers:</span></span>


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



## <a name="open-a-media-file"></a><span data-ttu-id="bb874-149">Abrir um arquivo de mídia</span><span class="sxs-lookup"><span data-stu-id="bb874-149">Open a Media File</span></span>

<span data-ttu-id="bb874-150">A `PlayMediaFile` função abre um arquivo de mídia, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="bb874-150">The `PlayMediaFile` function opens a media file, as follows:</span></span>

1.  <span data-ttu-id="bb874-151">Se *g \_ PPlayer* for **NULL**, a função chamará [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) para criar uma nova instância do objeto do Media Player.</span><span class="sxs-lookup"><span data-stu-id="bb874-151">If *g\_pPlayer* is **NULL**, the function calls [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create a new instance of the media player object.</span></span> <span data-ttu-id="bb874-152">Os parâmetros de entrada para **MFPCreateMediaPlayer** incluem um ponteiro para a interface de retorno de chamada e um identificador para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bb874-152">The input parameters to **MFPCreateMediaPlayer** include a pointer to the callback interface and a handle to the video window.</span></span>
2.  <span data-ttu-id="bb874-153">Para abrir o arquivo de mídia, a função chama [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passando a URL do arquivo.</span><span class="sxs-lookup"><span data-stu-id="bb874-153">To open the media file, the function calls [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passing in the URL of the file.</span></span> <span data-ttu-id="bb874-154">Esse método é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="bb874-154">This method completes asynchronously.</span></span> <span data-ttu-id="bb874-155">Quando concluído, o método [**IMFPMediaPlayerCallback:: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) do aplicativo é chamado.</span><span class="sxs-lookup"><span data-stu-id="bb874-155">When it completes, the application's [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is called.</span></span>


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



<span data-ttu-id="bb874-156">A `OnFileOpen` função exibe a caixa de diálogo arquivo comum, que permite ao usuário selecionar um arquivo para reprodução.</span><span class="sxs-lookup"><span data-stu-id="bb874-156">The `OnFileOpen` function displays the common file dialog, which enables the user to select a file for playback.</span></span> <span data-ttu-id="bb874-157">A interface **IFileOpenDialog** é usada para exibir a caixa de diálogo arquivo comum.</span><span class="sxs-lookup"><span data-stu-id="bb874-157">The **IFileOpenDialog** interface is used to display the common file dialog.</span></span> <span data-ttu-id="bb874-158">Essa interface faz parte das APIs do shell do Windows; Ele foi introduzido no Windows Vista como uma substituição para a função **GetOpenFileName** mais antiga.</span><span class="sxs-lookup"><span data-stu-id="bb874-158">This interface is part of the Windows Shell APIs; it was introduced in Windows Vista as a replacement for the older **GetOpenFileName** function.</span></span> <span data-ttu-id="bb874-159">Depois que o usuário seleciona um arquivo, `OnFileOpen` chama `PlayMediaFile` para iniciar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="bb874-159">After the user selects a file, `OnFileOpen` calls `PlayMediaFile` to start playback.</span></span>


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



## <a name="window-message-handlers"></a><span data-ttu-id="bb874-160">Manipuladores de mensagens de janelas</span><span class="sxs-lookup"><span data-stu-id="bb874-160">Window Message Handlers</span></span>

<span data-ttu-id="bb874-161">Em seguida, declare manipuladores de mensagens para as seguintes mensagens de janela:</span><span class="sxs-lookup"><span data-stu-id="bb874-161">Next, declare message handlers for the following window messages:</span></span>

-   <span data-ttu-id="bb874-162">**pintura do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bb874-162">**WM\_PAINT**</span></span>
-   <span data-ttu-id="bb874-163">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bb874-163">**WM\_SIZE**</span></span>
-   <span data-ttu-id="bb874-164">**fechar o WM \_**</span><span class="sxs-lookup"><span data-stu-id="bb874-164">**WM\_CLOSE**</span></span>

<span data-ttu-id="bb874-165">Para a mensagem do **WM \_ Paint** , você deve controlar se o vídeo está sendo reproduzido no momento.</span><span class="sxs-lookup"><span data-stu-id="bb874-165">For the **WM\_PAINT** message, you must track whether video is currently playing.</span></span> <span data-ttu-id="bb874-166">Nesse caso, chame o método [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) .</span><span class="sxs-lookup"><span data-stu-id="bb874-166">If so, call the [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method.</span></span> <span data-ttu-id="bb874-167">Esse método faz com que o objeto Player Redesenhe o quadro de vídeo mais recente.</span><span class="sxs-lookup"><span data-stu-id="bb874-167">This method causes the player object to redraw the most recent video frame.</span></span>

<span data-ttu-id="bb874-168">Se não houver vídeo, o aplicativo será responsável por pintar a janela.</span><span class="sxs-lookup"><span data-stu-id="bb874-168">If there is no video, the application is responsible for painting the window.</span></span> <span data-ttu-id="bb874-169">Para este tutorial, o aplicativo simplesmente chama a função **FillRect** do GDI para preencher toda a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="bb874-169">For this tutorial, the application simply calls the GDI **FillRect** function to fill the entire client area.</span></span>


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



<span data-ttu-id="bb874-170">Para a mensagem de **\_ tamanho do WM** , chame [**IMFPMediaPlayer:: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="bb874-170">For the **WM\_SIZE** message, call [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span> <span data-ttu-id="bb874-171">Esse método faz com que o objeto Player reajuste o vídeo para corresponder ao tamanho atual da janela.</span><span class="sxs-lookup"><span data-stu-id="bb874-171">This method causes the player object to readjust the video to match the current size of the window.</span></span> <span data-ttu-id="bb874-172">Observe que **UpdateVideo** é usado tanto para o WM como para o **\_ tamanho** do WM. **\_**</span><span class="sxs-lookup"><span data-stu-id="bb874-172">Note that **UpdateVideo** is used for both **WM\_PAINT** and **WM\_SIZE**.</span></span>


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



<span data-ttu-id="bb874-173">Para a mensagem de **\_ fechamento do WM** , libere os ponteiros [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) e [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="bb874-173">For the **WM\_CLOSE** message, release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) and [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) pointers.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a><span data-ttu-id="bb874-174">Implementar o método de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="bb874-174">Implement the Callback Method</span></span>

<span data-ttu-id="bb874-175">A interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) define um método único, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="bb874-175">The [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="bb874-176">Esse método notifica o aplicativo sempre que um evento ocorre durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="bb874-176">This method notifies the application whenever an event occurs during playback.</span></span> <span data-ttu-id="bb874-177">O método usa um parâmetro, um ponteiro para uma estrutura de [**\_ \_ cabeçalho de evento de MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="bb874-177">The method takes one parameter, a pointer to an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="bb874-178">O membro **eEventType** da estrutura especifica o evento que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="bb874-178">The **eEventType** member of the structure specifies the event that occurred.</span></span>

<span data-ttu-id="bb874-179">A estrutura do [**\_ \_ cabeçalho do evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pode ser seguida por dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="bb874-179">The [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure may be followed by additional data.</span></span> <span data-ttu-id="bb874-180">Para cada tipo de evento, é definida uma macro que converte o ponteiro do **\_ \_ cabeçalho do evento MFP** em uma estrutura específica do evento.</span><span class="sxs-lookup"><span data-stu-id="bb874-180">For each event type, a macro is defined that casts the **MFP\_EVENT\_HEADER** pointer to an event-specific structure.</span></span> <span data-ttu-id="bb874-181">(Consulte [**\_ \_ tipo de evento MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span><span class="sxs-lookup"><span data-stu-id="bb874-181">(See [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span></span>

<span data-ttu-id="bb874-182">Para este tutorial, dois eventos são significativos:</span><span class="sxs-lookup"><span data-stu-id="bb874-182">For this tutorial, two events are significant:</span></span>



| <span data-ttu-id="bb874-183">Evento</span><span class="sxs-lookup"><span data-stu-id="bb874-183">Event</span></span>                                    | <span data-ttu-id="bb874-184">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb874-184">Description</span></span>                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb874-185">**\_tipo de evento MFP \_ \_ MEDIAITEM \_ criado**</span><span class="sxs-lookup"><span data-stu-id="bb874-185">**MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED**</span></span> | <span data-ttu-id="bb874-186">Enviado quando o [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) é concluído.</span><span class="sxs-lookup"><span data-stu-id="bb874-186">Sent when the [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) completes.</span></span> |
| <span data-ttu-id="bb874-187">**\_conjunto de eventos do tipo de evento MFP \_ \_ MEDIAITEM \_**</span><span class="sxs-lookup"><span data-stu-id="bb874-187">**MFP\_EVENT\_TYPE\_MEDIAITEM\_SET**</span></span>     | <span data-ttu-id="bb874-188">Enviado quando o [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) é concluído.</span><span class="sxs-lookup"><span data-stu-id="bb874-188">Sent when [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) completes.</span></span>                         |



 

<span data-ttu-id="bb874-189">O código a seguir mostra como converter o ponteiro do [**\_ \_ cabeçalho do evento MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) para a estrutura específica do evento.</span><span class="sxs-lookup"><span data-stu-id="bb874-189">The following code shows how to cast the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pointer to the event-specific structure.</span></span>


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



<span data-ttu-id="bb874-190">O evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ created** notifica o aplicativo que o método [**IMFPMediaPlayer:: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) foi concluído.</span><span class="sxs-lookup"><span data-stu-id="bb874-190">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event notifies the application that the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method has completed.</span></span> <span data-ttu-id="bb874-191">A estrutura de eventos contém um ponteiro para a interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , que representa o item de mídia criado a partir da URL.</span><span class="sxs-lookup"><span data-stu-id="bb874-191">The event structure contains a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which represents the media item created from the URL.</span></span> <span data-ttu-id="bb874-192">Para enfileirar o item para reprodução, passe este ponteiro para o método [**IMFPMediaPlayer:: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :</span><span class="sxs-lookup"><span data-stu-id="bb874-192">To queue the item for playback, pass this pointer to the [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method:</span></span>


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



<span data-ttu-id="bb874-193">O evento de **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** notifica o aplicativo que o [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) foi concluído.</span><span class="sxs-lookup"><span data-stu-id="bb874-193">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event notifies the application that [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) has completed.</span></span> <span data-ttu-id="bb874-194">Chame [**IMFPMediaPlayer::P deite**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) para iniciar a reprodução:</span><span class="sxs-lookup"><span data-stu-id="bb874-194">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback:</span></span>


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



## <a name="implement-winmain"></a><span data-ttu-id="bb874-195">Implementar WinMain</span><span class="sxs-lookup"><span data-stu-id="bb874-195">Implement WinMain</span></span>

<span data-ttu-id="bb874-196">No restante deste tutorial, não há chamadas para Media Foundation APIs.</span><span class="sxs-lookup"><span data-stu-id="bb874-196">In the remainder of this tutorial, there are no calls to Media Foundation APIs.</span></span> <span data-ttu-id="bb874-197">O código a seguir mostra o procedimento de janela:</span><span class="sxs-lookup"><span data-stu-id="bb874-197">The following code shows the window procedure:</span></span>


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



<span data-ttu-id="bb874-198">A `InitializeWindow` função registra a classe Window do aplicativo e cria a janela.</span><span class="sxs-lookup"><span data-stu-id="bb874-198">The `InitializeWindow` function registers the application's window class and creates the window.</span></span>


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



<span data-ttu-id="bb874-199">Por fim, implemente o ponto de entrada do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="bb874-199">Finally, implement the application entry point:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="bb874-200">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb874-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb874-201">Usando o MFPlay para reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="bb874-201">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



