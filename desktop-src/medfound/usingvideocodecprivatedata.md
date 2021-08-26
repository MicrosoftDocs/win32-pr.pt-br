---
description: Usando dados privados do codec de vídeo
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Usando dados privados do codec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e417d4d83cc3ae3174e1bbf3310a6abb2900e2c5f3323192a8d17643e4066f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887086"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a>Usando dados privados do codec de vídeo (Microsoft Media Foundation)

a saída compactada produzida pelo Windows codecs de vídeo de mídia 9 não pode ser descompactada corretamente sem alguns dados fornecidos pelo codificador. Esses dados, chamados de dados privados do codec, devem ser anexados ao tipo de mídia de saída. Você pode obter os dados privados do codec chamando os métodos da interface [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) . passe a estrutura do [**\_ \_ tipo de mídia de DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) completa para [IWMCodecPrivateData:: SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype). Em seguida, chame [IWMCodecPrivateData:: GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) duas vezes, uma vez para obter o tamanho dos dados e, em seguida, novamente para copiar os dados para um buffer desse tamanho. Crie um novo buffer para manter a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) com os dados privados anexados e copie a estrutura e os dados para esse buffer. por fim, defina o membro **pbFormat** da estrutura do **\_ \_ tipo de mídia DMO** como o endereço do buffer recém-criado e defina o membro **cbFormat** como o tamanho combinado, em bytes, do **VIDEOINFOHEADER** e dos dados privados.

se você estiver usando o MediaFoundation, poderá construir uma estrutura de [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) de uma interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chamando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).

Você deve usar os dados privados do codec obtidos após a primeira configuração das propriedades no codificador. Se alguma propriedade for alterada, você deverá obter novos dados privados. Se você não usar os dados privados obtidos depois que todas as propriedades forem definidas para a sessão de codificação, o decodificador poderá não ser capaz de descompactar os dados.

O exemplo de código a seguir demonstra como obter os dados privados para um tipo de vídeo:


```
HRESULT GetFinalOutputType(DMO_MEDIA_TYPE* pMedia, IMediaObject* pDMO)
{
    // WARNING //
    // This function does not deallocate the memory pointed to by 
    // pMedia->pbFormat. If the VIDEOINFOHEADER referenced by pbFormat
    // was dynamically allocated, a reference to it must be kept before
    //  calling this function so that it can be freed.

    // Perform simple parameter checks.
    if(pMedia == NULL || pDMO == NULL)
        return E_POINTER;
    if(pMedia->formattype != MEDIATYPE_VideoInfo)
        return E_INVALIDARG;

    HRESULT hr = S_OK;

    IWMCodecPrivateData* pPrivData = NULL;
    BYTE* pbData = NULL;
    DWORD cbData = 0;

    BYTE* pbNewVidInf  = NULL;
    DWORD cbNewVidInf  = 0;
    BYTE* pbNewPriv    = NULL;

    // Get the private data interface.
    hr = pDMO->QueryInterface(IID_IWMCodecPrivateData,
                              (void**)&pPrivData);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the partial media type.
    hr = pPrivData->SetPartialOutputType(pMedia);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the size of the private data.
    hr = pPrivData->GetPrivateData(NULL, &cbData);
    GOTO_EXIT_IF_FAILED(hr);

    // Allocate memory for the private data.
    pbData = new BYTE[cbData];
    if(pbData == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto Exit:
    }

    // Get the private data.
    hr = pPrivData->GetPrivateData(pbData, &cbData);

    // Allocate memory for the new VIDEOINFOHEADER.
    cbNewVidInf = pMedia->cbFormat + cbData;
    pbNewVidInf = new BYTE[cbNewVidInf];

    // Copy the VIDEOINFOHEADER to the new buffer.
    memcpy((void*)pbNewVidInf, (void*)pMedia->pbFormat, pMedia->cbFormat);

    // Get the address of the first byte following the VIDEOINFOHEADER.
    pbNewPriv = pbNewVidInf + pMedia->cbFormat;

    // Copy the private data to the new buffer.
    memcpy((void*)pbNewPriv, (void*)pbData, cbData);

    // Set the new VIDEOINFOHEADER in the DMO_MEDIA_TYPE.
    pMedia->pbFormat = pbNewVidInf;
    pMedia->cbFormat = cbNewVidInf;

Exit:
    SAFE_RELEASE(pPrivData);
    SAFE_ARRAY_DELETE(pbData);
    pbNewPriv = NULL;
    return hr;
}
```



> [!Note]  
> Os dados privados do codec entregues por um codificador de vídeo não têm garantia de serem os mesmos que os dados privados fornecidos por uma implementação diferente do mesmo codec para a mesma configuração. Você sempre deve gerar esse valor usando as etapas neste tópico; Nunca Copie os dados privados de outro arquivo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a codificação de vídeo](configuringvideoencoding.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
