---
description: Configurando um codificador WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Configurando um codificador WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6324071257dd9d56e33d1dc6ece4886ee73661ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089776"
---
# <a name="configuring-a-wmv-encoder"></a>Configurando um codificador WMV

Para criar um tipo de saída válido para um codificador de vídeo do Windows Media (WMV), você deve ter as seguintes informações:

-   O formato do vídeo descompactado que você codificará.
-   O subtipo de vídeo que repesents o formato WMV codificado. Consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).
-   A taxa de bits de destino para o fluxo codificado.
-   As propriedades de configuração a serem definidas no codificador.

As propriedades de configuração estão documentadas na documentação do codec de áudio e vídeo do Windows Media e das APIs do DSP. Para obter mais informações, consulte "Propriedades do fluxo de vídeo" em [Propriedades de codificação](configuring-the-encoder.md).

Para obter um tipo de saída válido para o codificador, execute as etapas a seguir.

1.  Use a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para criar uma instância do codificador.
2.  Consulte o codificador para a interface **IPropertyStore** .
3.  Use a interface **IPropertyStore** para configurar o codificador.
4.  Chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o tipo de vídeo descompactado no codificador.
5.  Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter a lista de formatos de compactação do codificador. Os codificadores WMV não retornam um tipo de mídia completo desse método. Há duas informações ausentes nos tipos de mídia:

    -   A taxa de bits de destino.
    -   Dados de codec privado do codificador.

    Antes de definir o tipo de saída no codificador, você deve adicionar ambos esses itens ao tipo de mídia.

