---
title: Enumerando dispositivos windows Gerenciador de Dispositivos mídia
description: Saiba mais sobre como enumerar os dispositivos detectados pelo Windows Media Gerenciador de Dispositivos usando uma interface de enumeração.
ms.assetid: c5935681-b530-4446-a026-7ddc74084d23
keywords:
- Windows Media Gerenciador de Dispositivos, enumerando dispositivos
- Gerenciador de Dispositivos, enumerando dispositivos
- guia de programação, enumerando dispositivos
- aplicativos da área de trabalho, enumerando dispositivos
- criando aplicativos do Windows Media Gerenciador de Dispositivos, enumerando dispositivos
- enumerando dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94653d59b0880e9d52f43b34e21522a220d39beb
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068193"
---
# <a name="enumerating-windows-media-device-manager-devices"></a>Enumerando dispositivos windows Gerenciador de Dispositivos mídia

Depois de autenticar um aplicativo, você pode começar a enumerar os dispositivos detectados pelo Windows Media Gerenciador de Dispositivos. A enumeração é feita usando uma interface de [**enumeração, IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice), obtida usando [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) ou [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices). Se tiver suporte, use o método **EnumDevices2,** pois a versão anterior retornou apenas interfaces herdadas em dispositivos, enquanto a nova versão retorna as interfaces herdadas e novas.

Antes de obter um enumerador, você deve decidir qual exibição de enumeração usar. Alguns dispositivos expõem cada armazenamento como um dispositivo diferente. Por exemplo, dois cartões de memória flash em um dispositivo serão enumerados como se fossem dispositivos separados. Você pode especificar que todos os armazenamentos em um dispositivo sejam enumerados juntos como um único dispositivo. Você pode definir essa preferência apenas uma vez em seu aplicativo; Se você quiser alterá-lo, deverá desligar o aplicativo e reiniciá-lo. No entanto, observe que, às vezes, os dispositivos herdados ignorarão uma solicitação para enumerar armazenamentos de dispositivos separados como um único dispositivo e continuarão a enumerá-los separadamente.

As etapas a seguir mostram como enumerar dispositivos conectados:

1.  De definir a preferência de enumeração do dispositivo [**usando IWMDeviceManager3::SetDeviceEnumPreference**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager3-setdeviceenumpreference). Se esse método não for chamado, o método padrão será mostrar armazenamentos como dispositivos separados. Para determinar se "dispositivos" individuais são realmente armazenamentos no mesmo dispositivo, chame [**IWMDMDevice2::GetCanonicalName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getcanonicalname); os armazenamentos do mesmo dispositivo retornarão valores idênticos, exceto pelo dígito final após o último sinal de "$".
2.  Consulte [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) ou [**IWMDeviceManager2**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager2)e, em seguida, chame [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) para obter a interface do enumerador de dispositivo, [**IWMDMEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumdevice). (Se tiver suporte, use **EnumDevices2,** que é mais eficiente, pois a versão anterior pode não retornar dispositivos MTP).
3.  Chame o [**método IWMDMEnumDevices::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumdevice-next) para recuperar um ou mais dispositivos por vez. Continue a chamar esse método até que o método retorne S \_ FALSE ou uma mensagem de erro. Se recuperar apenas um dispositivo por vez, você não precisará alocar uma matriz para manter os dispositivos.

Como os usuários podem anexar ou remover dispositivos do computador enquanto o aplicativo está em execução, é uma boa ideia implementar a notificação de conexão ou remoção do dispositivo. Isso é feito implementando a interface [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification) e registrando-a. Para obter mais informações sobre isso, consulte [Habilitando notificações](enabling-notifications.md).

O código C++ a seguir enumera dispositivos e solicita informações sobre cada dispositivo.


