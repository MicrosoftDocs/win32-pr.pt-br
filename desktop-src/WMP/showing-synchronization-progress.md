---
title: Mostrando o progresso da sincronização
description: Mostrando o progresso da sincronização
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Windows Media Player, dispositivos portáteis
- Modelo de objeto do Windows Media Player, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Controle ActiveX do Windows Media Player, dispositivos portáteis
- Controle ActiveX, dispositivos portáteis
- Controle ActiveX móvel do Windows Media Player, dispositivos portáteis
- Windows Media Player Mobile, dispositivos portáteis
- dispositivos portáteis, progresso da sincronização
- sincronização do dispositivo, mostrando o progresso
- Sincronizando dispositivos, mostrando o progresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f109f09d4efacef620a2c21691f50cc0ac2143
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823566"
---
# <a name="showing-synchronization-progress"></a><span data-ttu-id="32167-113">Mostrando o progresso da sincronização</span><span class="sxs-lookup"><span data-stu-id="32167-113">Showing Synchronization Progress</span></span>

<span data-ttu-id="32167-114">Você pode exibir o progresso da sincronização para o usuário.</span><span class="sxs-lookup"><span data-stu-id="32167-114">You can display synchronization progress to the user.</span></span> <span data-ttu-id="32167-115">O código de exemplo a seguir mostra como criar um temporizador para recuperar periodicamente o valor de progresso atual usando **IWMPSyncDevice:: get \_ Progress**.</span><span class="sxs-lookup"><span data-stu-id="32167-115">The following example code shows how to create a timer to periodically retrieve the current progress value by using **IWMPSyncDevice::get\_progress**.</span></span> <span data-ttu-id="32167-116">Observe que o valor de progresso recuperado representa o progresso da operação de sincronização inteira para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="32167-116">Note that the progress value retrieved represents the progress for the entire synchronization operation for each device.</span></span> <span data-ttu-id="32167-117">Não há suporte para a recuperação do andamento da sincronização para itens de mídia individuais.</span><span class="sxs-lookup"><span data-stu-id="32167-117">Retrieving synchronization progress for individual media items is not supported.</span></span>

<span data-ttu-id="32167-118">Para determinar quando iniciar ou parar o temporizador, manipule o evento **DeviceSyncStateChange** .</span><span class="sxs-lookup"><span data-stu-id="32167-118">To determine when to start or stop the timer, handle the **DeviceSyncStateChange** event.</span></span> <span data-ttu-id="32167-119">A função de exemplo a seguir demonstra tal manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="32167-119">The following example function demonstrates such an event handler.</span></span> <span data-ttu-id="32167-120">O código também exibe o estado de sincronização atual como uma cadeia de texto usando um controle de texto estático, chamado IDC \_ SyncState.</span><span class="sxs-lookup"><span data-stu-id="32167-120">The code also displays the current synchronization state as a text string using a static text control, named IDC\_SYNCSTATE.</span></span>


```C++
void CMainDlg::DeviceSyncStateChange( IWMPSyncDevice * pDevice, WMPSyncState NewState )
{
    if(NULL == pDevice)
    {
        return;
    }

    HRESULT hr = E_POINTER;
    VARIANT_BOOL  vbIdentical = VARIANT_FALSE;
    // Window handle for static text control that shows the sync state.
    HWND hwndSyncStateText = GetDlgItem(IDC_SYNCSTATE); 

    // Strings to show sync state.
    const TCHAR *szSyncState[3] = {
    _T("Unknown"),
    _T("Synchronizing"),
    _T("Stopped")};

    // Get a pointer to the device the user selected in the list box.    
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]); 
    // Cache the pointer to the device that raised the event.
    CComPtr<IWMPSyncDevice> spDeviceParam(pDevice); 

    if(spDevice.p)
    {
        // Test whether the device that raised the event is the same as 
        // the one the user selected.
        hr = spDevice->isIdentical(spDeviceParam, &vbIdentical);
    }

    if(SUCCEEDED(hr) &&
        vbIdentical == VARIANT_TRUE)
    {    
        // Display the sync state.
        SendMessage(hwndSyncStateText, WM_SETTEXT, 0, (LPARAM)szSyncState[NewState]);

        switch(NewState)
        {
        case wmpssSynchronizing:
            // Start the progress timer.
            SetTimer(1, 1000, NULL);
            SetUIState(Synchronizing, TRUE);
            break;
        case wmpssStopped:
            // Stop the progress timer.
            KillTimer(1);
            // Make sure the final progress is displayed.            
            ShowProgress(GetSelectedDeviceIndex());
            SetUIState(Partnership, TRUE);
            break;      
        default:
            break;
        }
    }    
}
```



