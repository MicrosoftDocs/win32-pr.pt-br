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
# <a name="configuring-a-wmv-encoder"></a><span data-ttu-id="7fa46-103">Configurando um codificador WMV</span><span class="sxs-lookup"><span data-stu-id="7fa46-103">Configuring a WMV Encoder</span></span>

<span data-ttu-id="7fa46-104">Para criar um tipo de saída válido para um codificador de vídeo do Windows Media (WMV), você deve ter as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="7fa46-104">To create a valid output type for a Windows Media Video (WMV) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="7fa46-105">O formato do vídeo descompactado que você codificará.</span><span class="sxs-lookup"><span data-stu-id="7fa46-105">The format of the uncompressed video that you will encode.</span></span>
-   <span data-ttu-id="7fa46-106">O subtipo de vídeo que repesents o formato WMV codificado.</span><span class="sxs-lookup"><span data-stu-id="7fa46-106">The video subtype that repesents the encoded WMV format.</span></span> <span data-ttu-id="7fa46-107">Consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7fa46-107">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span>
-   <span data-ttu-id="7fa46-108">A taxa de bits de destino para o fluxo codificado.</span><span class="sxs-lookup"><span data-stu-id="7fa46-108">The target bitrate for the encoded stream.</span></span>
-   <span data-ttu-id="7fa46-109">As propriedades de configuração a serem definidas no codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-109">The configuration properties to set on the encoder.</span></span>

