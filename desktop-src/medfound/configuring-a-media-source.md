---
description: Configurando uma origem de mídia
ms.assetid: 1378bbe6-be94-4be1-b428-5ec58dabd1fa
title: Configurando uma origem de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea741e3c04282af445fbea7be07854bf517ec44f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105751966"
---
# <a name="configuring-a-media-source"></a><span data-ttu-id="f33b5-103">Configurando uma origem de mídia</span><span class="sxs-lookup"><span data-stu-id="f33b5-103">Configuring a Media Source</span></span>

<span data-ttu-id="f33b5-104">Ao usar o [resolvedor de origem](source-resolver.md) para criar uma fonte de mídia, você pode especificar um repositório de propriedades que contém propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="f33b5-104">When you use the [Source Resolver](source-resolver.md) to create a media source, you can specify a property store that contains configuration properties.</span></span> <span data-ttu-id="f33b5-105">Essas propriedades serão usadas para inicializar a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="f33b5-105">These properties will be used to initialize the media source.</span></span> <span data-ttu-id="f33b5-106">O conjunto de propriedades com suporte depende da implementação da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="f33b5-106">The set of supported properties depends on the implementation of the media source.</span></span> <span data-ttu-id="f33b5-107">Nem toda fonte de mídia define as propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="f33b5-107">Not every media source defines configuration properties.</span></span>

<span data-ttu-id="f33b5-108">A tabela a seguir lista as propriedades de configuração para as fontes de mídia fornecidas no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f33b5-108">The following table lists the configuration properties for the media sources that are provided in Media Foundation.</span></span> <span data-ttu-id="f33b5-109">As fontes de mídia de terceiros podem definir suas próprias propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f33b5-109">Third-party media sources can define their own custom properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f33b5-110">Origem da mídia</span><span class="sxs-lookup"><span data-stu-id="f33b5-110">Media source</span></span></th>
<th><span data-ttu-id="f33b5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f33b5-111">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f33b5-112">Origem da rede</span><span class="sxs-lookup"><span data-stu-id="f33b5-112">Network source</span></span></td>
<td><span data-ttu-id="f33b5-113">Consulte <a href="network-source-features.md">recursos de origem da rede</a>.</span><span class="sxs-lookup"><span data-stu-id="f33b5-113">See <a href="network-source-features.md">Network Source Features</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f33b5-114">Fonte de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="f33b5-114">ASF media source</span></span></td>
<td><ul>
<li><span data-ttu-id="f33b5-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span><span class="sxs-lookup"><span data-stu-id="f33b5-115"><a href="mfpkey-asfmediasource-approxseek-property.md"><strong>MFPKEY_ASFMediaSource_ApproxSeek</strong></a></span></span></li>
<li><span data-ttu-id="f33b5-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span><span class="sxs-lookup"><span data-stu-id="f33b5-116"><a href="mfpkey-asfmediasource-iterativeseekifnoindex.md">MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex</a></span></span></li>
<li><span data-ttu-id="f33b5-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span><span class="sxs-lookup"><span data-stu-id="f33b5-117"><a href="mfpkey-asfmediasource-iterativeseek-max-count.md">MFPKEY_ASFMediaSource_IterativeSeek_Max_Count</a></span></span></li>
<li><span data-ttu-id="f33b5-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span><span class="sxs-lookup"><span data-stu-id="f33b5-118"><a href="mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md">MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f33b5-119">Para configurar uma origem, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f33b5-119">To configure a source, perform the following steps.</span></span>

1.  <span data-ttu-id="f33b5-120">Chame **PSCreateMemoryPropertyStore** para criar um novo repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f33b5-120">Call **PSCreateMemoryPropertyStore** to create a new property store.</span></span> <span data-ttu-id="f33b5-121">Essa função retorna um ponteiro **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="f33b5-121">This function returns an **IPropertyStore** pointer.</span></span>
2.  <span data-ttu-id="f33b5-122">Chame **IPropertyStore:: SetValue** para definir uma ou mais propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="f33b5-122">Call **IPropertyStore::SetValue** to set one or more configuration properties.</span></span>
3.  <span data-ttu-id="f33b5-123">Chame uma das funções de criação do resolvedor de origem, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), e passe o ponteiro **IPropertyStore** no parâmetro *pProps* .</span><span class="sxs-lookup"><span data-stu-id="f33b5-123">Call one of the source resolver's creation functions, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), and pass the **IPropertyStore** pointer in the *pProps* parameter.</span></span>


```C++
// Creates a media source from a URL.

HRESULT CreateMediaSource(
    PCWSTR pszURL, 
    IPropertyStore *pConfig,    // Optional, can be NULL
    IMFMediaSource **ppSource
    )
{
    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        DbgLog(L"CreateObjectFromURL");

        hr = pSourceResolver->CreateObjectFromURL(
            pszURL,                     
            MF_RESOLUTION_MEDIASOURCE,  // Create a media source.
            pConfig,                    // Configuration properties.
            &ObjectType,                // Receives the object type. 
            &pSource            
            );

        DbgLog(L"CreateObjectFromURL - FINISHED");

    }

    if (SUCCEEDED(hr))
    {
        hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));
    }

    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="f33b5-124">O resolvedor de origem passa o ponteiro **IPropertyStore** diretamente para o manipulador de esquema ou o manipulador de fluxo de bytes que cria a origem.</span><span class="sxs-lookup"><span data-stu-id="f33b5-124">The source resolver passes the **IPropertyStore** pointer directly to the scheme handler or byte-stream handler that creates the source.</span></span> <span data-ttu-id="f33b5-125">O resolvedor de origem não faz nenhuma tentativa de validar as propriedades.</span><span class="sxs-lookup"><span data-stu-id="f33b5-125">The source resolver makes no attempt to validate the properties.</span></span>

<span data-ttu-id="f33b5-126">Em geral, essas propriedades são usadas para configurações avançadas.</span><span class="sxs-lookup"><span data-stu-id="f33b5-126">Generally, these properties are used for advanced settings.</span></span> <span data-ttu-id="f33b5-127">Se você não fornecer um repositório de propriedades, a origem da mídia ainda deverá funcionar corretamente com as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="f33b5-127">If you don't provide a property store, the media source should still function correctly with default settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f33b5-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f33b5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f33b5-129">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="f33b5-129">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



