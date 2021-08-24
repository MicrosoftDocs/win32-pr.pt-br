---
title: Mostrando o progresso da sincronização
description: Mostrando o progresso da sincronização
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Windows Media Player, dispositivos portáteis
- Windows Media Player modelo de objeto, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Windows Media Player ActiveX controle, dispositivos portáteis
- ActiveX controle, dispositivos portáteis
- Windows Media Player Controle ActiveX dispositivos móveis, dispositivos portáteis
- Windows Media Player Dispositivos móveis e portáteis
- dispositivos portáteis, progresso da sincronização
- sincronização de dispositivo, mostrando o progresso
- sincronizando dispositivos, mostrando o progresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126bff5f96aa9b18c1729d0da12b05a73da6eb43dd63d8135baf0544e19ada5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833287"
---
# <a name="showing-synchronization-progress"></a>Mostrando o progresso da sincronização

Você pode exibir o progresso da sincronização para o usuário. O código de exemplo a seguir mostra como criar um temporizador para recuperar periodicamente o valor de progresso atual usando **IWMPSyncDevice::get \_ progress**. Observe que o valor de progresso recuperado representa o progresso de toda a operação de sincronização para cada dispositivo. Não há suporte para recuperar o progresso da sincronização para itens de mídia individuais.

Para determinar quando iniciar ou parar o temporizador, manipular o **evento DeviceSyncStateChange.** A função de exemplo a seguir demonstra esse manipulador de eventos. O código também exibe o estado de sincronização atual como uma cadeia de caracteres de texto usando um controle de texto estático, chamado IDC \_ SYNCSTATE.


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



Quando o temporizador está em execução, ele envia uma mensagem TIMER \_ WM em intervalos de um segundo. O aplicativo lida com o TIMER \_ WM em seu loop de mensagem.

A função de exemplo a seguir demonstra como mostrar o progresso usando um controle de texto estático (IDC PROGSTATIC) e usando um controle de \_ progresso (IDC \_ SYNCPROG). Chame essa função em resposta à mensagem TIMER WM e após a conclusão do processo de sincronização, conforme \_ mostrado no exemplo anterior.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Enumerando dispositivos**](enumerating-devices.md)
</dt> <dt>

[**IWMPSyncDevice Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice::get \_ progress**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[**IWMPSyncDevice::isIdentical**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




