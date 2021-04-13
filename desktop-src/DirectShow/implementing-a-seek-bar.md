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
# <a name="implementing-a-seek-bar"></a>Implementando uma barra de busca

Esta seção descreve como implementar uma barra de busca para um aplicativo de player de mídia. A barra de busca é implementada como um controle TrackBar. Para obter uma visão geral de como procurar no DirectShow, consulte [buscando o grafo de filtro](seeking-the-filter-graph.md).

Quando o aplicativo for iniciado, inicialize o TrackBar:


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



O TrackBar será desabilitado até que o usuário abra um arquivo de mídia. O intervalo TrackBar é definido de 0 a 100. Durante a reprodução do arquivo, o aplicativo calculará a posição de reprodução como uma porcentagem da duração do arquivo e atualizará o TrackBar de acordo. Por exemplo, a posição TrackBar "50" sempre corresponde ao meio do arquivo.

Quando o usuário abre um arquivo, cria um grafo de reprodução de arquivo usando o **RenderFile**. O código para isso é mostrado em [como reproduzir um arquivo](how-to-play-a-file.md). Em seguida, consulte o Gerenciador do grafo de filtro para a interface **IMediaSeeking** e armazene o ponteiro de interface:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Para determinar se o arquivo é pesquisável, chame o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) ou o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . Esses métodos fazem quase a mesma coisa, mas sua semântica é um pouco diferente. O exemplo a seguir usa **CheckCapabilites**:


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



O \_ sinalizador am buscando \_ CanSeekAbsolute verifica se o arquivo de origem é pesquisável e se o \_ sinalizador am buscando \_ CanGetDuration verifica se a duração do arquivo pode ser determinada com antecedência. Se ambos os recursos tiverem suporte, o aplicativo habilitará o TrackBar e recuperará a duração do arquivo.

Se o grafo for pesquisável, o aplicativo usará um temporizador para atualizar a posição TrackBar durante a reprodução. Ao executar o gráfico de filtro para executar o arquivo, inicie o evento de timer chamando uma das funções de temporizador do Windows, como **SetTimer**. Para obter mais informações sobre temporizadores, consulte o tópico "timers" no Platform SDK.


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



Use o evento timer para atualizar a posição do TrackBar. Chame [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar a posição de reprodução do Currant e, em seguida, calcule a posição como uma porcentagem da duração do arquivo:


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



O usuário também pode mover o TrackBar para buscar o arquivo. Quando o usuário arrasta ou clica no controle TrackBar, o aplicativo recebe um evento do WM \_ HSCROLL. A palavra baixa do parâmetro *wParam* é a mensagem de notificação TrackBar. Por exemplo, \_ a faixa de extremidade de TB é enviada ao final da ação TrackBar e TB \_ THUMBTRACK é enviado continuamente enquanto o usuário arrasta o TrackBar. O código a seguir mostra uma maneira de manipular a \_ mensagem do WM HSCROLL:


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



Se o usuário arrastar o TrackBar, o aplicativo emitirá uma série de comandos de busca, um para cada \_ mensagem de TB THUMBTRACK que receber. Para tornar as operações de busca o mais suaves possível, o aplicativo pausa o grafo. Pausar o grafo interrompe a reprodução, mas garante que a janela de vídeo seja atualizada. Quando o aplicativo recebe a \_ mensagem de endtrack de TB, ele restaura o grafo para seu estado original.

 

 



