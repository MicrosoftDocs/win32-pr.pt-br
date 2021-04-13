---
description: Implementando uma barra de busca
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Implementando uma barra de busca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500590"
---
# <a name="implementing-a-seek-bar"></a><span data-ttu-id="0218b-103">Implementando uma barra de busca</span><span class="sxs-lookup"><span data-stu-id="0218b-103">Implementing a Seek Bar</span></span>

<span data-ttu-id="0218b-104">Esta seção descreve como implementar uma barra de busca para um aplicativo de player de mídia.</span><span class="sxs-lookup"><span data-stu-id="0218b-104">This section describes how to implement a seek bar for a media-player application.</span></span> <span data-ttu-id="0218b-105">A barra de busca é implementada como um controle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0218b-105">The seek bar is implemented as a trackbar control.</span></span> <span data-ttu-id="0218b-106">Para obter uma visão geral de como procurar no DirectShow, consulte [buscando o grafo de filtro](seeking-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="0218b-106">For an overview of seeking in DirectShow, see [Seeking the Filter Graph](seeking-the-filter-graph.md).</span></span>

<span data-ttu-id="0218b-107">Quando o aplicativo for iniciado, inicialize o TrackBar:</span><span class="sxs-lookup"><span data-stu-id="0218b-107">When the application starts, initialize the trackbar:</span></span>


```C++
void InitSlider(HWND hwnd) 
{
    // Initialize the trackbar range, but disable the 
    // control until the user opens a file.
    hScroll = GetDlgItem(hwnd, IDC_SLIDER1);
    EnableWindow(hScroll, FALSE);
    SendMessage(hScroll, TBM_SETRANGE, TRUE, MAKELONG(0, 100));
}
```



<span data-ttu-id="0218b-108">O TrackBar será desabilitado até que o usuário abra um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="0218b-108">The trackbar is disabled until the user opens a media file.</span></span> <span data-ttu-id="0218b-109">O intervalo TrackBar é definido de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="0218b-109">The trackbar range is set from 0 to 100.</span></span> <span data-ttu-id="0218b-110">Durante a reprodução do arquivo, o aplicativo calculará a posição de reprodução como uma porcentagem da duração do arquivo e atualizará o TrackBar de acordo.</span><span class="sxs-lookup"><span data-stu-id="0218b-110">During file playback, the application will calculate the playback position as a percentage of the file duration, and update the trackbar accordingly.</span></span> <span data-ttu-id="0218b-111">Por exemplo, a posição TrackBar "50" sempre corresponde ao meio do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0218b-111">For example, trackbar position "50" always corresponds to the middle of the file.</span></span>

<span data-ttu-id="0218b-112">Quando o usuário abre um arquivo, cria um grafo de reprodução de arquivo usando o **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="0218b-112">When the user opens a file, build a file-playback graph using **RenderFile**.</span></span> <span data-ttu-id="0218b-113">O código para isso é mostrado em [como reproduzir um arquivo](how-to-play-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="0218b-113">The code for this is shown in [How To Play a File](how-to-play-a-file.md).</span></span> <span data-ttu-id="0218b-114">Em seguida, consulte o Gerenciador do grafo de filtro para a interface **IMediaSeeking** e armazene o ponteiro de interface:</span><span class="sxs-lookup"><span data-stu-id="0218b-114">Then query the Filter Graph Manager for the **IMediaSeeking** interface and store the interface pointer:</span></span>


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



<span data-ttu-id="0218b-115">Para determinar se o arquivo é pesquisável, chame o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) ou o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="0218b-115">To determine whether the file is seekable, call either the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method or the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="0218b-116">Esses métodos fazem quase a mesma coisa, mas sua semântica é um pouco diferente.</span><span class="sxs-lookup"><span data-stu-id="0218b-116">These methods do almost the same thing, but their semantics are slightly different.</span></span> <span data-ttu-id="0218b-117">O exemplo a seguir usa **CheckCapabilites**:</span><span class="sxs-lookup"><span data-stu-id="0218b-117">The following example uses **CheckCapabilites**:</span></span>


```C++
// Determine if the source is seekable.
BOOL  bCanSeek = FALSE;
DWORD caps = AM_SEEKING_CanSeekAbsolute | AM_SEEKING_CanGetDuration; 
bCanSeek = (S_OK == pSeek->CheckCapabilities(&caps));
if (bCanSeek)
{
    // Enable the trackbar.
    EnableWindow(hScroll, TRUE);

    // Find the file duration.
    pSeek->GetDuration(&g_rtTotalTime);
}
```



<span data-ttu-id="0218b-118">O \_ sinalizador am buscando \_ CanSeekAbsolute verifica se o arquivo de origem é pesquisável e se o \_ sinalizador am buscando \_ CanGetDuration verifica se a duração do arquivo pode ser determinada com antecedência.</span><span class="sxs-lookup"><span data-stu-id="0218b-118">The AM\_SEEKING\_CanSeekAbsolute flag checks whether the source file is seekable, and the AM\_SEEKING\_CanGetDuration flag checks whether the duration of the file can be determined in advance.</span></span> <span data-ttu-id="0218b-119">Se ambos os recursos tiverem suporte, o aplicativo habilitará o TrackBar e recuperará a duração do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0218b-119">If both of the capabilities are supported, the application enables the trackbar and retrieves the file duration.</span></span>

