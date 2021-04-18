---
description: Usando dados privados do codec de vídeo
ms.assetid: 0cc24fe4-a5b6-4805-8c8e-3066d12ec4bd
title: Usando dados privados do codec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e86fc31a50d2c4e553b5947717ea930698d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814061"
---
# <a name="using-video-codec-private-data-microsoft-media-foundation"></a><span data-ttu-id="c61c0-103">Usando dados privados do codec de vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="c61c0-103">Using Video Codec Private Data (Microsoft Media Foundation)</span></span>

<span data-ttu-id="c61c0-104">A saída compactada produzida pelos codecs do Windows Media Video 9 não pode ser corretamente descompactada sem alguns dados fornecidos pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="c61c0-104">The compressed output produced by the Windows Media Video 9 codecs cannot be properly decompressed without some data provided by the encoder.</span></span> <span data-ttu-id="c61c0-105">Esses dados, chamados de dados privados do codec, devem ser anexados ao tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="c61c0-105">This data, called codec private data, must be appended to the output media type.</span></span> <span data-ttu-id="c61c0-106">Você pode obter os dados privados do codec chamando os métodos da interface [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) .</span><span class="sxs-lookup"><span data-stu-id="c61c0-106">You can get the codec private data by calling the methods of the [IWMCodecPrivateData](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata) interface.</span></span> <span data-ttu-id="c61c0-107">Passe a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) completa para [IWMCodecPrivateData:: SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span><span class="sxs-lookup"><span data-stu-id="c61c0-107">Pass the otherwise complete [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure to [IWMCodecPrivateData::SetPartialOutputType](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-setpartialoutputtype).</span></span> <span data-ttu-id="c61c0-108">Em seguida, chame [IWMCodecPrivateData:: GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) duas vezes, uma vez para obter o tamanho dos dados e, em seguida, novamente para copiar os dados para um buffer desse tamanho.</span><span class="sxs-lookup"><span data-stu-id="c61c0-108">Then call [IWMCodecPrivateData::GetPrivateData](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprivatedata-getprivatedata) twice, once to get the size of the data, and then again to copy the data to a buffer of that size.</span></span> <span data-ttu-id="c61c0-109">Crie um novo buffer para manter a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) com os dados privados anexados e copie a estrutura e os dados para esse buffer.</span><span class="sxs-lookup"><span data-stu-id="c61c0-109">Create a new buffer to hold the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure with the private data appended, and copy the structure and the data to that buffer.</span></span> <span data-ttu-id="c61c0-110">Por fim, defina o membro **pbFormat** da estrutura do **\_ \_ tipo de mídia DMO** como o endereço do buffer recém-criado e defina o membro **cbFormat** como o tamanho combinado, em bytes, do **VIDEOINFOHEADER** e dos dados privados.</span><span class="sxs-lookup"><span data-stu-id="c61c0-110">Finally, set the **pbFormat** member of the **DMO\_MEDIA\_TYPE** structure to the address of the newly created buffer and set the **cbFormat** member to the combined size, in bytes, of the **VIDEOINFOHEADER** and the private data.</span></span>

<span data-ttu-id="c61c0-111">Se você estiver usando o MediaFoundation, poderá construir uma estrutura de [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) de uma interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) chamando [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span><span class="sxs-lookup"><span data-stu-id="c61c0-111">If you are using MediaFoundation you can construct a [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure from an [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface by calling [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype).</span></span>

<span data-ttu-id="c61c0-112">Você deve usar os dados privados do codec obtidos após a primeira configuração das propriedades no codificador.</span><span class="sxs-lookup"><span data-stu-id="c61c0-112">You must use the codec private data obtained after first setting the properties on the encoder.</span></span> <span data-ttu-id="c61c0-113">Se alguma propriedade for alterada, você deverá obter novos dados privados.</span><span class="sxs-lookup"><span data-stu-id="c61c0-113">If any properties are changed, you must get new private data.</span></span> <span data-ttu-id="c61c0-114">Se você não usar os dados privados obtidos depois que todas as propriedades forem definidas para a sessão de codificação, o decodificador poderá não ser capaz de descompactar os dados.</span><span class="sxs-lookup"><span data-stu-id="c61c0-114">If you do not use the private data obtained after all the properties are set for the encoding session, the decoder may not be able to decompress the data.</span></span>

<span data-ttu-id="c61c0-115">O exemplo de código a seguir demonstra como obter os dados privados para um tipo de vídeo:</span><span class="sxs-lookup"><span data-stu-id="c61c0-115">The following code example demonstrates how to obtain the private data for a video type:</span></span>


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
> <span data-ttu-id="c61c0-116">Os dados privados do codec entregues por um codificador de vídeo não têm garantia de serem os mesmos que os dados privados fornecidos por uma implementação diferente do mesmo codec para a mesma configuração.</span><span class="sxs-lookup"><span data-stu-id="c61c0-116">The codec private data delivered by a video encoder is not guaranteed to be the same as the private data delivered by a different implementation of the same codec for the same configuration.</span></span> <span data-ttu-id="c61c0-117">Você sempre deve gerar esse valor usando as etapas neste tópico; Nunca Copie os dados privados de outro arquivo.</span><span class="sxs-lookup"><span data-stu-id="c61c0-117">You must always generate this value using the steps in this topic; never copy the private data from another file.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c61c0-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c61c0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c61c0-119">Configurando a codificação de vídeo</span><span class="sxs-lookup"><span data-stu-id="c61c0-119">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="c61c0-120">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="c61c0-120">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
