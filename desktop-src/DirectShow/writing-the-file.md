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
# <a name="writing-the-file"></a><span data-ttu-id="967a7-103">Gravando o arquivo</span><span class="sxs-lookup"><span data-stu-id="967a7-103">Writing the File</span></span>

<span data-ttu-id="967a7-104">Para gravar o arquivo, basta executar o gráfico de filtro chamando o método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) .</span><span class="sxs-lookup"><span data-stu-id="967a7-104">To write the file, simply run the filter graph by calling the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method.</span></span> <span data-ttu-id="967a7-105">Aguarde até que a reprodução seja concluída e pare explicitamente o grafo chamando [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); caso contrário, o arquivo não será gravado corretamente.</span><span class="sxs-lookup"><span data-stu-id="967a7-105">Wait for playback to complete and explicitly stop the graph by calling [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); otherwise the file is not written correctly.</span></span>

<span data-ttu-id="967a7-106">Para exibir o progresso da operação de gravação de arquivo, consulte o filtro Mux para a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="967a7-106">To display the progress of the file-writing operation, query the Mux filter for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="967a7-107">Chame o método [**IMediaSeeking:: getDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) para recuperar a duração do arquivo.</span><span class="sxs-lookup"><span data-stu-id="967a7-107">Call the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method to retrieve the duration of the file.</span></span> <span data-ttu-id="967a7-108">Periodicamente, enquanto o grafo está em execução, chame o método [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) para recuperar a posição atual do grafo no fluxo.</span><span class="sxs-lookup"><span data-stu-id="967a7-108">Periodically while the graph is running, call the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method to retrieve the graph's current position in the stream.</span></span> <span data-ttu-id="967a7-109">A posição atual dividida por duração fornece a porcentagem concluída.</span><span class="sxs-lookup"><span data-stu-id="967a7-109">Current position divided by duration gives the percentage complete.</span></span>

> [!Note]  
> <span data-ttu-id="967a7-110">Um aplicativo geralmente consulta o Gerenciador do grafo de filtro para **IMediaSeeking**, mas a gravação de arquivos é uma exceção a essa regra.</span><span class="sxs-lookup"><span data-stu-id="967a7-110">An application usually queries the Filter Graph Manager for **IMediaSeeking**, but file writing is an exception to this rule.</span></span> <span data-ttu-id="967a7-111">O Gerenciador de gráfico de filtro calcula a posição atual a partir da posição inicial e o tempo de execução do grafo, o que é preciso para a reprodução de arquivos, mas não para a gravação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="967a7-111">The Filter Graph Manager calculates the current position from the starting position and how long the graph has been running, which is accurate for file playback but not for file writing.</span></span> <span data-ttu-id="967a7-112">Portanto, para obter um resultado preciso, você deve recuperar a posição do filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="967a7-112">Therefore, to get an accurate result, you should retrieve the position from the MUX filter.</span></span>

 

<span data-ttu-id="967a7-113">O código a seguir obtém a duração do arquivo, inicia um temporizador para atualizar a interface do usuário do aplicativo e executa o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="967a7-113">The following code gets the duration of the file, starts a timer to update the application UI, and runs the filter graph.</span></span> <span data-ttu-id="967a7-114">(A verificação de erro é omitida para fins de clareza.)</span><span class="sxs-lookup"><span data-stu-id="967a7-114">(Error checking is omitted for clarity.)</span></span>


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



<span data-ttu-id="967a7-115">Quando o aplicativo recebe um evento de timer, ele pode atualizar a interface do usuário com a posição atual:</span><span class="sxs-lookup"><span data-stu-id="967a7-115">When the application receives a timer event, it can update the UI with the current position:</span></span>


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



<span data-ttu-id="967a7-116">Quando o aplicativo recebe um evento de conclusão do DirectShow, ele deve parar o grafo, conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="967a7-116">When the application receives a DirectShow completion event, it should stop the graph, as shown in the following code:</span></span>


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



 

 



