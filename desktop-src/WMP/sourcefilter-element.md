---
title: Elemento sourceFilter
description: O elemento sourceFilter contém elementos que selecionam itens de uma biblioteca.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Elemento sourceFilter do Windows Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750186"
---
# <a name="sourcefilter-element"></a><span data-ttu-id="fc9d4-104">Elemento sourceFilter</span><span class="sxs-lookup"><span data-stu-id="fc9d4-104">sourceFilter Element</span></span>

<span data-ttu-id="fc9d4-105">O elemento **sourceFilter** contém elementos que selecionam itens de uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-105">The **sourceFilter** element contains elements that select items from a library.</span></span>

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a><span data-ttu-id="fc9d4-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc9d4-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="fc9d4-107"><span id="type"></span><span id="TYPE"></span>**Escreva**</span><span class="sxs-lookup"><span data-stu-id="fc9d4-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="fc9d4-108">O tipo de objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-108">The type of filter object.</span></span> <span data-ttu-id="fc9d4-109">Não há valores predefinidos para este atributo.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="fc9d4-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="fc9d4-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="fc9d4-111">O GUID que identifica exclusivamente o objeto de filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-111">The GUID that uniquely identifies the source filter object.</span></span> <span data-ttu-id="fc9d4-112">Os métodos do objeto de filtro de origem são invocados para interpretar os elementos de **fragmento** contidos no elemento **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="fc9d4-112">The source filter object's methods are invoked to interpret the **fragment** elements contained in the **sourceFilter** element.</span></span>



| <span data-ttu-id="fc9d4-113">Valor</span><span class="sxs-lookup"><span data-stu-id="fc9d4-113">Value</span></span>                                  | <span data-ttu-id="fc9d4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc9d4-114">Description</span></span>                                              |
|----------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="fc9d4-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span><span class="sxs-lookup"><span data-stu-id="fc9d4-115">{4202947A-A563-4B05-A754-A1B4B5989849}</span></span> | <span data-ttu-id="fc9d4-116">O GUID do filtro de origem "música em minha biblioteca".</span><span class="sxs-lookup"><span data-stu-id="fc9d4-116">The GUID for the "Music in my library" source filter.</span></span>    |
| <span data-ttu-id="fc9d4-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span><span class="sxs-lookup"><span data-stu-id="fc9d4-117">{B2D9BDDC-8E49-444B-9BA4-193ABF9C7870}</span></span> | <span data-ttu-id="fc9d4-118">O GUID do filtro de origem "vídeo em minha biblioteca".</span><span class="sxs-lookup"><span data-stu-id="fc9d4-118">The GUID for the "Video in my library" source filter.</span></span>    |
| <span data-ttu-id="fc9d4-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span><span class="sxs-lookup"><span data-stu-id="fc9d4-119">{CC823400-A8E4-4081-B073-D3B6D952FE69}</span></span> | <span data-ttu-id="fc9d4-120">O GUID do filtro de origem "imagens em minha biblioteca".</span><span class="sxs-lookup"><span data-stu-id="fc9d4-120">The GUID for the "Pictures in my library" source filter.</span></span> |
| <span data-ttu-id="fc9d4-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span><span class="sxs-lookup"><span data-stu-id="fc9d4-121">{E5415A66-7763-4BDE-B97F-5557CA73C303}</span></span> | <span data-ttu-id="fc9d4-122">O GUID do filtro de origem "programas de TV em minha biblioteca".</span><span class="sxs-lookup"><span data-stu-id="fc9d4-122">The GUID for the "TV shows in my library" source filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="fc9d4-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="fc9d4-123"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="fc9d4-124">O nome do objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-124">The name of the filter object.</span></span>



