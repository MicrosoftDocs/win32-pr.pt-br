---
title: Implementar o objeto de acesso ao dispositivo
description: Este tópico explica como insinuar o objeto de acesso ao dispositivo e usá-lo para acessar um dispositivo.
ms.assetid: 26619A25-67FE-44DC-82DD-36076326748D
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: c90252e2a906928706fa8577e133a019482976b4d5dd8e4a7cb1ebd4fb245ec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029087"
---
# <a name="implement-the-device-access-object"></a>Implementar o objeto de acesso ao dispositivo

Este tópico explica como insinuar o objeto de acesso ao dispositivo e usá-lo para acessar um dispositivo. A classe instandada implementa as interfaces [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) e [**ICreateDeviceAccessAsync.**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1

Para insinuar o objeto de acesso ao dispositivo, primeiro você deve chamar a função [**CreateDeviceAccessInstance.**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) Se **CreateDeviceAccessInstance** for bem-sucedido, você poderá chamar o método [**Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) para aguardar a operação assíncrona ser finalada. Se **Wait** for bem-sucedido, você poderá recuperar um [**objeto IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) (ou o erro apropriado) do [**método GetResult.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult)

```C++
HRESULT
CMyServer::Initialize(
        PCWSTR   pszDeviceInterfacePath
    )

/*++
Routine Description:

    This routine is called to initialize the Device Access object.
    It's not part of the constructor as the initialization can fail.
    It opens the device and gets the IDeviceIoControl interface to the device instance
    via the broker.

Arguments:
    pszDeviceInterfacePath - the device interface string that needs to be opened

Return Value:

    HRESULT

--*/

{
    HRESULT hr;
    ICreateDeviceAccessAsync *pDeviceAccess;

     //
     // Here's the actual open call.  This will *fail* if your lowbox does
     // not have the capability mapped to the interface class specified.
     // If you are running this as normal user, it will just pass through to
     // create file.
     //

   hr = CreateDeviceAccessInstance(pszDeviceInterfacePath,
                                   GENERIC_READ|GENERIC_WRITE,
                                   &pDeviceAccess);

    if (FAILED(hr)) {
        return hr;
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->Wait(INFINITE);
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->GetResult(IID_IDeviceIoControl,
                                            (void **)&m_pDeviceIoControl);
    }

    pDeviceAccess->Release();

    return hr;
}
```



### <a name="step-2"></a>Etapa 2

Este é um exemplo de uma chamada para o **método DeviceIoControlSync.**


```C++
IFACEMETHODIMP 
CMyServer::put_SevenSegmentDisplay(
    BYTE   value
    )
/*++

Routine Description:
    This routine puts the display value into the device.

Arguments:
    
    value - The value to be written to the device.
    
Return Value:

    HRESULT

--*/
{
    BYTE sevenSegment = 0;
    HRESULT hr;

    if (value >= ARRAYSIZE(g_NumberToMask)) {
        return E_INVALIDARG;
    }


    sevenSegment = g_NumberToMask[value];
    hr = m_pDeviceIoControl->DeviceIoControlSync(
                         IOCTL_OSRUSBFX2_SET_7_SEGMENT_DISPLAY,
                         &sevenSegment,
                         sizeof(BYTE),
                         NULL,
                         0,
                         NULL
                         );

    return hr;
}
```



## <a name="remarks"></a>Comentários

Você também pode enviar um IOCTL de forma assíncrona usando o [**método DeviceIoControlAsync.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) Nesse caso, você deve implementar a interface [**IDeviceRequestCompletionCallback.**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)aplicativos de dispositivo [UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de Desenvolvimento de Hardware](/windows-hardware/drivers/)
