---
description: Um dispositivo de captura de vídeo pode dar suporte a um intervalo de taxas de quadros.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Como definir a taxa de quadros de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760603"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Como definir a taxa de quadros de captura de vídeo

Um dispositivo de captura de vídeo pode dar suporte a um intervalo de taxas de quadros. Se essas informações estiverem disponíveis, as taxas de quadros mínima e máxima serão armazenadas como atributos de tipo de mídia:



| Atributo                                                         | Descrição         |
|-------------------------------------------------------------------|---------------------|
| [intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ máx.](mf-mt-frame-rate-range-max.md) | Taxa máxima de quadros. |
| [intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md) | Taxa mínima de quadros. |



 

O intervalo pode variar dependendo do formato de captura. Por exemplo, em tamanhos de quadros maiores, a taxa máxima de quadros pode ser reduzida.

Para definir a taxa de quadros:

1.  Crie a origem de mídia para o dispositivo de captura. Consulte [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).
2.  Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem da mídia para obter o descritor de apresentação.
3.  Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obter o descritor de fluxo para o fluxo de vídeo.
4.  Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo.
5.  Enumere os formatos de captura, conforme descrito em [como definir o formato de captura de vídeo](how-to-set-the-video-capture-format.md).
6.  Selecione o formato de saída desejado na lista.
7.  Consulte o tipo de mídia para o intervalo de taxa de quadros do [MF \_ MT \_ \_ \_ \_ máximo](mf-mt-frame-rate-range-max.md) e o [intervalo de taxa de quadro do MF \_ MT \_ \_ \_ \_ ](mf-mt-frame-rate-range-min.md) . Esses valores fornecem o intervalo de taxas de quadros com suporte. O dispositivo pode dar suporte a outras taxas de quadros dentro desse intervalo.
8.  Defina o atributo de [**\_ \_ quadro MF MT**](mf-mt-frame-rate-attribute.md) no tipo de mídia para especificar a taxa de quadros desejada.
9.  Chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) com o tipo de mídia modificado.

O exemplo a seguir define a taxa de quadros igual à taxa máxima de quadros que o dispositivo dá suporte:


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