6.  Para especificar a taxa de bits de destino, defina o atributo de [**\_ média de taxa de \_ \_ bits MF MT**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia.
7.  Adicione os dados do codec privado ao tipo de mídia, conforme explicado na próxima seção.
8.  Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.

### <a name="private-codec-data"></a>Dados de codec privado

Os dados do codec privado são uma estrutura de dados opaca que você deve obter do codificador WMV e adicionar ao tipo de compactação antes de definir o tipo de compactação no codificador. Para obter os dados privados, você deve usar a interface **IWMCodecPrivateData** , que está documentada no SDK do Windows Media Format 11.

Para obter os dados do codec privado, execute as seguintes etapas:

1.  Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter um tipo de mídia do codificador. (Esta é a etapa 6 da seção anterior.)
2.  Especifique a taxa de bits de destino definindo o atributo de [**\_ média de taxa de \_ \_ bits MF MT**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia.
3.  Converta o tipo de mídia em uma estrutura de [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) chamando a função [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .
4.  Consulte o codificador para a interface **IWMCodecPrivateData** .
5.  Chame o método **IWMCodecPrivateData:: SetPartialOutputType** , passando a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertido.
6.  Chame o método **IWMCodecPrivateData:: GetPrivateData** duas vezes, uma vez para obter o tamanho do buffer para os dados privados e uma vez para copiar os dados no buffer.
7.  Adicione os dados privados ao tipo de mídia definindo o atributo [**de \_ \_ \_ dados de usuário MF MT**](mf-mt-user-data-attribute.md) no tipo.

O exemplo estendido a seguir mostra como criar um formato de compactação WMV a partir de um tipo de vídeo descompactado:


```C++
#include <wmcodecdsp.h>
#include <Wmsdk.h>
#include <Dmo.h>
#include <mfapi.h>
#include <uuids.h>

#include <mfidl.h>
#include <mftransform.h>
#include <mferror.h>

#pragma comment(lib, "Msdmo")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "strmiids")
#pragma comment(lib, "propsys")

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn, 
    REFGUID subtype,
    UINT32 TargetBitrate, 
    IPropertyStore *pEncoderProps, 
    IMFMediaType **ppEncodingType,
    DWORD mftEnumFlags = MFT_ENUM_FLAG_SYNCMFT
    );

HRESULT CreateVideoEncoder(REFGUID subtype, DWORD mftEnumFlags, IMFTransform **ppMFT);
HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut);
HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest);

//
// GetEncodedVideoType
// Given an uncompressed video type, finds a suitable WMV type.
//

HRESULT GetEncodedVideoType(
    IMFMediaType *pTypeIn,          // Uncompressed format
    REFGUID subtype,                // Compression format
    UINT32 TargetBitrate,           // Target bit rate
    IPropertyStore *pEncoderProps,  // Encoder properties (can be NULL)
    IMFMediaType **ppEncodingType,  // Receives the WMV type.
    DWORD mftEnumFlags              // MFTEnumEx flags
    )
{
    HRESULT hr = S_OK;

    IMFTransform *pMFT = NULL;
    IPropertyStore *pPropStore = NULL;
    IMFMediaType *pTypeOut = NULL;

    // Instantiate the encoder
    hr = CreateVideoEncoder(subtype, mftEnumFlags, &pMFT);

    // Copy the properties to the encoder.

    if (SUCCEEDED(hr))
    {
        if (pEncoderProps)
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPropStore));

            if (SUCCEEDED(hr))
            {
                hr = CopyPropertyStore(pEncoderProps, pPropStore);
            }
        }
    }

    // Set the uncompressed type.
    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetInputType(0, pTypeIn, 0);
    }

    // Get the partial output type
    if (SUCCEEDED(hr))
    {
        hr = pMFT->GetOutputAvailableType(0, 0, &pTypeOut);
    }

    // Set the bit rate.
    // You must set this before getting the codec private data.

    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetUINT32(MF_MT_AVG_BITRATE, TargetBitrate);   
    }

    if (SUCCEEDED(hr))
    {
        hr = AddPrivateData(pMFT, pTypeOut);
    }

    if (SUCCEEDED(hr))
    {
        hr = pMFT->SetOutputType(0, pTypeOut, 0);
    }

    if (SUCCEEDED(hr))
    {
        *ppEncodingType = pTypeOut;
        (*ppEncodingType)->AddRef();
    }

    SafeRelease(&pMFT);
    SafeRelease(&pPropStore);
    SafeRelease(&pTypeOut);
    return hr;
}
```



A função CreateVideoEncoder cria um codificador de vídeo para um subtipo de vídeo especificado, como **MFVideoFormat \_ WMV3**:


```C++
//
// CreateVideoEncoder
// Creates a video encoder for a specified video subtype.
//

HRESULT CreateVideoEncoder(
    REFGUID subtype,            // Encoding subtype.
    DWORD mftEnumFlags,         // Flags for MFTEnumEx
    IMFTransform **ppMFT        // Receives a pointer to the encoder.
    )
{
    HRESULT hr = S_OK;
    IMFTransform *pMFT = NULL;

    MFT_REGISTER_TYPE_INFO info;
    info.guidMajorType = MFMediaType_Video;
    info.guidSubtype = subtype;

    IMFActivate **ppActivates = NULL;    
    UINT32 count = 0;

    hr = MFTEnumEx(
        MFT_CATEGORY_VIDEO_ENCODER,
        mftEnumFlags | MFT_ENUM_FLAG_SORTANDFILTER,
        NULL,
        &info,
        &ppActivates,
        &count
        );

    if (count == 0)
    {
        hr = E_FAIL;
    }

    if (SUCCEEDED(hr))
    {
        hr = ppActivates[0]->ActivateObject(
            __uuidof(IMFTransform),
            (void**)&pMFT
            );
    }

    if (SUCCEEDED(hr))
    {
        *ppMFT = pMFT;
        (*ppMFT)->AddRef();
    }

    // Clean up

    for (DWORD i = 0; i < count; i++)
    {
        ppActivates[i]->Release();
    }
    CoTaskMemFree(ppActivates);
    SafeRelease(&pMFT);
    return hr;
}
```



A função AddPrivateData adiciona os dados do codec privado ao tipo de compactação:


```C++
//
// AddPrivateData
// Appends the private codec data to a media type.
//
// pMFT: The video encoder
// pTypeOut: A video type from the encoder's type list.
//
// The function modifies pTypeOut by adding the codec data.
//

HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
{
    HRESULT hr = S_OK;
    ULONG cbData = 0;
    BYTE *pData = NULL;

    IWMCodecPrivateData *pPrivData = NULL;

    DMO_MEDIA_TYPE mtOut = { 0 };

    // Convert the type to a DMO type.
    hr = MFInitAMMediaTypeFromMFMediaType(
        pTypeOut, 
        FORMAT_VideoInfo, 
        (AM_MEDIA_TYPE*)&mtOut
        );
    
    if (SUCCEEDED(hr))
    {
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
    }

    if (SUCCEEDED(hr))
    {
        hr = pPrivData->SetPartialOutputType(&mtOut);
    }

    //
    // Get the private codec data
    //

    // First get the buffer size.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(NULL, &cbData);
    }

    if (SUCCEEDED(hr))
    {
        pData = new BYTE[cbData];

        if (pData == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Now get the data.
    if (SUCCEEDED(hr))
    {
        hr = pPrivData->GetPrivateData(pData, &cbData);
    }

    // Add the data to the media type.
    if (SUCCEEDED(hr))
    {
        hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
    }

    delete [] pData;
    MoFreeMediaType(&mtOut);
    SafeRelease(&pPrivData);
    return hr;
}
```



A função CopyPropertyStore é uma função auxiliar que copia as propriedades de um repositório de propriedades para outro:


```C++
//
// CopyPropertyStore
// Helper function to copy properties from one property
// store to another property store.
//

HRESULT CopyPropertyStore(IPropertyStore *pSrc, IPropertyStore *pDest)
{
    HRESULT hr = S_OK;
    DWORD cProps = 0;

    PROPERTYKEY key;
    PROPVARIANT var;

    PropVariantInit(&var);

    hr = pSrc->GetCount(&cProps);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cProps; i++)
        {
            hr = pSrc->GetAt(i, &key);

            if (FAILED(hr)) { break; }

            hr = pSrc->GetValue(key, &var);

            if (FAILED(hr)) { break; }

            hr = pDest->SetValue(key, var);

            if (FAILED(hr)) { break; }

            PropVariantClear(&var);
        }
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> </dl>

 

 
