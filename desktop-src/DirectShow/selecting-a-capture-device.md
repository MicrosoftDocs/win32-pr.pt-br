---
description: Selecionando um dispositivo de captura
ms.assetid: 8f92873d-569a-48af-a913-6d4cce65640f
title: Selecionando um dispositivo de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b599728c6bd2d98b89285b6008923aa4fb2a3aef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105758048"
---
# <a name="selecting-a-capture-device"></a>Selecionando um dispositivo de captura

Para selecionar um dispositivo de captura de áudio ou vídeo, use o [enumerador de dispositivo do sistema](system-device-enumerator.md), descrito no tópico [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md). O enumerador de dispositivo do sistema retorna uma coleção de monikers de dispositivo, selecionada por categoria de dispositivo. Um *moniker* é um objeto com que contém informações sobre outro objeto. Os monikers permitem que o aplicativo Obtenha informações sobre um objeto sem realmente criar o objeto. Posteriormente, o aplicativo pode usar o moniker para criar o objeto. Para obter mais informações sobre monikers, consulte a documentação de [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker).

Para usar o enumerador de dispositivo do sistema, execute as etapas a seguir.

1.  Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância do enumerador de dispositivo do sistema.
2.  Chame [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) e especifique a categoria de dispositivo como um GUID. Para dispositivos de captura, as categorias a seguir são relevantes. 

    | GUID da categoria                       | Descrição           |
    |-------------------------------------|-----------------------|
    | **\_AUDIOINPUTDEVICECATEGORY CLSID** | Dispositivos de captura de áudio |
    | **\_VIDEOINPUTDEVICECATEGORY CLSID** | Dispositivos de captura de vídeo |

    

     

    Se uma câmera de vídeo tiver um microfone integrado, ela aparecerá em ambas as categorias. No entanto, a câmera e o microfone são tratados como dispositivos separados pelo sistema, para fins de enumeração, criação de dispositivos e streaming de dados.

3.  O método [**CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) retorna um ponteiro para a interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) . Para enumerar os monikers, chame [**IEnumMoniker:: Next**](/windows/win32/api/objidl/nf-objidl-ienummoniker-next).

O código a seguir cria um enumerador para uma categoria de dispositivo especificada.


```C++
#include <windows.h>
#include <dshow.h>

#pragma comment(lib, "strmiids")

HRESULT EnumerateDevices(REFGUID category, IEnumMoniker **ppEnum)
{
    // Create the System Device Enumerator.
    ICreateDevEnum *pDevEnum;
    HRESULT hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL,  
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDevEnum));

    if (SUCCEEDED(hr))
    {
        // Create an enumerator for the category.
        hr = pDevEnum->CreateClassEnumerator(category, ppEnum, 0);
        if (hr == S_FALSE)
        {
            hr = VFW_E_NOT_FOUND;  // The category is empty. Treat as an error.
        }
        pDevEnum->Release();
    }
    return hr;
}
```



A interface [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) enumera uma lista de interfaces [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) , cada uma representando um moniker de dispositivo. O aplicativo pode ler as propriedades do moniker ou usar o moniker para criar um filtro de captura do DirectShow para o dispositivo. As propriedades de moniker são retornadas como valores de **variante** . As propriedades a seguir têm suporte dos monikers de dispositivo.



| Propriedade       | Descrição                                                               | Tipo de VARIANTE |
|----------------|---------------------------------------------------------------------------|--------------|
| FriendlyName | O nome do dispositivo.                                                   | **VT \_ BSTR** |
| Ndescrição  | Uma descrição do dispositivo.                                              | **VT \_ BSTR** |
| DevicePath   | Uma cadeia de caracteres exclusiva que identifica o dispositivo. (Somente dispositivos de captura de vídeo.) | **VT \_ BSTR** |
| "WaveInID"     | O identificador de um dispositivo de captura de áudio. (Somente dispositivos de captura de áudio.) | **\_I4 VT**   |



 

