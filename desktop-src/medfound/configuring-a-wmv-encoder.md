---
description: Configurando um codificador WMV
ms.assetid: 6e690d17-da17-452a-aa9a-9701a560856b
title: Configurando um codificador WMV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39001edd5901d09bc618fe92d251070d24633fb94812a9c2696b11866f3cb9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880540"
---
# <a name="configuring-a-wmv-encoder"></a>Configurando um codificador WMV

Para criar um tipo de saída válido para um codificador wmv (vídeo de mídia de Windows), você deve ter as seguintes informações:

-   O formato do vídeo descompactado que você codificará.
-   O subtipo de vídeo que repessa o formato WMV codificado. Consulte [GUIDs de subtipo de vídeo.](video-subtype-guids.md)
-   A taxa de bits de destino para o fluxo codificado.
-   As propriedades de configuração a definir no codificador.

As propriedades de configuração estão documentadas na documentação Windows Codec de Áudio e Vídeo de Mídia e APIs do DSP. Para obter mais informações, consulte "Propriedades de fluxo de vídeo" [em Propriedades de codificação](configuring-the-encoder.md).

Para obter um tipo de saída válido para o codificador, execute as etapas a seguir.

1.  Use a [**função MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para criar uma instância do codificador.
2.  Consulte o codificador para a interface **IPropertyStore.**
3.  Use a interface **IPropertyStore** para configurar o codificador.
4.  Chame [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o tipo de vídeo descompactado no codificador.
5.  Chame [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter a lista de formatos de compactação do codificador. Os codificadores WMV não retornam um tipo de mídia completo desse método. Os tipos de mídia não têm duas informações:

    -   A taxa de bits de destino.
    -   Dados de codec privados do codificador.

    Antes de definir o tipo de saída no codificador, você deve adicionar ambos os itens ao tipo de mídia.

6.  Para especificar a taxa de bits de destino, de definido o atributo [**\_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia.
7.  Adicione os dados de codec privados ao tipo de mídia, conforme explicado na próxima seção.
8.  Chame [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.

### <a name="private-codec-data"></a>Dados de codec privados

Os dados de codec privados são uma estrutura de dados opaca que você deve obter do codificador WMV e adicionar ao tipo de compactação, antes de definir o tipo de compactação no codificador. Para obter os dados privados, você deve usar a interface **IWMCodecPrivateData,** que está documentada no SDK Windows Media Format 11.

Para obter os dados de codec privados, execute as seguintes etapas:

1.  Chame [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter um tipo de mídia do codificador. (Esta é a etapa 6 da seção anterior.)
2.  Especifique a taxa de bits de destino definindo o atributo [**\_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia.
3.  Converta o tipo de mídia [**em uma estrutura DMO MEDIA \_ \_ TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) chamando a [**função MFInitAMMediaTypeFromMFMediaType.**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)
4.  Consulte o codificador para a interface **IWMCodecPrivateData.**
5.  Chame o **método IWMCodecPrivateData::SetPartialOutputType,** passando a estrutura [**DMO MEDIA TYPE \_ \_ convertida.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)
6.  Chame o método **IWMCodecPrivateData::GetPrivateData** duas vezes, uma vez para obter o tamanho do buffer para os dados privados e uma vez para copiar os dados para o buffer.
7.  Adicione os dados privados ao tipo de mídia definindo o atributo [**\_ MF MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md) no tipo.

O exemplo estendido a seguir mostra como criar um formato de compactação WMV de um tipo de vídeo descompactado:


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



A função AddPrivateData adiciona os dados de codec privados ao tipo de compactação:


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



A função CopyPropertyStore é uma função auxiliar que copia propriedades de um repositório de propriedades para outro:


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

[Inciando um MFT codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores de mídia](windows-media-encoders.md)
</dt> </dl>

 

 