<span data-ttu-id="0218b-120">Se o grafo for pesquisável, o aplicativo usará um temporizador para atualizar a posição TrackBar durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="0218b-120">If the graph is seekable, the application will use a timer to update the trackbar position during playback.</span></span> <span data-ttu-id="0218b-121">Ao executar o gráfico de filtro para executar o arquivo, inicie o evento de timer chamando uma das funções de temporizador do Windows, como **SetTimer**.</span><span class="sxs-lookup"><span data-stu-id="0218b-121">When you run the filter graph to play the file, start the timer event by calling one of the Windows timer functions, such as **SetTimer**.</span></span> <span data-ttu-id="0218b-122">Para obter mais informações sobre temporizadores, consulte o tópico "timers" no Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="0218b-122">For more information about timers, see the topic "Timers" in the Platform SDK.</span></span>


```C++
void StartPlayback(HWND hwnd) 
{
    pControl->Run();
    if (bCanSeek)
    {
        StopTimer(); // Make sure an old timer is not still active.
        nTimerID = SetTimer(hwnd, IDT_TIMER1, TICK_FREQ, (TIMERPROC)NULL);
        if (nTimerID == 0)
        {
            /* Handle Error */
        }
    }
}

void StopTimer() 
{
    if (wTimerID != 0)
    {
        KillTimer(g_hwnd, wTimerID);
        wTimerID = 0;
    }
}
```



<span data-ttu-id="0218b-123">Use o evento timer para atualizar a posição do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0218b-123">Use the timer event to update the position of the trackbar.</span></span> <span data-ttu-id="0218b-124">Chame [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar a posição de reprodução do Currant e, em seguida, calcule a posição como uma porcentagem da duração do arquivo:</span><span class="sxs-lookup"><span data-stu-id="0218b-124">Call [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) to retrieve the currant playback position, and then calculate the position as a percentage of the file duration:</span></span>


```C++
case WM_TIMER:
    if (wParam == IDT_TIMER1)
    {
        // Timer should not be running unless we really can seek.
        ASSERT(bCanSeek == TRUE);

        REFERENCE_TIME timeNow;
        if (SUCCEEDED(pSeek->GetCurrentPosition(&timeNow)))
        {
            long sliderTick = (long)((timeNow * 100) / g_rtTotalTime);
            SendMessage( hScroll, TBM_SETPOS, TRUE, sliderTick );
        }
    }
    break;
```



<span data-ttu-id="0218b-125">O usuário também pode mover o TrackBar para buscar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0218b-125">The user can also move the trackbar to seek the file.</span></span> <span data-ttu-id="0218b-126">Quando o usuário arrasta ou clica no controle TrackBar, o aplicativo recebe um evento do WM \_ HSCROLL.</span><span class="sxs-lookup"><span data-stu-id="0218b-126">When the user drags or clicks the trackbar control, the application receives a WM\_HSCROLL event.</span></span> <span data-ttu-id="0218b-127">A palavra baixa do parâmetro *wParam* é a mensagem de notificação TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0218b-127">The low word of the *wParam* parameter is the trackbar notification message.</span></span> <span data-ttu-id="0218b-128">Por exemplo, \_ a faixa de extremidade de TB é enviada ao final da ação TrackBar e TB \_ THUMBTRACK é enviado continuamente enquanto o usuário arrasta o TrackBar.</span><span class="sxs-lookup"><span data-stu-id="0218b-128">For example, TB\_ENDTRACK is sent at the end of the trackbar action, and TB\_THUMBTRACK is sent continuously while the user drags the trackbar.</span></span> <span data-ttu-id="0218b-129">O código a seguir mostra uma maneira de manipular a \_ mensagem do WM HSCROLL:</span><span class="sxs-lookup"><span data-stu-id="0218b-129">The following code shows one way to handle the WM\_HSCROLL message:</span></span>


```C++
static OAFilterState state;
static BOOL bStartOfScroll = TRUE;

case WM_HSCROLL:
    short int userReq = LOWORD(wParam);
    if (userReq == TB_ENDTRACK || userReq == TB_THUMBTRACK)
    {
        DWORD dwPosition  = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
        // Pause when the scroll action begins.
        if (bStartOfScroll) 
        {
            pControl->GetState(10, &state);
            bStartOfScroll = FALSE;
            pControl->Pause();
        }
        // Update the position continuously.
        REFERENCE_TIME newTime = (g_rtTotalTime/100) * dwPosition;
        pSeek->SetPositions(&newTime, AM_SEEKING_AbsolutePositioning,
            NULL, AM_SEEKING_NoPositioning);

        // Restore the state at the end.
        if (userReq == TB_ENDTRACK)
        {
            if (state == State_Stopped)
                pControl->Stop();
            else if (state == State_Running) 
                pControl->Run();
            bStartOfScroll = TRUE;
        }
    }
}
```



<span data-ttu-id="0218b-130">Se o usuário arrastar o TrackBar, o aplicativo emitirá uma série de comandos de busca, um para cada \_ mensagem de TB THUMBTRACK que receber.</span><span class="sxs-lookup"><span data-stu-id="0218b-130">If the user drags the trackbar, the application issues a series of seek commands, one for each TB\_THUMBTRACK message that it receives.</span></span> <span data-ttu-id="0218b-131">Para tornar as operações de busca o mais suaves possível, o aplicativo pausa o grafo.</span><span class="sxs-lookup"><span data-stu-id="0218b-131">To make the seek operations as smooth as possible, the application pauses the graph.</span></span> <span data-ttu-id="0218b-132">Pausar o grafo interrompe a reprodução, mas garante que a janela de vídeo seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="0218b-132">Pausing the graph halts playback but ensures that the video window is updated.</span></span> <span data-ttu-id="0218b-133">Quando o aplicativo recebe a \_ mensagem de endtrack de TB, ele restaura o grafo para seu estado original.</span><span class="sxs-lookup"><span data-stu-id="0218b-133">When the application receives the TB\_ENDTRACK message, it restores the graph to its original state.</span></span>

 

 



