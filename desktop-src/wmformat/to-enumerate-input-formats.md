---
title: Para enumerar formatos de entrada
description: Para enumerar formatos de entrada
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- Formato de sistema avançado (ASF), enumerando formatos de entrada
- ASF (formato de sistemas avançados), enumerando formatos de entrada
- perfis, enumerando formatos de entrada
- codecs, enumerando formatos de entrada
- ASF (Advanced Systems Format), enumerações de formato de entrada
- ASF (formato de sistemas avançados), enumerações de formato de entrada
- perfis, enumerações de formato de entrada
- codecs, enumerações de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18360d3172af785fd1c00648ba0c9e869fb7fbc6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007243"
---
# <a name="to-enumerate-input-formats"></a>Para enumerar formatos de entrada

Cada um dos codecs de mídia do Windows aceita um ou mais tipos de mídia de entrada para compactação. O Windows Media Format SDK permite que você insira uma variedade maior de formatos do que aqueles com suporte nos codecs. O SDK faz isso executando transformações de pré-processamento nas entradas quando necessário, como redimensionar quadros de vídeo ou reamostrar áudio. Em qualquer caso, você deve garantir que os formatos de entrada para os arquivos gravados correspondam aos dados enviados para o gravador. Cada codec tem um formato de mídia de entrada padrão definido no gravador quando o perfil é carregado. Você pode examinar o formato de entrada padrão chamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).

Os codecs de vídeo dão suporte aos seguintes formatos: IYUV, I420, YV12, YUY2, UYVY, YVYU, YVU9, RGB 32, RGB 24, RGB 565, RGB 555 e RGB 8. Os codecs de áudio dão suporte a áudio PCM.

Para enumerar os formatos de entrada com suporte por um codec, execute as seguintes etapas:

1.  Crie um objeto do gravador e defina um perfil a ser usado. Para obter mais informações sobre como configurar perfis no gravador, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).
2.  Identifique o número de entrada para o qual você deseja verificar os formatos. Para obter mais informações sobre como identificar números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).
3.  Recupere o número total de formatos de entrada com suporte pela entrada desejada chamando [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).
4.  Execute o loop por todos os formatos de entrada com suporte, executando as etapas a seguir para cada um.
    -   Recupere a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para o formato de entrada chamando [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).
    -   Recupere a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o formato de entrada. Chame [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype), passando **NULL** para o parâmetro *pType* para obter o tamanho da estrutura. Em seguida, aloque memória para manter a estrutura e chamar **GetMediaType** novamente para obter a estrutura. [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) herda de [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops), para que você possa fazer as chamadas para **GetMediaType** da instância do **IWMInputMediaProps** recuperada na etapa anterior.
    -   O formato descrito na estrutura [**do \_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contém todas as informações pertinentes sobre o formato de entrada. O formato básico da mídia é identificado pela **mídia do \_ WM \_ tipo. subtipo**. Para fluxos de vídeo, o membro **pbFormat** aponta para uma estrutura de [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) alocada dinamicamente que contém mais detalhes sobre o fluxo, incluindo o tamanho do retângulo. O tamanho dos quadros de entrada não é necessário para corresponder exatamente a um tamanho suportado pelo codec. Se eles não corresponderem, os componentes de tempo de execução do SDK, em muitos casos, redimensionarão automaticamente os quadros de vídeo de entrada para algo que o codec possa aceitar.

O código de exemplo a seguir localiza o formato de entrada do subtipo passado como um parâmetro. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


```C++
HRESULT FindInputFormat(IWMWriter* pWriter, 
                       DWORD dwInput,
                       GUID guidSubType,
                       IWMInputMediaProps** ppProps)
{
    DWORD   cFormats = 0;
    DWORD   cbSize   = 0;

    WM_MEDIA_TYPE*      pType  = NULL;
    IWMInputMediaProps* pProps = NULL;

    // Set the ppProps parameter to point to NULL. This will
    //  be used to check the results of the function later.
    *ppProps = NULL;

    // Find the number of formats supported by this input.
    HRESULT hr = pWriter->GetInputFormatCount(dwInput, &cFormats);
    if (FAILED(hr))
    {
        goto Exit;
    }
    // Loop through all of the supported formats.
    for (DWORD formatIndex = 0; formatIndex < cFormats; formatIndex++)
    {
        // Get the input media properties for the input format.
        hr = pWriter->GetInputFormat(dwInput, formatIndex, &pProps);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Get the size of the media type structure.
        hr = pProps->GetMediaType(NULL, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }
        // Allocate memory for the media type structure.
        pType = (WM_MEDIA_TYPE*) new (std::nothrow) BYTE[cbSize];
        if (pType == NULL)
        {
            hr = E_OUTOFMEMORY;
            goto Exit;
        }
        
        // Get the media type structure.
        hr = pProps->GetMediaType(pType, &cbSize);
        if (FAILED(hr))
        {
            goto Exit;
        }

        if(pType->subtype == guidSubType)
        {
            *ppProps = pProps;
            (*ppProps)->AddRef();
            goto Exit;
        }

        // Clean up for next iteration.
        delete [] pType;
        pType = NULL;
        SAFE_RELEASE(pProps);
    } // End for formatIndex.

    // If execution made it to this point, no matching format was found.
    hr = NS_E_INVALID_INPUT_FORMAT;

Exit:
    delete [] pType;
    SAFE_RELEASE(pProps);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




