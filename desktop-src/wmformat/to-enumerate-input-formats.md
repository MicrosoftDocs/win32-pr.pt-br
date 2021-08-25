---
title: Para enumerar formatos de entrada
description: Para enumerar formatos de entrada
ms.assetid: 482adfc4-d9ed-403d-912b-1a5a70baf04c
keywords:
- ASF (Advanced Systems Format), enumerando formatos de entrada
- ASF (Formato de Sistemas Avançados), enumerando formatos de entrada
- perfis, enumerando formatos de entrada
- codecs, enumerando formatos de entrada
- FORMATO DE SISTEMAS Avançados (ASF), enumerações de formato de entrada
- ASF (Formato de Sistemas Avançados), enumerações de formato de entrada
- perfis, enumerações de formato de entrada
- codecs, enumerações de formato de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09e1583c9331e9cfab26e7ac64064224111ea58858d32b876ece843b83df0d2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929246"
---
# <a name="to-enumerate-input-formats"></a>Para enumerar formatos de entrada

Cada um dos codecs Windows Media aceita um ou mais tipos de mídia de entrada para compactação. O Windows SDK de Formato de Mídia permite que você instale uma variedade maior de formatos do que os com suporte dos codecs. O SDK faz isso executando transformações de pré-processamento nas entradas quando necessário, como reizing video frames ou resampling audio. Em qualquer caso, você deve garantir que os formatos de entrada para os arquivos que você escreve corresponderem aos dados que você envia para o autor. Cada codec tem um formato de mídia de entrada padrão definido no autor quando o perfil é carregado. Você pode examinar o formato de entrada padrão chamando [**IWMWriter::GetInputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)

Os codecs de vídeo são suportados nos seguintes formatos: IYUV, I420, YV12, YUY2, UYVY, YVYU, Y LTD9, RGB 32, RGB 24, RGB 565, RGB 555 e RGB 8. Os codecs de áudio são suportados por áudio PCM.

Para enumerar os formatos de entrada com suporte de um codec, execute as seguintes etapas:

1.  Criar um objeto writer e definir um perfil a ser usado. Para obter mais informações sobre como definir perfis no autor, consulte [Para usar perfis com o Writer](to-use-profiles-with-the-writer.md).
2.  Identifique o número de entrada para o qual você deseja verificar os formatos. Para obter mais informações sobre como identificar números de entrada, [consulte Para identificar entradas por número](to-identify-inputs-by-number.md).
3.  Recupere o número total de formatos de entrada com suporte pela entrada desejada chamando [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount).
4.  Executar um loop em todos os formatos de entrada com suporte, executando as etapas a seguir para cada um.
    -   Recupere a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para o formato de entrada chamando [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat).
    -   Recupere a [**estrutura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o formato de entrada. Chame [**IWMMediaProps::GetMediaType,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)passando **NULL** para o *parâmetro pType* para obter o tamanho da estrutura. Em seguida, aloce a memória para manter a estrutura e chame **GetMediaType** novamente para obter a estrutura. [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) herda de [**IWMMediaProps,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)portanto, você pode fazer as chamadas para **GetMediaType** da instância de **IWMInputMediaProps** recuperadas na etapa anterior.
    -   O formato descrito na estrutura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contém todas as informações pertinentes sobre o formato de entrada. O formato básico da mídia é identificado por **WM \_ MEDIA \_ TYPE.subtype**. Para fluxos de vídeo, o membro **pbFormat** aponta para uma estrutura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) alocada dinamicamente que contém mais detalhes sobre o fluxo, incluindo o tamanho do retângulo. O tamanho dos quadros de entrada não é necessário para corresponder exatamente a um tamanho com suporte do codec. Se eles não corresponderem, os componentes de tempo de run-time do SDK, em muitos casos, reorganizarão automaticamente os quadros de vídeo de entrada para algo que o codec possa aceitar.

O código de exemplo a seguir localiza o formato de entrada do subtipo passado como um parâmetro. Para obter mais informações sobre como usar esse código, [consulte Usando os exemplos de código](using-the-code-examples.md).


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

[**IWMWriter Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




