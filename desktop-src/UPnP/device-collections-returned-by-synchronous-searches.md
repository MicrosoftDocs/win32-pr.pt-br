---
title: Coleções de dispositivos retornadas por pesquisas síncronas
description: Coleções de dispositivos são objetos que contêm um ou mais objetos device. Uma coleção de dispositivos expõe a interface IUPnPDevices que fornece métodos e propriedades para percorrer a coleção e extrair objetos de dispositivo individuais.
ms.assetid: 45455c3f-7281-4f96-a609-2efd2cf36aa2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94901dd2f3988327c32d7c21799ff4db7647e76fd987247e903501bd8937851a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755522"
---
# <a name="device-collections-returned-by-synchronous-searches"></a>Coleções de dispositivos retornadas por pesquisas síncronas

Coleções de dispositivos são objetos que contêm um ou mais objetos device. Uma coleção de dispositivos expõe a interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) que fornece métodos e propriedades para percorrer a coleção e extrair objetos de dispositivo individuais.

## <a name="vbscript-example"></a>Exemplo de VBScript

Os aplicativos VBScript podem acessar os objetos na coleção de duas maneiras. Primeiro, eles podem percorrer os elementos sequencialmente usando um para ... Cada... próximo loop, conforme mostrado no exemplo a seguir:


```VB
for each deviceObj in devices
    MsgBox(deviceObj.FriendlyName)
next
```



Neste exemplo, supõe-se que a variável de dispositivos tenha sido inicializada com o resultado de uma pesquisa anterior. O loop passa pelos objetos Device na coleção, atribuindo à variável deviceObj o valor de cada objeto Device por vez. O corpo do loop pode conter código que processa o objeto Device.

## <a name="c-example"></a>Exemplo de C++

O exemplo a seguir mostra o código C++ necessário para acessar os objetos em uma coleção de objetos de dispositivo. A função mostrada, **TraverseCollection**, recebe um ponteiro para a interface [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) como um parâmetro de entrada. Esse ponteiro de interface pode ser retornado pelo [**método FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) ou outros **métodos Find** do objeto Device Finder.


```C++
#include <windows.h>
#include <upnp.h>

#pragma comment(lib, "oleaut32.lib")

HRESULT TraverseCollection(IUPnPDevices * pDevices)
{
    IUnknown * pUnk = NULL;
    HRESULT hr = pDevices->get__NewEnum(&pUnk);
    if (SUCCEEDED(hr))
    {
        IEnumVARIANT * pEnumVar = NULL;
        hr = pUnk->QueryInterface(IID_IEnumVARIANT, (void **) &pEnumVar);
        if (SUCCEEDED(hr))
        {
            VARIANT varCurDevice;
            VariantInit(&varCurDevice);
            pEnumVar->Reset();
            // Loop through each device in the collection
            while (S_OK == pEnumVar->Next(1, &varCurDevice, NULL))
            {
                IUPnPDevice * pDevice = NULL;
                IDispatch * pdispDevice = V_DISPATCH(&varCurDevice);
                if (SUCCEEDED(pdispDevice->QueryInterface(IID_IUPnPDevice, (void **) &pDevice)))
                {
                    // Do something interesting with pDevice
                    BSTR bstrName = NULL;
                    if (SUCCEEDED(pDevice->get_FriendlyName(&bstrName)))
                    {
                        OutputDebugStringW(bstrName);
                        SysFreeString(bstrName);
                    }
                }
                VariantClear(&varCurDevice);
                pDevice->Release();
            }
            pEnumVar->Release();
        }
        pUnk->Release();
    }
    return hr;
}
```



A primeira etapa é solicitar um novo enumerador para a coleção usando a [**\_ propriedade NewEnum.**](/windows/win32/api/upnp/nf-upnp-iupnpdevices-get__newenum) Isso retorna um enumerador como a interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) O código de exemplo invoca [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter a interface [**IEnumVARIANT.**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) O código de exemplo define o enumerador como o início da coleção invocando o [**método IEnumVARIANT::Reset.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) Por fim, o código de exemplo invoca [**o método IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para percorrer a coleção. Os objetos de dispositivo na coleção estão contidos em **estruturas VARIANT.** Essas estruturas contêm ponteiros para interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) nos objetos do dispositivo. Para obter a interface [**IUPnPDevice,**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice) o código de exemplo invoca **QueryInterface** na interface **IDispatch.**

 

 