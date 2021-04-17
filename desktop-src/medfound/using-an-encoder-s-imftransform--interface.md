---
description: Para converter arquivos de mídia em formato ASF, você pode usar codificadores de mídia do Windows. Para usar esses codificadores, eles devem ser registrados com o sistema.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Criando um codificador usando CoCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a19a3ec13f60e7f602fa4f16854efa060dd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783773"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Criando um codificador usando CoCreateInstance

Para converter arquivos de mídia em formato ASF, você pode usar codificadores de mídia do Windows. Para usar esses codificadores, eles devem ser registrados com o sistema. Os codificadores são implementados como [transformações de Media Foundation](media-foundation-transforms.md) (MFTs) e devem expor a interface IMFTransform. Este tópico descreve como um aplicativo pode obter um ponteiro para a interface IMFTransform do codificador MFT necessário e instanciá-lo para uso.

Para obter informações sobre o registro do codificador, consulte [instanciando um MFT do codificador](instantiating-the-encoder-mft.md).

-   [Usando a interface IMFTransform de um codificador](#creating-an-encoder-by-using-cocreateinstance)
    -   [Exemplo de criação de codificador](#encoder-creation-example)
-   [Tópicos relacionados](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Usando a interface IMFTransform de um codificador

Após o registro bem-sucedido dos codificadores de mídia do Windows com o sistema, um aplicativo pode enumerar os codificadores chamando [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum). Para pesquisar o codificador correto, você deve especificar o seguinte:

-   O GUID que representa a categoria, que é o **\_ \_ \_ codificador de áudio de categoria de MFT** ou o **\_ \_ \_ codificador de vídeo de categoria de MFT**.

-   O formato a ser correspondido. Isso é definido na estrutura [**de \_ \_ \_ informações do tipo de registro de MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) que especifica o tipo e subtipo principais do tipo de mídia no qual o codificador gerará amostras. Essa estrutura é passada no parâmetro *pOutputType* . Para obter informações sobre os tipos com suporte, consulte [GUIDs de tipo de mídia](media-type-guids.md).

    > [!Note]  
    > As informações de tipo de entrada no parâmetro *pInputType* não são necessárias. Isso ocorre porque o tipo de entrada é conhecido pelo aplicativo e o codificador espera que o fluxo de entrada esteja em um formato descompactado.

     

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) retorna uma matriz de ponteiros [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para o codificador MFTs que corresponde aos critérios de pesquisa. Você pode criar uma instância de um codificador chamando a função COM **CoCreateInstance** e passando o CLSID do codificador que você deseja usar. Essa função retorna um ponteiro para a interface **IMFTransform** que representa o codificador. Para obter mais informações sobre essa chamada de função, consulte a documentação do SDK do Windows para o Component Object Model (COM).

### <a name="encoder-creation-example"></a>Exemplo de criação de codificador

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

[Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> </dl>

 

 



