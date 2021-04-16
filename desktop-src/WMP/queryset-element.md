---
title: Elemento queryset
description: O elemento queryset contém elementos que definem quais itens de mídia serão selecionados da biblioteca.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- Elemento queryset Windows Media Player
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4971c2a7f601132640d7654a95dd288f1740a467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765721"
---
# <a name="queryset-element"></a><span data-ttu-id="91d32-104">Elemento queryset</span><span class="sxs-lookup"><span data-stu-id="91d32-104">querySet Element</span></span>

<span data-ttu-id="91d32-105">O elemento **queryset** contém elementos que definem quais itens de mídia serão selecionados da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="91d32-105">The **querySet** element contains elements that define which media items will be selected from the library.</span></span>

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a><span data-ttu-id="91d32-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="91d32-106">Attributes</span></span>

<span data-ttu-id="91d32-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="91d32-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="91d32-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="91d32-108">Parent/Child Elements</span></span>



| <span data-ttu-id="91d32-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="91d32-109">Hierarchy</span></span> | <span data-ttu-id="91d32-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="91d32-110">Elements</span></span>                                   |
|-----------|--------------------------------------------|
| <span data-ttu-id="91d32-111">Pai</span><span class="sxs-lookup"><span data-stu-id="91d32-111">Parent</span></span>    | [<span data-ttu-id="91d32-112">smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="91d32-112">smartPlaylist</span></span>](smartplaylist-element.md) |
| <span data-ttu-id="91d32-113">Filho</span><span class="sxs-lookup"><span data-stu-id="91d32-113">Child</span></span>     | [<span data-ttu-id="91d32-114">sourceFilter</span><span class="sxs-lookup"><span data-stu-id="91d32-114">sourceFilter</span></span>](sourcefilter-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="91d32-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="91d32-115">Remarks</span></span>

<span data-ttu-id="91d32-116">O elemento **queryset** especifica quais itens de mídia devem ser selecionados da biblioteca, sem considerar o tamanho do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="91d32-116">The **querySet** element specifies which media items should be selected from the library, without regard for the size of the result set.</span></span> <span data-ttu-id="91d32-117">O elemento **Filter** , por outro lado, limita o tamanho do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="91d32-117">The **filter** element, on the other hand, limits the size of the result set.</span></span>

## <a name="examples"></a><span data-ttu-id="91d32-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91d32-118">Examples</span></span>


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a><span data-ttu-id="91d32-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91d32-119">Requirements</span></span>



| <span data-ttu-id="91d32-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d32-120">Requirement</span></span> | <span data-ttu-id="91d32-121">Valor</span><span class="sxs-lookup"><span data-stu-id="91d32-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="91d32-122">Versão</span><span class="sxs-lookup"><span data-stu-id="91d32-122">Version</span></span><br/> | <span data-ttu-id="91d32-123">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="91d32-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91d32-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="91d32-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d32-125">**Elemento Argument**</span><span class="sxs-lookup"><span data-stu-id="91d32-125">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="91d32-126">**Elemento Filter**</span><span class="sxs-lookup"><span data-stu-id="91d32-126">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="91d32-127">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="91d32-127">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="91d32-128">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="91d32-128">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="91d32-129">**Elemento sourceFilter**</span><span class="sxs-lookup"><span data-stu-id="91d32-129">**sourceFilter Element**</span></span>](sourcefilter-element.md)
</dt> <dt>

[<span data-ttu-id="91d32-130">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="91d32-130">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