As propriedades "FriendlyName" e "Description" são adequadas para exibição em uma interface do usuário.

-   A propriedade "FriendlyName" está disponível para cada dispositivo. Ele contém um nome legível para o dispositivo.
-   A propriedade "Description" está disponível apenas para dispositivos DV e D-VHS/MPEG. Para obter mais informações, consulte [Driver MSDV](msdv-driver.md) e [Driver MSTape](mstape-driver.md). Se disponível, ele contém uma descrição do dispositivo que é mais específico do que a propriedade "FriendlyName". Normalmente, ele inclui o nome do fornecedor.
-   A propriedade "DevicePath" não é uma cadeia de caracteres legível, mas é garantido que seja exclusivo para cada dispositivo de captura de vídeo no sistema. Você pode usar essa propriedade para distinguir entre duas ou mais instâncias do mesmo modelo de dispositivo.
-   Se a propriedade "WaveInID" estiver presente, isso significa que o filtro de captura do DirectShow usa as APIs de áudio da forma de [onda](../multimedia/waveform-audio.md) internamente para se comunicar com o dispositivo. O valor da propriedade "WaveInID" corresponde ao identificador usado pelas funções **Wave \** _, como [_ *waveInOpen* *](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen).

Para ler as propriedades do moniker, execute as etapas a seguir.

1.  Chame [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) para obter um ponteiro para a interface [**IPropertyBag**](../com/ipropertybag-and-ipersistpropertybag.md) .
2.  Chame **IPropertyBag:: Read** para ler a propriedade.

O exemplo de código a seguir mostra como enumerar uma lista de monikers de dispositivo e obter as propriedades.


```C++
void DisplayDeviceInformation(IEnumMoniker *pEnum)
{
    IMoniker *pMoniker = NULL;

    while (pEnum->Next(1, &pMoniker, NULL) == S_OK)
    {
        IPropertyBag *pPropBag;
        HRESULT hr = pMoniker->BindToStorage(0, 0, IID_PPV_ARGS(&pPropBag));
        if (FAILED(hr))
        {
            pMoniker->Release();
            continue;  
        } 

        VARIANT var;
        VariantInit(&var);

        // Get description or friendly name.
        hr = pPropBag->Read(L"Description", &var, 0);
        if (FAILED(hr))
        {
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
        }
        if (SUCCEEDED(hr))
        {
            printf("%S\n", var.bstrVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Write(L"FriendlyName", &var);

        // WaveInID applies only to audio capture devices.
        hr = pPropBag->Read(L"WaveInID", &var, 0);
        if (SUCCEEDED(hr))
        {
            printf("WaveIn ID: %d\n", var.lVal);
            VariantClear(&var); 
        }

        hr = pPropBag->Read(L"DevicePath", &var, 0);
        if (SUCCEEDED(hr))
        {
            // The device path is not intended for display.
            printf("Device path: %S\n", var.bstrVal);
            VariantClear(&var); 
        }

        pPropBag->Release();
        pMoniker->Release();
    }
}

void main()
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        IEnumMoniker *pEnum;

        hr = EnumerateDevices(CLSID_VideoInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        hr = EnumerateDevices(CLSID_AudioInputDeviceCategory, &pEnum);
        if (SUCCEEDED(hr))
        {
            DisplayDeviceInformation(pEnum);
            pEnum->Release();
        }
        CoUninitialize();
    }
}
```



Para criar um filtro de captura do DirectShow para o dispositivo, chame o método [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para obter um ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Em seguida, chame [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) para adicionar o filtro ao grafo de filtro:


```C++
IBaseFilter *pCap = NULL;
hr = pMoniker->BindToObject(0, 0, IID_IBaseFilter, (void**)&pCap);
if (SUCCEEDED(hr))
{
    hr = m_pGraph->AddFilter(pCap, L"Capture Filter");
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de áudio](audio-capture.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 