<span data-ttu-id="32167-121">Quando o temporizador está em execução, ele envia uma \_ mensagem de temporizador do WM em intervalos de um segundo.</span><span class="sxs-lookup"><span data-stu-id="32167-121">When the timer is running, it sends a WM\_TIMER message at one-second intervals.</span></span> <span data-ttu-id="32167-122">O aplicativo lida com o \_ temporizador do WM em seu loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="32167-122">The application handles WM\_TIMER in its message loop.</span></span>

<span data-ttu-id="32167-123">A função de exemplo a seguir demonstra como mostrar o progresso usando um controle de texto estático (IDC \_ PROGSTATIC) e usando um controle Progress (IDC \_ SYNCPROG).</span><span class="sxs-lookup"><span data-stu-id="32167-123">The following example function demonstrates how to show progress by using both a static text control (IDC\_PROGSTATIC), and using a progress control (IDC\_SYNCPROG).</span></span> <span data-ttu-id="32167-124">Chame essa função em resposta à mensagem de \_ temporizador do WM e após a conclusão do processo de sincronização, conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="32167-124">Call this function in response to the WM\_TIMER message and upon completion of the synchronization process, as shown in the preceding example.</span></span>


```C++
STDMETHODIMP CMainDlg::ShowProgress(long lIndex)
{  
    ATLASSERT(m_ppWMPDevices);

    long lProgress = 0;
    WCHAR buffer[10]; // Buffer larger than needed to hold progress string.
    ZeroMemory(buffer, sizeof WCHAR * 10);

    // Retrieve a handle to the progress control
    HWND  hwndSyncProgressCtl = GetDlgItem(IDC_SYNCPROG); 
    // Retrieve a handle to the static control that displays 
    // progress as text.
    HWND  hwndSyncProgressText = GetDlgItem(IDC_PROGSTATIC); 

    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[lIndex]);
    
    HRESULT hr = spDevice->get_progress(&lProgress);

    // Convert progress to a string and add the percent character.
    _ltow(lProgress, buffer, 10);
    CComBSTR bstrProgress(buffer);
    bstrProgress += " %";

    // Display the text.
    ::SendMessage(hwndSyncProgressText, WM_SETTEXT, 0, (LPARAM)(LPCTSTR)COLE2T(bstrProgress));
    // Set the progress control position.
    ::SendMessage(hwndSyncProgressCtl, PBM_SETPOS, (WPARAM)(int)lProgress, 0);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="32167-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32167-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32167-126">**Enumerando dispositivos**</span><span class="sxs-lookup"><span data-stu-id="32167-126">**Enumerating Devices**</span></span>](enumerating-devices.md)
</dt> <dt>

[<span data-ttu-id="32167-127">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="32167-127">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="32167-128">**IWMPSyncDevice:: obter \_ progresso**</span><span class="sxs-lookup"><span data-stu-id="32167-128">**IWMPSyncDevice::get\_progress**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[<span data-ttu-id="32167-129">**IWMPSyncDevice:: isidêntico**</span><span class="sxs-lookup"><span data-stu-id="32167-129">**IWMPSyncDevice::isIdentical**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[<span data-ttu-id="32167-130">**Trabalhando com dispositivos portáteis**</span><span class="sxs-lookup"><span data-stu-id="32167-130">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




