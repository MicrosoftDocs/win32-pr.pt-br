---
description: Um dispositivo de captura de vídeo pode dar suporte A vários formatos de captura. Formatos normalmente diferem por tipo de compactação, espaço de cores (YUV ou RGB), tamanho do quadro ou taxa de quadros.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Como definir o formato de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764417"
---
# <a name="how-to-set-the-video-capture-format"></a>Como definir o formato de captura de vídeo

Um dispositivo de captura de vídeo pode dar suporte A vários formatos de captura. Formatos normalmente diferem por tipo de compactação, espaço de cores (YUV ou RGB), tamanho do quadro ou taxa de quadros.

A lista de formatos com suporte está contida no *descritor de apresentação*. Para obter mais informações, consulte [descritores de apresentação](presentation-descriptors.md).

Para enumerar os formatos com suporte:

1.  Crie a origem de mídia para o dispositivo de captura. Consulte [enumerando dispositivos de captura de vídeo](enumerating-video-capture-devices.md).
2.  Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) na origem da mídia para obter o descritor de apresentação.
3.  Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para obter o descritor de fluxo para o fluxo de vídeo.
4.  Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo.
5.  Chame [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) para obter o número de formatos com suporte.
6.  Em um loop, chame [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obter cada formato. O formato é representado por um *tipo de mídia*. Para obter mais informações, consulte [tipos de mídia de vídeo](video-media-types.md).

O exemplo a seguir enumera os formatos de captura para um dispositivo:


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



A `LogMediaType` função usada neste exemplo é listada no tópico [tipo de mídia depuração código](media-type-debugging-code.md).

Para definir o formato de captura:

1.  Obtenha um ponteiro para a interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) , conforme mostrado no exemplo anterior.
2.  Chame [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) para obter o formato desejado, especificado pelo índice.
3.  Chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para definir o formato.

Se você não definir o formato de captura, o dispositivo usará seu formato padrão.

O exemplo a seguir define o formato de captura:


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



A ordem na qual os formatos são retornados depende do dispositivo. Normalmente, eles são agrupados primeiro por tipo de compactação ou espaço de cores; e, em seguida, do menor tamanho de quadro para o maior tamanho de quadro dentro de cada grupo.

A taxa de quadros é tratada de forma ligeiramente diferente dos outros atributos de formato. Para obter mais informações, consulte [como definir a taxa de quadros de captura de vídeo](how-to-set-the-video-capture-frame-rate.md).

> [!Note]  
> Em alguns dispositivos, a lista de formatos conterá uma entrada duplicada para cada formato. Por exemplo, se o dispositivo der suporte a 15 formatos de captura distintos, a lista conterá 30 entradas. Dentro de cada par, um dos tipos de mídia terá o atributo [**MF \_ MT \_ am \_ Format \_ Type**](mf-mt-am-format-type-attribute.md) igual ao **Format \_ VIDEOINFO**, e o outro terá o **\_ tipo de \_ \_ formato \_ MF MT am** igual ao **formato \_ VideoInfo2**. (Esses dois valores são definidos no arquivo de cabeçalho UUIDs. h.) O segundo tipo também pode conter informações de cores adicionais ([informações de cores estendidas](extended-color-information.md)) ou mostrar um valor diferente para entrelaçamento ([**\_ \_ \_ modo de entrelaçamento MF MT**](mf-mt-interlace-mode-attribute.md)). Esses tipos duplicados existem para dar suporte a aplicativos mais antigos do DirectShow. Em um aplicativo Media Foundation, você deve ignorar o **formato \_ VIDEOINFO** tipo sempre que um tipo de **\_ VideoInfo2 de formato** duplicado estiver listado.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



