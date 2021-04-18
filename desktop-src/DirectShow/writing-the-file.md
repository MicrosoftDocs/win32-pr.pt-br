---
description: Gravando o arquivo
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Gravando o arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda23b144956ab5afca9dd733b29a6f9d639cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760080"
---
# <a name="writing-the-file"></a>Gravando o arquivo

Para gravar o arquivo, basta executar o gráfico de filtro chamando o método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . Aguarde até que a reprodução seja concluída e pare explicitamente o grafo chamando [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); caso contrário, o arquivo não será gravado corretamente.

Para exibir o progresso da operação de gravação de arquivo, consulte o filtro Mux para a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Chame o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) para recuperar a duração do arquivo. Periodicamente, enquanto o grafo está em execução, chame o método [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar a posição atual do grafo no fluxo. A posição atual dividida por duração fornece a porcentagem concluída.

> [!Note]  
> Um aplicativo geralmente consulta o Gerenciador do grafo de filtro para **IMediaSeeking**, mas a gravação de arquivos é uma exceção a essa regra. O Gerenciador de gráfico de filtro calcula a posição atual a partir da posição inicial e o tempo de execução do grafo, o que é preciso para a reprodução de arquivos, mas não para a gravação de arquivos. Portanto, para obter um resultado preciso, você deve recuperar a posição do filtro MUX.

 

O código a seguir obtém a duração do arquivo, inicia um temporizador para atualizar a interface do usuário do aplicativo e executa o gráfico de filtro. (A verificação de erro é omitida para fins de clareza.)


```C++
IMediaSeeking *pSeek = NULL;
IMediaEventEx *pEvent = NULL;
IMediaControl *pControl = NULL;
REFERENCE_TIME rtTotal;

// Query for interfaces. Remember to release them later.
hr = pMux->QueryInterface(IID_IMediaSeeking, (void**)&pSeek);
hr = pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEvent);
hr = pGraph->QueryInterface(IID_IMediaControl, (void**)&pControl);

// Error checking is omitted for clarity.

// Set the DirectShow event notification window.
hr = pEvent->SetNotifyWindow((OAHWND)hwnd, WM_GRAPHNOTIFY, 0);

// Set the range of the progress bar to the file length (in seconds).
hr = pSeek->GetDuration(&rtTotal);
SendDlgItemMessage(hwnd, IDC_PROGRESS1, PBM_SETRANGE, 0, 
   MAKELPARAM(0, rtTotal / 10000000));
// Start the timer.
UINT_PTR res = SetTimer(hwnd, nIDEvent, 100, NULL);
// Run the graph.
pControl->Run();
```



Quando o aplicativo recebe um evento de timer, ele pode atualizar a interface do usuário com a posição atual:


```C++
void OnTimer(HWND hDlg, IMediaSeeking *pSeek)
{
    REFERENCE_TIME rtNow;
    HRESULT hr = pSeek->GetCurrentPosition(&rtNow);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(hDlg, IDC_PROGRESS1, PBM_SETPOS, rtNow/10000000, 0);
    }
}
```



Quando o aplicativo recebe um evento de conclusão do DirectShow, ele deve parar o grafo, conforme mostrado no código a seguir:


```C++
// Application window procedure
LRESULT CALLBACK WndProc(HWND hDlg, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    /*  ...  */
    case WM_GRAPHNOTIFY:
        DoHandleEvent();
        break;
    /*  ...  */
    }
}

void DoHandleEvent()
{
    long evCode, param1, param2;
    bool bComplete = false;
    if (!pEvent) return;

    // Get all the events, and see we're done.
    while (SUCCEEDED(pEvent->GetEvent(&evCode, &param1, &param2, 0))
    {
        pEvent->FreeEventParams(evCode, param1, param2);
        switch(evCode)
        {
            case EC_USERABORT:
            case EC_ERRORABORT:
            case EC_COMPLETE:
                bComplete = true;
                break;
        }
    }
    if (bComplete)
    {
        pControl->Stop(); // Important! You must stop the graph!

        // Turn off event notification.
        pEvent->SetNotifyWindow(NULL, 0, 0);
        pEvent->Release();
        pEvent = NULL;
        // Reset the progress bar to zero and get rid of the timer.
        SendDlgItemMessage(IDC_PROGRESS1, PBM_SETPOS, 0, 0);
        KillTimer(hwnd, nIDEvent);
    }
}
```



 

 



