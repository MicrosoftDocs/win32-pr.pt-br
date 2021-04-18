---
description: Este tutorial mostra como usar a API de transcodificação para codificar um arquivo de áudio do Windows Media (WMA).
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Tutorial: codificando um arquivo WMA'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781378"
---
# <a name="tutorial-encoding-a-wma-file"></a><span data-ttu-id="82ac0-103">Tutorial: codificando um arquivo WMA</span><span class="sxs-lookup"><span data-stu-id="82ac0-103">Tutorial: Encoding a WMA File</span></span>

<span data-ttu-id="82ac0-104">Este tutorial mostra como usar a [API de transcodificação](transcode-api.md) para codificar um arquivo de áudio do Windows Media (WMA).</span><span class="sxs-lookup"><span data-stu-id="82ac0-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode a Windows Media Audio (WMA) file.</span></span>

<span data-ttu-id="82ac0-105">Este tutorial reutiliza a maior parte do código do tutorial [codificando um arquivo MP4](tutorial--encoding-an-mp4-file-.md), portanto, você deve ler o tutorial primeiro.</span><span class="sxs-lookup"><span data-stu-id="82ac0-105">This tutorial reuses most of the code from the tutorial [Encoding an MP4 File](tutorial--encoding-an-mp4-file-.md), so you should read that tutorial first.</span></span> <span data-ttu-id="82ac0-106">O único código que difere é a função `CreateTranscodeProfile` , que cria o perfil transcodificar.</span><span class="sxs-lookup"><span data-stu-id="82ac0-106">The only code that differs is the function `CreateTranscodeProfile`, which creates the transcode profile.</span></span>

## <a name="create-the-transcode-profile"></a><span data-ttu-id="82ac0-107">Criar o perfil transcodificar</span><span class="sxs-lookup"><span data-stu-id="82ac0-107">Create the Transcode Profile</span></span>

<span data-ttu-id="82ac0-108">Um *perfil de transcodificação* descreve os parâmetros de codificação e o contêiner de arquivo.</span><span class="sxs-lookup"><span data-stu-id="82ac0-108">A *transcode profile* describes the encoding parameters and the file container.</span></span> <span data-ttu-id="82ac0-109">Para o WMA, o contêiner de arquivo é um arquivo ASF (Advanced Streaming Format).</span><span class="sxs-lookup"><span data-stu-id="82ac0-109">For WMA, the file container is an Advanced Streaming Format (ASF) file.</span></span> <span data-ttu-id="82ac0-110">O arquivo ASF contém um fluxo de áudio, que é codificado usando o [**codificador de áudio do Windows Media**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="82ac0-110">The ASF file contains an audio stream, which is encoded using the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="82ac0-111">Para criar a topologia de transcodificação, crie o perfil transcodificar e especifique os parâmetros para o fluxo de áudio e o contêiner.</span><span class="sxs-lookup"><span data-stu-id="82ac0-111">To build the transcode topology, create the transcode profile and specify the parameters for the audio stream and the container.</span></span> <span data-ttu-id="82ac0-112">Em seguida, crie a topologia especificando a fonte de entrada, a URL de saída e o perfil de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="82ac0-112">Then create the topology by specifying the input source, the output URL, and the transcode profile.</span></span>

<span data-ttu-id="82ac0-113">Para criar o perfil, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="82ac0-113">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="82ac0-114">Chame a função [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) para criar um perfil de transcodificação vazio.</span><span class="sxs-lookup"><span data-stu-id="82ac0-114">Call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function to create an empty transcode profile.</span></span>
2.  <span data-ttu-id="82ac0-115">Chame [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) para obter uma lista de tipos de mídia de áudio do codificador.</span><span class="sxs-lookup"><span data-stu-id="82ac0-115">Call [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) to get a list of audio media types from the encoder.</span></span> <span data-ttu-id="82ac0-116">Essa função retorna um ponteiro [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que representa uma coleção de ponteiros [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="82ac0-116">This function returns an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) pointer that represents a collection of [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) pointers.</span></span>
3.  <span data-ttu-id="82ac0-117">Escolha o tipo de mídia de áudio que corresponde aos seus requisitos de transcodificação e copie os atributos para um repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="82ac0-117">Choose the audio media type that matches your transcoding requirements and copy the attributes to an attribute store.</span></span> <span data-ttu-id="82ac0-118">Para este tutorial, o primeiro tipo de mídia na lista é usado.</span><span class="sxs-lookup"><span data-stu-id="82ac0-118">For this tutorial, the first media type in the list is used.</span></span>
    -   <span data-ttu-id="82ac0-119">Chame [**IMFCollection:: GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) para selecionar um tipo de mídia de áudio na lista.</span><span class="sxs-lookup"><span data-stu-id="82ac0-119">Call [**IMFCollection::GetElement**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) to select an audio media type from the list.</span></span>
    -   <span data-ttu-id="82ac0-120">Consulte o tipo de mídia para obter um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) do repositório de atributos do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="82ac0-120">Query the media type to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface of the media type's attribute store.</span></span>
    -   <span data-ttu-id="82ac0-121">Chame [**IMFAttributes:: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) para obter o número de atributos contidos no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="82ac0-121">Call [**IMFAttributes::GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) to get the number of attributes contained in the media type.</span></span>
    -   <span data-ttu-id="82ac0-122">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="82ac0-122">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    -   <span data-ttu-id="82ac0-123">Chame [**IMFAttributes:: CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) para copiar os atributos do tipo de mídia para o novo repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="82ac0-123">Call [**IMFAttributes::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) to copy the attributes from the media type to the new attribute store.</span></span>
4.  <span data-ttu-id="82ac0-124">Chame [**IMFTranscodeProfile:: Setaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) para definir os atributos para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="82ac0-124">Call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) to set the attributes for the audio stream.</span></span>
5.  <span data-ttu-id="82ac0-125">Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos para os atributos de nível de contêiner.</span><span class="sxs-lookup"><span data-stu-id="82ac0-125">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
6.  <span data-ttu-id="82ac0-126">Defina o [atributo \_ \_ ContainerType de transcodificar MF](mf-transcode-containertype.md) como **MFTranscodeContainerType \_ ASF**, que especifica um contêiner de arquivo asf.</span><span class="sxs-lookup"><span data-stu-id="82ac0-126">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute to **MFTranscodeContainerType\_ASF**, which specifies an ASF file container.</span></span>
7.  <span data-ttu-id="82ac0-127">Chame [**IMFTranscodeProfile:: Setcontêinerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) para definir os atributos de nível de contêiner no perfil.</span><span class="sxs-lookup"><span data-stu-id="82ac0-127">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes on the profile.</span></span>


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="82ac0-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82ac0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82ac0-129">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="82ac0-129">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 



