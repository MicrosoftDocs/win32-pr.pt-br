---
description: Usando o DMOs no DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Usando o DMOs no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091739"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="1484f-103">Usando o DMOs no DirectShow</span><span class="sxs-lookup"><span data-stu-id="1484f-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="1484f-104">Aplicativos baseados no DirectShow podem usar DMOs em um grafo de filtro, por meio do filtro de [invólucro do DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="1484f-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="1484f-105">Esse filtro agrega um DMO e manipula todos os detalhes do uso do DMO, como a passagem de dados de e para o DMO, a alocação de objetos [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="1484f-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="1484f-106">Como o DMO é agregado pelo filtro, o aplicativo pode consultar o filtro para todas as interfaces COM que o DMO expõe.</span><span class="sxs-lookup"><span data-stu-id="1484f-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="1484f-107">No entanto, o aplicativo deve permitir que o filtro manipule todas as operações de streaming no DMO.</span><span class="sxs-lookup"><span data-stu-id="1484f-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="1484f-108">Por exemplo, não defina os tipos de mídia, processe os buffers, libere o DMO, bloqueie o DMO, habilite ou desabilite o controle de qualidade ou defina otimizações de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1484f-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="1484f-109">Se você souber o identificador de classe (CLSID) de um DMO específico que deseja usar, poderá inicializar o filtro de invólucro de DMO com esse DMO, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1484f-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="1484f-110">Chame **CoCreateInstance** para criar o filtro de invólucro do DMO.</span><span class="sxs-lookup"><span data-stu-id="1484f-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="1484f-111">Consulte o filtro de invólucro do DMO para a interface [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="1484f-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="1484f-112">Chame o método [**IDMOWrapperFilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) .</span><span class="sxs-lookup"><span data-stu-id="1484f-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="1484f-113">Especifique o CLSID do DMO e o GUID da categoria do DMO.</span><span class="sxs-lookup"><span data-stu-id="1484f-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="1484f-114">Para obter uma lista de categorias de DMO, consulte [GUIDs do DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="1484f-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="1484f-115">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="1484f-115">The following code shows these steps:</span></span>


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



<span data-ttu-id="1484f-116">A função [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera DMOs no registro.</span><span class="sxs-lookup"><span data-stu-id="1484f-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="1484f-117">Essa função usa um conjunto diferente de GUIDs de categoria dos que são usados para filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1484f-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="1484f-118">**Usando o enumerador de dispositivo do sistema com DMOs**</span><span class="sxs-lookup"><span data-stu-id="1484f-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="1484f-119">Em vez de criar diretamente um DMO, você pode usar o [enumerador de dispositivo do sistema](system-device-enumerator.md), que pode enumerar qualquer categoria de DMO com suporte do método **DMOEnum** .</span><span class="sxs-lookup"><span data-stu-id="1484f-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="1484f-120">O enumerador de dispositivo do sistema também inclui DMOs quando enumera determinadas categorias de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1484f-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="1484f-121">A tabela a seguir mostra o mapeamento entre as categorias de DMO e as categorias do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1484f-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



|                             |                                |
|-----------------------------|--------------------------------|
| <span data-ttu-id="1484f-122">Categoria de DMO</span><span class="sxs-lookup"><span data-stu-id="1484f-122">DMO Category</span></span>                | <span data-ttu-id="1484f-123">Equivalente do DirectShow</span><span class="sxs-lookup"><span data-stu-id="1484f-123">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="1484f-124">\_codificador de áudio DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="1484f-124">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="1484f-125">\_AUDIOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="1484f-125">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="1484f-126">\_decodificador de áudio DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="1484f-126">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="1484f-127">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="1484f-127">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="1484f-128">\_codificador de vídeo DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="1484f-128">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="1484f-129">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="1484f-129">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="1484f-130">\_decodificador de vídeo DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="1484f-130">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="1484f-131">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="1484f-131">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="1484f-132">O enumerador de dispositivo do sistema retorna uma lista de objetos moniker.</span><span class="sxs-lookup"><span data-stu-id="1484f-132">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="1484f-133">Se o moniker representar um DMO, o método **IMoniker:: BindToObject** criará automaticamente o filtro de invólucro de DMO e o inicializará com esse DMO.</span><span class="sxs-lookup"><span data-stu-id="1484f-133">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="1484f-134">Portanto, o fato de que um DMO está envolvido é transparente para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1484f-134">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="1484f-135">Para obter mais informações sobre como usar o enumerador de dispositivo do sistema, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="1484f-135">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="1484f-136">**Limitações**</span><span class="sxs-lookup"><span data-stu-id="1484f-136">**Limitations**</span></span>

<span data-ttu-id="1484f-137">Há algumas limitações ao usar o DMOs no DirectShow:</span><span class="sxs-lookup"><span data-stu-id="1484f-137">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="1484f-138">O filtro de invólucro de DMO não dá suporte a DMOs com zero entradas, várias entradas ou zero saídas.</span><span class="sxs-lookup"><span data-stu-id="1484f-138">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="1484f-139">Todas as conexões de PIN no filtro de invólucro do DMO usam a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="1484f-139">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="1484f-140">Os serviços de edição do DirectShow não dão suporte a transições ou efeitos baseados em DMO.</span><span class="sxs-lookup"><span data-stu-id="1484f-140">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1484f-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1484f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1484f-142">Usando DMOs</span><span class="sxs-lookup"><span data-stu-id="1484f-142">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



