---
description: Para converter arquivos de mídia em formato ASF, você pode usar codificadores de Mídia do Windows. Saiba mais sobre como criar um codificador usando CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Criando um codificador usando CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068462"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Criando um codificador usando CoCreateInstance

Para converter arquivos de mídia em formato ASF, você pode usar codificadores de Mídia do Windows. Para usar esses codificadores, eles devem ser registrados no sistema. Os codificadores são implementados como Media Foundation transformação (MFTs) e devem expor a interface IMFTransform. [](media-foundation-transforms.md) Este tópico descreve como um aplicativo pode obter um ponteiro para a interface IMFTransform necessária do codificador MFT e insinuá-lo para uso.

Para obter informações sobre o registro do codificador, consulte [Instando um codificador MFT](instantiating-the-encoder-mft.md).

-   [Usando a interface IMFTransform de um codificador](#creating-an-encoder-by-using-cocreateinstance)
    -   [Exemplo de criação do codificador](#encoder-creation-example)
-   [Tópicos relacionados](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Usando a interface IMFTransform de um codificador

Após o registro bem-sucedido de codificadores de mídia do Windows com o sistema, um aplicativo pode enumerar os codificadores chamando [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Para pesquisar o codificador correto, você deve especificar o seguinte:

-   O GUID que representa a categoria , que é CODIFICADOR DE ÁUDIO DE CATEGORIA **MFT \_ ou \_ \_ CODIFICADOR** **DE VÍDEO DE CATEGORIA \_ \_ \_ MFT.**

-   O formato a ser corresponder. Isso é definido na estrutura [**MFT \_ REGISTER TYPE \_ \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) que especifica o tipo principal e o subtipo do tipo de mídia no qual o codificador gerará amostras. Essa estrutura é passada no *parâmetro pOutputType.* Para obter informações sobre os tipos com suporte, consulte [GUIDs de tipo de mídia.](media-type-guids.md)

    > [!Note]  
    > As informações de tipo de entrada no *parâmetro pInputType* não são necessárias. Isso acontece porque o tipo de entrada é conhecido pelo aplicativo e o codificador espera que o fluxo de entrada está em um formato descompactado.

     

[**MFTEnum retorna**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) uma matriz de [**ponteiros IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para os MFTs do codificador que corresponderem aos critérios de pesquisa. Você pode insinuar um codificador chamando a função COM **CoCreateInstance** e passando o CLSID do codificador que você deseja usar. Essa função retorna um ponteiro para a interface **IMFTransform** que representa o codificador. Para obter mais informações sobre essa chamada de função, consulte SDK do Windows documentação do Component Object Model (COM).

### <a name="encoder-creation-example"></a>Exemplo de criação do codificador

O exemplo de código a seguir mostra como criar um codificador de áudio ou vídeo.


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inciando um MFT codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> </dl>

 

 