| <span data-ttu-id="fc9d4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fc9d4-125">Value</span></span>                  | <span data-ttu-id="fc9d4-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc9d4-126">Description</span></span>                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9d4-127">Música na minha biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc9d4-127">Music in my library</span></span>    | <span data-ttu-id="fc9d4-128">Um objeto de filtro que seleciona itens especificados do conjunto de itens de música na biblioteca do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-128">A filter object that selects specified items from the set of music items in the user's library.</span></span> |
| <span data-ttu-id="fc9d4-129">Vídeo na minha biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc9d4-129">Video in my library</span></span>    | <span data-ttu-id="fc9d4-130">Um objeto de filtro que seleciona itens especificados do conjunto de itens de vídeo na biblioteca do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-130">A filter object that selects specified items from the set of video items in the user's library.</span></span> |
| <span data-ttu-id="fc9d4-131">Imagens na minha biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc9d4-131">Pictures in my library</span></span> | <span data-ttu-id="fc9d4-132">Um objeto de filtro que seleciona itens especificados do conjunto de itens de fotos na biblioteca do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-132">A filter object that selects specified items from the set of photo items in the user's library.</span></span> |
| <span data-ttu-id="fc9d4-133">Programas de TV em minha biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc9d4-133">TV shows in my library</span></span> | <span data-ttu-id="fc9d4-134">Um objeto de filtro que seleciona itens especificados do conjunto de itens de TV na biblioteca do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-134">A filter object that selects specified items from the set of TV items in the user's library.</span></span>    |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="fc9d4-135">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="fc9d4-135">Parent/Child Elements</span></span>



| <span data-ttu-id="fc9d4-136">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="fc9d4-136">Hierarchy</span></span> | <span data-ttu-id="fc9d4-137">Elementos</span><span class="sxs-lookup"><span data-stu-id="fc9d4-137">Elements</span></span>                         |
|-----------|----------------------------------|
| <span data-ttu-id="fc9d4-138">Pai</span><span class="sxs-lookup"><span data-stu-id="fc9d4-138">Parent</span></span>    | [<span data-ttu-id="fc9d4-139">queryset</span><span class="sxs-lookup"><span data-stu-id="fc9d4-139">querySet</span></span>](queryset-element.md) |
| <span data-ttu-id="fc9d4-140">Filho</span><span class="sxs-lookup"><span data-stu-id="fc9d4-140">Child</span></span>     | [<span data-ttu-id="fc9d4-141">fragmento</span><span class="sxs-lookup"><span data-stu-id="fc9d4-141">fragment</span></span>](fragment-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="fc9d4-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc9d4-142">Remarks</span></span>

<span data-ttu-id="fc9d4-143">O elemento **sourceFilter** seleciona itens da biblioteca sem considerar o tamanho do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-143">The **sourceFilter** element selects items from the library without regard for the size of the result set.</span></span> <span data-ttu-id="fc9d4-144">O elemento **Filter** , por outro lado, limita o tamanho do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-144">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="fc9d4-145">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc9d4-145">Examples</span></span>


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
    name = "Music in my library">
        <fragment name = "Genre">
            <argument name = "condition">Is</argument>
            <argument name = "value">Rock</argument>
        </fragment>
        <fragment name = "Album Artist">
            <argument name = "condition">Is Not</argument>
            <argument name = "value">Brenda Diaz</argument>
        </fragment>
</sourceFilter>
```



## <a name="requirements"></a><span data-ttu-id="fc9d4-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc9d4-146">Requirements</span></span>



| <span data-ttu-id="fc9d4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc9d4-147">Requirement</span></span> | <span data-ttu-id="fc9d4-148">Valor</span><span class="sxs-lookup"><span data-stu-id="fc9d4-148">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="fc9d4-149">Versão</span><span class="sxs-lookup"><span data-stu-id="fc9d4-149">Version</span></span><br/> | <span data-ttu-id="fc9d4-150">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-150">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc9d4-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc9d4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc9d4-152">**Elemento Filter**</span><span class="sxs-lookup"><span data-stu-id="fc9d4-152">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="fc9d4-153">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="fc9d4-153">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="fc9d4-154">**Elemento queryset**</span><span class="sxs-lookup"><span data-stu-id="fc9d4-154">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="fc9d4-155">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fc9d4-155">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





