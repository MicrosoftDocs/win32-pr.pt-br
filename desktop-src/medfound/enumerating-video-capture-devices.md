---
description: Este tópico descreve como enumerar os dispositivos de captura de vídeo no sistema de usuários e como criar uma instância de um dispositivo.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Enumerando dispositivos de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476c4b41e6f8913414200c7a811ba9625f2c4bc9cfea66875ec5f15b788bdc05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061616"
---
# <a name="enumerating-video-capture-devices"></a>Enumerando dispositivos de captura de vídeo

Este tópico descreve como enumerar os dispositivos de captura de vídeo no sistema do usuário e como criar uma instância de um dispositivo.

Para enumerar os dispositivos de captura de vídeo no sistema, faça o seguinte:

1.  Chame [**MFCreateAttributes para**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) criar um armazenamento de atributos. Essa função recebe um [**ponteiro IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Chame [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) para definir o atributo [MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE \_ \_ TYPE.](mf-devsource-attribute-source-type.md) De definir o valor do atributo como **MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ GUID**.
3.  Chame [**MFEnumDeviceSources.**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) Essa função recebe uma matriz de [**ponteiros IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e o tamanho da matriz. Cada ponteiro representa um dispositivo de captura de vídeo distinto.

Para criar uma instância de um dispositivo de captura:

-   Chame [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para obter um ponteiro para a interface [**IMFMediaSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

O código a seguir mostra essas etapas:


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



Depois de criar a fonte de mídia, libere os ponteiros de interface e libere a memória para a matriz:


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



