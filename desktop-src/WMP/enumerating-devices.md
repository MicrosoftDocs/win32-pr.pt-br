---
title: Enumerando dispositivos (SDK do WMP)
description: Este código de exemplo mostra uma função que enumera dispositivos criando uma matriz de ponteiros que representam um dispositivo.
ms.assetid: 0236a629-c09a-4687-a8ba-fa05107fab33
keywords:
- Windows Media Player, dispositivos portáteis
- Windows Media Player de objeto, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Windows Media Player controle ActiveX, dispositivos portáteis
- Controle ActiveX, dispositivos portáteis
- Windows Media Player controle ActiveX móvel, dispositivos portáteis
- Windows Media Player dispositivos móveis e portáteis
- dispositivos portáteis, enumerando
- enumerações, dispositivos portáteis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44f71fa26f40983424ced70280d9c03e0892a00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068433"
---
# <a name="enumerating-devices"></a>Enumerando dispositivos

Windows Media Player representa dispositivos portáteis usando a interface **IWMPSyncDevice.** O código de exemplo a seguir mostra uma função que cria uma matriz de ponteiros para **IWMPSyncDevice**. Cada ponteiro na matriz representa um dispositivo para o qual Windows Media Player tem informações armazenadas. Um dispositivo não precisa estar conectado ao computador, nem é necessário ter uma parceria com a instância Windows Media Player atual.

Você deve enumerar dispositivos sempre que receber o evento **DeviceConnect** ou **o evento DeviceDisconnect.**

A função a seguir enumera os dispositivos. O *parâmetro bConnectedOnly* especifica se apenas os dispositivos conectados ao computador do usuário são enumerados no momento.


```C++
STDMETHODIMP CMainDlg::EnumDevices(BOOL bConnectedOnly)
{
    HRESULT hr = S_OK;
    CComPtr<IWMPSyncServices>  spSyncServices;
    long cDeviceArray = 0;  // Size to make the array
    long cAllDevices = 0;  // Count of all devices
    long cDeviceIndex = 0; // Index for adding devices to array.
    CComPtr<IWMPSyncDevice> spTempDevice;
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;

    // Delete any existing array.
    FreeDeviceArray();

    // Retrieve a pointer to IWMPSyncServices.
    hr = m_spPlayer->QueryInterface(&spSyncServices);

    if(SUCCEEDED(hr) && spSyncServices.p)
    {  
        hr = spSyncServices->get_deviceCount(&cAllDevices);
    }

    if(SUCCEEDED(hr) && cAllDevices > 0)
    {
        if(bConnectedOnly)
        {
            // Count the number of connected devices.
            for(long i = 0; i < cAllDevices; i++)
            {     
                spTempDevice.Release();
                hr = spSyncServices->getDevice(i, &spTempDevice);

                if(SUCCEEDED(hr) && spTempDevice.p)
                {
                    spTempDevice->get_connected(&vbIsConnected);

                    if(vbIsConnected == VARIANT_TRUE)
                    {
                        // Count only the connected devices.
                        cDeviceArray++;
                    }
                }
            }
        }
        else
        {
            cDeviceArray = cAllDevices;
        }

        if(cDeviceArray == 0)
        {
            return hr;
        }

        // Cache the device count.
        m_cDevices = cDeviceArray;

        // Create a new device array.
        m_ppWMPDevices = new IWMPSyncDevice*[cDeviceArray];
        if(!m_ppWMPDevices)
        {
            return E_OUTOFMEMORY;
        }
        
        ZeroMemory(m_ppWMPDevices, sizeof (IWMPSyncDevice*) * cDeviceArray);

        // Fill the array.
        for(long i = 0; i < cAllDevices; i++)
        {
            spTempDevice.Release();
            hr = spSyncServices->getDevice(i, &spTempDevice);
            if(SUCCEEDED(hr) && spTempDevice.p)
            {
                spTempDevice->get_connected(&vbIsConnected);

                if( (bConnectedOnly && vbIsConnected == VARIANT_TRUE) ||
                     !bConnectedOnly )
                {
                    // Add the device to the custom array.
                    spTempDevice.CopyTo(&m_ppWMPDevices[cDeviceIndex++]);
                }
            }
        }
    }

    return hr;
}
```



Você pode usar código semelhante para recuperar outras listas de dispositivos desse tipo. Por exemplo, você pode usar [o \_ status IWMPSyncDevice::get](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) para criar uma matriz de dispositivos para os quais existe uma parceria.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPEvents2::D eviceConnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect)
</dt> <dt>

[**IWMPEvents2::D eviceDisconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect)
</dt> <dt>

[**IWMPSyncDevice Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice::get \_ connected**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected)
</dt> <dt>

[**IWMPSyncServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
</dt> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




