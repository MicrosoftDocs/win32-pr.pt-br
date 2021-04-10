---
description: Estabelecer uma conexão
ms.assetid: 16286da5-5979-413b-a4db-ca157b10a571
title: Estabelecer uma conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ea922b3cd44430dc7c213a513c44fa8ef2ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011818"
---
# <a name="establishing-a-connection"></a>Estabelecer uma conexão

Depois que o usuário seleciona um dispositivo, a função ChooseDevice, por sua vez, chama o método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) para estabelecer uma conexão entre o aplicativo e o dispositivo. O método IPortableDevice:: Open usa dois argumentos:

-   Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome Plug and Play do dispositivo. (Essa cadeia de caracteres é recuperada chamando o método [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) .)
-   Um ponteiro para uma [**interface IPortableDeviceValues**](iportabledevicevalues.md) que especifica as informações do cliente para o aplicativo.


```C++
// CoCreate the IPortableDevice interface and call Open() with
// the chosen PnPDeviceID string.
hr = CoCreateInstance(CLSID_PortableDeviceFTM,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(ppDevice));
if (SUCCEEDED(hr))
{
    hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
    if (FAILED(hr))
    {
        if (hr == E_ACCESSDENIED)
        {
            printf("Failed to Open the device for Read Write access, will open it for Read-only access instead\n");
            pClientInformation->SetUnsignedIntegerValue(WPD_CLIENT_DESIRED_ACCESS, GENERIC_READ);
            hr = (*ppDevice)->Open(pPnpDeviceIDs[uiCurrentDevice], pClientInformation);
            if (FAILED(hr))
            {
                printf("! Failed to Open the device, hr = 0x%lx\n",hr);
                // Release the IPortableDevice interface, because we cannot proceed
                // with an unopen device.
                (*ppDevice)->Release();
                *ppDevice = NULL;
            }
        }
        else
        {
            printf("! Failed to Open the device, hr = 0x%lx\n",hr);
            // Release the IPortableDevice interface, because we cannot proceed
            // with an unopen device.
            (*ppDevice)->Release();
            *ppDevice = NULL;
        }
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceFTM, hr = 0x%lx\n",hr);
}
```



Para o Windows 7, o [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice) dá suporte a dois CLSIDs para **CoCreateInstance**. **CLSID \_ do PortableDevice** retorna um ponteiro **IPortableDevice** que não agrega o marshaler de thread livre; **CLSID \_ do PortableDeviceFTM** é um novo CLSID que retorna um ponteiro **IPortableDevice** que agrega o marshaler de thread livre. Os dois ponteiros também dão suporte à mesma funcionalidade.

Aplicativos que residem em Apartments de thread único devem usar **CLSID \_ PortableDeviceFTM** , pois isso elimina a sobrecarga do marshaling do ponteiro de interface. **CLSID \_ do O PortableDevice** ainda tem suporte para aplicativos herdados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Selecionando um dispositivo**](selecting-a-device.md)
</dt> </dl>

 

 