<span data-ttu-id="7fa46-110">As propriedades de configuração estão documentadas na documentação do codec de áudio e vídeo do Windows Media e das APIs do DSP.</span><span class="sxs-lookup"><span data-stu-id="7fa46-110">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="7fa46-111">Para obter mais informações, consulte "Propriedades do fluxo de vídeo" em [Propriedades de codificação](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="7fa46-111">For more information, see "Video Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

<span data-ttu-id="7fa46-112">Para obter um tipo de saída válido para o codificador, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fa46-112">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="7fa46-113">Use a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para criar uma instância do codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-113">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="7fa46-114">Consulte o codificador para a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="7fa46-114">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="7fa46-115">Use a interface **IPropertyStore** para configurar o codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-115">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="7fa46-116">Chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o tipo de vídeo descompactado no codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-116">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed video type on the encoder.</span></span>
5.  <span data-ttu-id="7fa46-117">Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter a lista de formatos de compactação do codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-117">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of compression formats from the encoder.</span></span> <span data-ttu-id="7fa46-118">Os codificadores WMV não retornam um tipo de mídia completo desse método.</span><span class="sxs-lookup"><span data-stu-id="7fa46-118">The WMV encoders do not return a complete media type from this method.</span></span> <span data-ttu-id="7fa46-119">Há duas informações ausentes nos tipos de mídia:</span><span class="sxs-lookup"><span data-stu-id="7fa46-119">The media types are missing two pieces of information:</span></span>

    -   <span data-ttu-id="7fa46-120">A taxa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="7fa46-120">The target bitrate.</span></span>
    -   <span data-ttu-id="7fa46-121">Dados de codec privado do codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-121">Private codec data from the encoder.</span></span>

    <span data-ttu-id="7fa46-122">Antes de definir o tipo de saída no codificador, você deve adicionar ambos esses itens ao tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7fa46-122">Before setting the output type on the encoder, you must add both of these items to the media type.</span></span>

6.  <span data-ttu-id="7fa46-123">Para especificar a taxa de bits de destino, defina o atributo de [**\_ média de taxa de \_ \_ bits MF MT**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7fa46-123">To specify the target bitrate, set the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
7.  <span data-ttu-id="7fa46-124">Adicione os dados do codec privado ao tipo de mídia, conforme explicado na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="7fa46-124">Add the private codec data to the media type, as explained in the next section.</span></span>
8.  <span data-ttu-id="7fa46-125">Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de compactação no codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-125">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="private-codec-data"></a><span data-ttu-id="7fa46-126">Dados de codec privado</span><span class="sxs-lookup"><span data-stu-id="7fa46-126">Private Codec Data</span></span>

<span data-ttu-id="7fa46-127">Os dados do codec privado são uma estrutura de dados opaca que você deve obter do codificador WMV e adicionar ao tipo de compactação antes de definir o tipo de compactação no codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-127">The private codec data is an opaque data structure that you must get from the WMV encoder and add to the compression type, before setting the compression type on the encoder.</span></span> <span data-ttu-id="7fa46-128">Para obter os dados privados, você deve usar a interface **IWMCodecPrivateData** , que está documentada no SDK do Windows Media Format 11.</span><span class="sxs-lookup"><span data-stu-id="7fa46-128">To get the private data, you must use the **IWMCodecPrivateData** interface, which is documented in the Windows Media Format 11 SDK.</span></span>

<span data-ttu-id="7fa46-129">Para obter os dados do codec privado, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="7fa46-129">To get the private codec data, perform the following steps:</span></span>

1.  <span data-ttu-id="7fa46-130">Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter um tipo de mídia do codificador.</span><span class="sxs-lookup"><span data-stu-id="7fa46-130">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a media type from the encoder.</span></span> <span data-ttu-id="7fa46-131">(Esta é a etapa 6 da seção anterior.)</span><span class="sxs-lookup"><span data-stu-id="7fa46-131">(This is step 6 from the previous section.)</span></span>
2.  <span data-ttu-id="7fa46-132">Especifique a taxa de bits de destino definindo o atributo de [**\_ média de taxa de \_ \_ bits MF MT**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7fa46-132">Specify the target bitrate by setting the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the media type.</span></span>
3.  <span data-ttu-id="7fa46-133">Converta o tipo de mídia em uma estrutura de [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) chamando a função [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="7fa46-133">Convert the media type into a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure by calling the [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype) function.</span></span>
4.  <span data-ttu-id="7fa46-134">Consulte o codificador para a interface **IWMCodecPrivateData** .</span><span class="sxs-lookup"><span data-stu-id="7fa46-134">Query the encoder for the **IWMCodecPrivateData** interface.</span></span>
5.  <span data-ttu-id="7fa46-135">Chame o método **IWMCodecPrivateData:: SetPartialOutputType** , passando a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) convertido.</span><span class="sxs-lookup"><span data-stu-id="7fa46-135">Call the **IWMCodecPrivateData::SetPartialOutputType** method, passing in the converted [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure.</span></span>
6.  <span data-ttu-id="7fa46-136">Chame o método **IWMCodecPrivateData:: GetPrivateData** duas vezes, uma vez para obter o tamanho do buffer para os dados privados e uma vez para copiar os dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="7fa46-136">Call the **IWMCodecPrivateData::GetPrivateData** method twice, once to get the size of the buffer for the private data, and once to copy the data into the buffer.</span></span>
7.  <span data-ttu-id="7fa46-137">Adicione os dados privados ao tipo de mídia definindo o atributo [**de \_ \_ \_ dados de usuário MF MT**](mf-mt-user-data-attribute.md) no tipo.</span><span class="sxs-lookup"><span data-stu-id="7fa46-137">Add the private data to the media type by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute on the type.</span></span>

<span data-ttu-id="7fa46-138">O exemplo estendido a seguir mostra como criar um formato de compactação WMV a partir de um tipo de vídeo descompactado:</span><span class="sxs-lookup"><span data-stu-id="7fa46-138">The following extended example shows how to create a WMV compression format from an uncompressed video type:</span></span>


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



<span data-ttu-id="7fa46-139">A função CreateVideoEncoder cria um codificador de vídeo para um subtipo de vídeo especificado, como **MFVideoFormat \_ WMV3**:</span><span class="sxs-lookup"><span data-stu-id="7fa46-139">The CreateVideoEncoder function creates a video encoder for a specified video subtype, such as **MFVideoFormat\_WMV3**:</span></span>


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



<span data-ttu-id="7fa46-140">A função AddPrivateData adiciona os dados do codec privado ao tipo de compactação:</span><span class="sxs-lookup"><span data-stu-id="7fa46-140">The AddPrivateData function adds the private codec data to the compression type:</span></span>


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



<span data-ttu-id="7fa46-141">A função CopyPropertyStore é uma função auxiliar que copia as propriedades de um repositório de propriedades para outro:</span><span class="sxs-lookup"><span data-stu-id="7fa46-141">The CopyPropertyStore function is a helper function that copies properties from one property store to another:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7fa46-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fa46-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fa46-143">Criando uma instância de um MFT do codificador</span><span class="sxs-lookup"><span data-stu-id="7fa46-143">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="7fa46-144">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="7fa46-144">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 
