---
description: No Windows Vista, Microsoft Media Foundation expõe metadados por meio da interface IMFMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Provedores de metadados no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759583"
---
# <a name="metadata-providers-in-windows-vista"></a><span data-ttu-id="9ccb0-103">Provedores de metadados no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ccb0-103">Metadata Providers in Windows Vista</span></span>

<span data-ttu-id="9ccb0-104">No Windows Vista, Microsoft Media Foundation expõe metadados por meio da interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="9ccb0-104">In Windows Vista, Microsoft Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="9ccb0-105">Lendo metadados</span><span class="sxs-lookup"><span data-stu-id="9ccb0-105">Reading Metadata</span></span>

<span data-ttu-id="9ccb0-106">Para ler metadados de uma fonte de mídia, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="9ccb0-106">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="9ccb0-107">Obtenha um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-107">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="9ccb0-108">Você pode usar a interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obter um ponteiro **IMFMediaSource** .</span><span class="sxs-lookup"><span data-stu-id="9ccb0-108">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="9ccb0-109">Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para obter o descritor de apresentação da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-109">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="9ccb0-110">Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) na origem de mídia para obter um ponteiro para a interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .</span><span class="sxs-lookup"><span data-stu-id="9ccb0-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) interface.</span></span> <span data-ttu-id="9ccb0-111">No parâmetro *guidService* de **MFGetService**, especifique o valor **serviço do \_ \_ provedor de \_ metadados MF**.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-111">In the *guidService* parameter of **MFGetService**, specify the value **MF\_METADATA\_PROVIDER\_SERVICE**.</span></span> <span data-ttu-id="9ccb0-112">Se a origem não oferecer suporte à interface **IMFMetadataProvider** , **MFGetService** retornará **o \_ serviço MF E \_ sem \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-112">If the source does not support the **IMFMetadataProvider** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
4.  <span data-ttu-id="9ccb0-113">Chame [**IMFMetadataProvider:: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) e transmita um ponteiro para o descritor de apresentação.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-113">Call [**IMFMetadataProvider::GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) and pass in a pointer to the presentation descriptor.</span></span> <span data-ttu-id="9ccb0-114">Esse método retorna um ponteiro para a interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="9ccb0-114">This method returns a pointer to the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span>
    -   <span data-ttu-id="9ccb0-115">Para obter metadados de nível de fluxo, primeiro chame [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) para obter o identificador de fluxo.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-115">To get stream-level metadata first call [**IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) to get the stream identifier.</span></span> <span data-ttu-id="9ccb0-116">Em seguida, passe o identificador de fluxo no parâmetro *dwStreamIdentifier* de [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span><span class="sxs-lookup"><span data-stu-id="9ccb0-116">Then pass the stream identifier in the *dwStreamIdentifier* parameter of [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).</span></span>
    -   <span data-ttu-id="9ccb0-117">Para obter metadados no nível da apresentação, defina *dwStreamIdentifier* como zero.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-117">To get presentation-level metadata, set *dwStreamIdentifier* to zero.</span></span>
5.  <span data-ttu-id="9ccb0-118">\[\]Chamada opcional [**IMFMetadata:: GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) para obter uma lista dos idiomas nos quais os metadados estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-118">\[Optional\] Call [**IMFMetadata::GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) to get a list of the languages in which metadata is available.</span></span> <span data-ttu-id="9ccb0-119">Os idiomas são identificados usando marcas de idioma compatíveis com o RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-119">Languages are identified using RFC 1766-compliant language tags.</span></span>
6.  <span data-ttu-id="9ccb0-120">\[\]Chamada opcional [**IMFMetadata:: setlanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) para selecionar o idioma.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-120">\[Optional\] Call [**IMFMetadata::SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) to select the language.</span></span>
7.  <span data-ttu-id="9ccb0-121">\[\]Chamada opcional [**IMFMetadata:: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) para obter uma lista dos nomes de todas as propriedades de metadados para este fluxo ou apresentação.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-121">\[Optional\] Call [**IMFMetadata::GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) to get a list of the names of all the metadata properties for this stream or presentation.</span></span>
8.  <span data-ttu-id="9ccb0-122">Chame [**IMFMetadata:: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) para obter um valor de propriedade de metadados específico, passando o nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-122">Call [**IMFMetadata::GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) to get a specific metadata property value, passing in the name of the property.</span></span>

<span data-ttu-id="9ccb0-123">O código a seguir mostra as etapas 2 a 4:</span><span class="sxs-lookup"><span data-stu-id="9ccb0-123">The following code shows steps 2–4:</span></span>


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



<span data-ttu-id="9ccb0-124">O código a seguir mostra as etapas 7 a 8.</span><span class="sxs-lookup"><span data-stu-id="9ccb0-124">The following code shows steps 7–8.</span></span> <span data-ttu-id="9ccb0-125">Suponha que `DisplayProperty` seja uma função que exibe um valor de **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="9ccb0-125">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="9ccb0-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ccb0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ccb0-127">Metadados de mídia</span><span class="sxs-lookup"><span data-stu-id="9ccb0-127">Media Metadata</span></span>](media-metadata.md)
</dt> <dt>

[<span data-ttu-id="9ccb0-128">Provedores de metadados do Shell</span><span class="sxs-lookup"><span data-stu-id="9ccb0-128">Shell Metadata Providers</span></span>](shell-metadata-providers.md)
</dt> </dl>

 

 



