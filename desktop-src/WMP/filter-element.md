---
title: Elemento Filter
description: O elemento Filter contém elementos que limitam o tamanho de uma lista de reprodução, a duração de uma lista de reprodução ou o número de itens de mídia em uma lista de reprodução.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Elemento Filter do Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796414"
---
# <a name="filter-element"></a><span data-ttu-id="3ef19-104">Elemento Filter</span><span class="sxs-lookup"><span data-stu-id="3ef19-104">filter Element</span></span>

<span data-ttu-id="3ef19-105">O elemento **Filter** contém elementos que limitam o tamanho de uma lista de reprodução, a duração de uma lista de reprodução ou o número de itens de mídia em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="3ef19-105">The **filter** element contains elements that limit the size of a playlist, duration of a playlist, or number of media items in a playlist.</span></span>

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a><span data-ttu-id="3ef19-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="3ef19-106">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="3ef19-107"><span id="type"></span><span id="TYPE"></span>**Escreva**</span><span class="sxs-lookup"><span data-stu-id="3ef19-107"><span id="type"></span><span id="TYPE"></span>**type**</span></span>
</dt> <dd>

<span data-ttu-id="3ef19-108">O tipo de objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="3ef19-108">The type of filter object.</span></span> <span data-ttu-id="3ef19-109">Não há valores predefinidos para este atributo.</span><span class="sxs-lookup"><span data-stu-id="3ef19-109">There are no predefined values for this attribute.</span></span>

</dd> <dt>

<span data-ttu-id="3ef19-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="3ef19-110"><span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="3ef19-111">O GUID que identifica exclusivamente um objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="3ef19-111">The GUID that uniquely identifies a filter object.</span></span> <span data-ttu-id="3ef19-112">Os métodos do objeto de filtro são invocados para interpretar os elementos de **fragmento** contidos no elemento de **filtro** .</span><span class="sxs-lookup"><span data-stu-id="3ef19-112">The filter object's methods are invoked to interpret the **fragment** elements contained in the **filter** element.</span></span>



| <span data-ttu-id="3ef19-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3ef19-113">Value</span></span>                                  | <span data-ttu-id="3ef19-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ef19-114">Description</span></span>                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef19-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span><span class="sxs-lookup"><span data-stu-id="3ef19-115">{BC5E21B0-504C-46F6-82BF-FB975C911AD6}</span></span> | <span data-ttu-id="3ef19-116">A ID do filtro "filtro de playlist automática da Microsoft--limita as listas de reprodução automática por contagem, tamanho ou duração".</span><span class="sxs-lookup"><span data-stu-id="3ef19-116">The id for the "Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration" filter.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3ef19-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nome** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="3ef19-117"><span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (required)</span></span> 
</dt> <dd>

<span data-ttu-id="3ef19-118">O nome do objeto de filtro.</span><span class="sxs-lookup"><span data-stu-id="3ef19-118">The name of the filter object.</span></span>



| <span data-ttu-id="3ef19-119">Valor</span><span class="sxs-lookup"><span data-stu-id="3ef19-119">Value</span></span>                                                                              | <span data-ttu-id="3ef19-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ef19-120">Description</span></span>                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| <span data-ttu-id="3ef19-121">Filtro de playlist automática da Microsoft--limita as listas de reprodução automática por contagem, tamanho ou duração</span><span class="sxs-lookup"><span data-stu-id="3ef19-121">Microsoft Auto Playlist Filter -- Limits auto playlists by count, size or duration</span></span> | <span data-ttu-id="3ef19-122">Limita listas de reprodução automáticas por contagem, tamanho ou duração.</span><span class="sxs-lookup"><span data-stu-id="3ef19-122">Limits auto playlists by count, size, or duration.</span></span> |



 

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="3ef19-123">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="3ef19-123">Parent/Child Elements</span></span>



| <span data-ttu-id="3ef19-124">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="3ef19-124">Hierarchy</span></span> | <span data-ttu-id="3ef19-125">Elementos</span><span class="sxs-lookup"><span data-stu-id="3ef19-125">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="3ef19-126">Pai</span><span class="sxs-lookup"><span data-stu-id="3ef19-126">Parent</span></span>    | [<span data-ttu-id="3ef19-127">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="3ef19-127">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="3ef19-128">Filho</span><span class="sxs-lookup"><span data-stu-id="3ef19-128">Child</span></span>     | [<span data-ttu-id="3ef19-129">fragmento</span><span class="sxs-lookup"><span data-stu-id="3ef19-129">fragment</span></span>](fragment-element.md)           |



 

## <a name="remarks"></a><span data-ttu-id="3ef19-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ef19-130">Remarks</span></span>

<span data-ttu-id="3ef19-131">O elemento **Filter** não adiciona nenhum elemento de mídia a uma lista de reprodução; Ele simplesmente remove ou filtra o conteúdo que foi selecionado pelo elemento **sourceFilter** .</span><span class="sxs-lookup"><span data-stu-id="3ef19-131">The **filter** element does not add any media elements to a playlist; it simply removes or filters out content that was selected by the **sourceFilter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="3ef19-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ef19-132">Examples</span></span>


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a><span data-ttu-id="3ef19-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ef19-133">Requirements</span></span>



| <span data-ttu-id="3ef19-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ef19-134">Requirement</span></span> | <span data-ttu-id="3ef19-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3ef19-135">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="3ef19-136">Versão</span><span class="sxs-lookup"><span data-stu-id="3ef19-136">Version</span></span><br/> | <span data-ttu-id="3ef19-137">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3ef19-137">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ef19-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ef19-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef19-139">**Elemento Argument**</span><span class="sxs-lookup"><span data-stu-id="3ef19-139">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="3ef19-140">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="3ef19-140">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="3ef19-141">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="3ef19-141">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="3ef19-142">**Elemento sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="3ef19-142">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="3ef19-143">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3ef19-143">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