```C++
HRESULT CWMDMController::EnumDevices()
{
    HRESULT hr = S_OK;

    // Change behavior to show devices as one object, not each storage as a device.
    // This can be called only once for each instance of this application.
    CComQIPtr<IWMDeviceManager3>pDevMgr3(m_IWMDMDeviceMgr);
    hr = pDevMgr3->SetDeviceEnumPreference(DO_NOT_VIRTUALIZE_STORAGES_AS_DEVICES);
    
    // Get number of attached devices.
    DWORD iDevices = 0;
    hr = m_IWMDMDeviceMgr->GetDeviceCount(&iDevices);
    if (hr == S_OK)
    {
        // TODO: Display count of devices.
    }

    //
    // Get a device enumerator to enumerate devices.
    //
    CComPtr<IWMDeviceManager2> pDevMgr2;
    hr = m_IWMDMDeviceMgr->QueryInterface (__uuidof(IWMDeviceManager2), (void**) &pDevMgr2);
    if (hr == S_OK)
    {
        // TODO: Display message indicating that application obtained IWMDeviceManager2.
    }
    else
    {
        // TODO: Display message indicating that we couldn't 
        // get IWMDeviceManager2 in EnumDevices.
        return hr;
    }
   CComPtr<IWMDMEnumDevice> pEnumDevice;
   hr = pDevMgr2->EnumDevices2(&pEnumDevice);
    if (hr != S_OK)
    {
        // TODO: Display messaging indicating that an error occurred 
        // in calling EnumDevices2.
        return hr;
    }

    // Length of all the strings we'll send in. 
    const UINT MAX_CHARS = 100;

    // Iterate through devices.
    while(TRUE)
    {
        // Get a device handle.
        IWMDMDevice *pIWMDMDevice;
        ULONG ulFetched = 0;
        hr = pEnumDevice->Next(1, &pIWMDMDevice, &ulFetched);
        if ((hr != S_OK) || (ulFetched != 1))
        {
            break;
        }
        
        // Get a display icon for the device.
        ULONG deviceIcon = 0;
        hr = pIWMDMDevice->GetDeviceIcon(&deviceIcon);

        // Print the device manufacturer.
        WCHAR manufacturer[MAX_CHARS];
        hr = pIWMDMDevice->GetManufacturer((LPWSTR)&manufacturer, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display manufacturer name.
        }

        // Get the device name.
        WCHAR name[MAX_CHARS];
        hr = pIWMDMDevice->GetName((LPWSTR)&name, MAX_CHARS);
        if (hr == S_OK)
        {
            // TODO: Display name.
        }

        // TODO: Get other device information if wanted.

        // Obtain an IWMDMDevice2 interface and call some methods.
        CComQIPtr<IWMDMDevice2> pIWMDMDevice2(pIWMDMDevice);
        if (pIWMDMDevice2 != NULL)
        {
            // Get the canonical name.
            WCHAR canonicalName[MAX_CHARS];
            hr = pIWMDMDevice2->GetCanonicalName(canonicalName, MAX_CHARS);
            if (hr == S_OK)
            {
                // TODO: Display canonical name.
            }
        }

        // Obtain an IWMDMDevice3 interface and call some methods.
        CComQIPtr<IWMDMDevice3>pIWMDMDevice3(pIWMDMDevice);
        if (pIWMDMDevice3 != NULL)
        {
            // Find out what protocol is being used.
            PROPVARIANT val;
            PropVariantInit(&val);
            hr = pIWMDMDevice3->GetProperty(g_wszWMDMDeviceProtocol, &val);

            if (hr == S_OK)
            {
                if (*val.puuid == WMDM_DEVICE_PROTOCOL_RAPI)
                {
                    // TODO: Display message indicating device is a RAPI device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MTP)
                {
                    / /TODO: Display message indicating device is an MTP device.
                }
                else if (*val.puuid == WMDM_DEVICE_PROTOCOL_MSC)
                {
                    // TODO: Display message indicating device is an MSC device.
                }
                else
                {
                    // TODO: Display message indicating that the 
                    // application encountered an unknown protocol.
                }
                PropVariantClear(&val);
            }
        }

        // Examine the device capabilities. You could use some of these
        // to enable or disable the application's UI elements.
        CComQIPtr<IWMDMDeviceControl> pDeviceControl(pIWMDMDevice);
        if (pDeviceControl != NULL)
        {
            DWORD caps = 0;
            hr = pDeviceControl->GetCapabilities(&caps);
            if (caps & WMDM_DEVICECAP_CANPLAY)
            {
                // TODO: Display message indicating that the media 
                // device can play MP3 audio.
            }
            // TODO: Test for other capabilities here.
        }
    } // Get the next device.
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando um aplicativo de Gerenciador de Dispositivos Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




