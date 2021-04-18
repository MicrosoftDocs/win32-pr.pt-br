---
description: A partir do Windows 7, Microsoft Media Foundation expõe os metadados por meio da interface IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Provedores de metadados do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788685"
---
# <a name="shell-metadata-providers"></a><span data-ttu-id="f0582-103">Provedores de metadados do Shell</span><span class="sxs-lookup"><span data-stu-id="f0582-103">Shell Metadata Providers</span></span>

<span data-ttu-id="f0582-104">A partir do Windows 7, Microsoft Media Foundation expõe os metadados por meio da interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="f0582-104">Starting in Windows 7, Microsoft Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span>

<span data-ttu-id="f0582-105">Os metadados obtidos usando o processo definido neste tópico devem ser usados somente para acesso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f0582-105">Metadata obtained using the process defined in this topic should only be used for read-only access.</span></span> <span data-ttu-id="f0582-106">Não há suporte para a gravação de dados usando esse processo.</span><span class="sxs-lookup"><span data-stu-id="f0582-106">Writing data using this process is not supported.</span></span> <span data-ttu-id="f0582-107">Você pode criar um objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para fins de escrita usando um identificador de classe (CLSID) obtido do [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span><span class="sxs-lookup"><span data-stu-id="f0582-107">You can create an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object for writing purposes using a class identifier (CLSID) obtained from [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).</span></span>

## <a name="reading-metadata"></a><span data-ttu-id="f0582-108">Lendo metadados</span><span class="sxs-lookup"><span data-stu-id="f0582-108">Reading Metadata</span></span>

<span data-ttu-id="f0582-109">Para ler metadados de uma fonte de mídia, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="f0582-109">To read metadata from a media source, perform the following steps:</span></span>

1.  <span data-ttu-id="f0582-110">Obtenha um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="f0582-110">Get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span> <span data-ttu-id="f0582-111">Você pode usar a interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) para obter um ponteiro **IMFMediaSource** .</span><span class="sxs-lookup"><span data-stu-id="f0582-111">You can use the [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface to get an **IMFMediaSource** pointer.</span></span>
2.  <span data-ttu-id="f0582-112">Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) na origem de mídia para obter um ponteiro para a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="f0582-112">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media source to get a pointer to the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="f0582-113">No parâmetro *guidService* de **MFGetService**, especifique o valor do **\_ serviço de \_ manipulador \_ de propriedades MF**.</span><span class="sxs-lookup"><span data-stu-id="f0582-113">In the *guidService* parameter of **MFGetService**, specify the value **MF\_PROPERTY\_HANDLER\_SERVICE**.</span></span> <span data-ttu-id="f0582-114">Se a origem não oferecer suporte à interface **IPropertyStore** , **MFGetService** retornará **o \_ serviço MF E \_ sem \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="f0582-114">If the source does not support the **IPropertyStore** interface, **MFGetService** returns **MF\_E\_UNSUPPORTED\_SERVICE**.</span></span>
3.  <span data-ttu-id="f0582-115">Chame os métodos [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para enumerar as propriedades de metadados.</span><span class="sxs-lookup"><span data-stu-id="f0582-115">Call [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) methods to enumerate the metadata properties.</span></span>

<span data-ttu-id="f0582-116">O código a seguir mostra essas etapas.</span><span class="sxs-lookup"><span data-stu-id="f0582-116">The following code shows these steps.</span></span> <span data-ttu-id="f0582-117">Suponha que `DisplayProperty` seja uma função que exibe um valor de **PROPVARIANT** .</span><span class="sxs-lookup"><span data-stu-id="f0582-117">Assume that `DisplayProperty` is a function that displays a **PROPVARIANT** value.</span></span>


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



<span data-ttu-id="f0582-118">Para obter uma lista de chaves de propriedade de metadados, consulte [Propriedades de metadados para arquivos de mídia](metadata-properties-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="f0582-118">For a list of metadata property keys, see [Metadata Properties for Media Files](metadata-properties-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0582-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0582-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0582-120">Metadados de mídia</span><span class="sxs-lookup"><span data-stu-id="f0582-120">Media Metadata</span></span>](media-metadata.md)
</dt> </dl>

 

 
