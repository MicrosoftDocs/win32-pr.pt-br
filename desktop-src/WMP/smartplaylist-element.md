---
title: Elemento smartPlaylist
description: O elemento smartPlaylist contém a parte definida dinamicamente de uma playlist.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Elemento smartPlaylist do Windows Media Player
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797935"
---
# <a name="smartplaylist-element"></a><span data-ttu-id="d5f01-104">Elemento smartPlaylist</span><span class="sxs-lookup"><span data-stu-id="d5f01-104">smartPlaylist Element</span></span>

<span data-ttu-id="d5f01-105">O elemento **smartPlaylist** contém a parte definida dinamicamente de uma playlist.</span><span class="sxs-lookup"><span data-stu-id="d5f01-105">The **smartPlaylist** element contains the dynamically defined portion of a playlist.</span></span>

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a><span data-ttu-id="d5f01-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="d5f01-106">Attributes</span></span>



| <span data-ttu-id="d5f01-107">Termo</span><span class="sxs-lookup"><span data-stu-id="d5f01-107">Term</span></span>                                                                                                                                   | <span data-ttu-id="d5f01-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5f01-108">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f01-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**versão** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="d5f01-109"><span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (required)</span></span> <br/> | <span data-ttu-id="d5f01-110">O número decimal que representa o número de versão do esquema de playlist inteligente.</span><span class="sxs-lookup"><span data-stu-id="d5f01-110">The decimal number representing the version number of the smart playlist schema.</span></span> <span data-ttu-id="d5f01-111">Defina como 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="d5f01-111">Set to 1.0.0.0.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="d5f01-112">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="d5f01-112">Parent/Child Elements</span></span>



| <span data-ttu-id="d5f01-113">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="d5f01-113">Hierarchy</span></span> | <span data-ttu-id="d5f01-114">Elementos</span><span class="sxs-lookup"><span data-stu-id="d5f01-114">Elements</span></span>                                                       |
|-----------|----------------------------------------------------------------|
| <span data-ttu-id="d5f01-115">Pai</span><span class="sxs-lookup"><span data-stu-id="d5f01-115">Parent</span></span>    | [<span data-ttu-id="d5f01-116">Seq</span><span class="sxs-lookup"><span data-stu-id="d5f01-116">seq</span></span>](seq-element.md)                                         |
| <span data-ttu-id="d5f01-117">Filho</span><span class="sxs-lookup"><span data-stu-id="d5f01-117">Child</span></span>     | <span data-ttu-id="d5f01-118">[queryset](queryset-element.md), [filtro](filter-element.md)</span><span class="sxs-lookup"><span data-stu-id="d5f01-118">[querySet](queryset-element.md), [filter](filter-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d5f01-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5f01-119">Remarks</span></span>

<span data-ttu-id="d5f01-120">Um elemento **smartPlaylist** normalmente contém um elemento **queryset** e também pode conter um elemento **Filter** .</span><span class="sxs-lookup"><span data-stu-id="d5f01-120">A **smartPlaylist** element typically contains a **querySet** element and can also contain a **filter** element.</span></span>

## <a name="examples"></a><span data-ttu-id="d5f01-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5f01-121">Examples</span></span>


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
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
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
```



## <a name="requirements"></a><span data-ttu-id="d5f01-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5f01-122">Requirements</span></span>



| <span data-ttu-id="d5f01-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f01-123">Requirement</span></span> | <span data-ttu-id="d5f01-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d5f01-124">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="d5f01-125">Versão</span><span class="sxs-lookup"><span data-stu-id="d5f01-125">Version</span></span><br/> | <span data-ttu-id="d5f01-126">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="d5f01-126">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5f01-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5f01-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f01-128">**Elemento Argument**</span><span class="sxs-lookup"><span data-stu-id="d5f01-128">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="d5f01-129">**Elemento Filter**</span><span class="sxs-lookup"><span data-stu-id="d5f01-129">**filter Element**</span></span>](filter-element.md)
</dt> <dt>

[<span data-ttu-id="d5f01-130">**Elemento Fragment**</span><span class="sxs-lookup"><span data-stu-id="d5f01-130">**fragment Element**</span></span>](fragment-element.md)
</dt> <dt>

[<span data-ttu-id="d5f01-131">**Elemento queryset**</span><span class="sxs-lookup"><span data-stu-id="d5f01-131">**querySet Element**</span></span>](queryset-element.md)
</dt> <dt>

[<span data-ttu-id="d5f01-132">**Elemento seq**</span><span class="sxs-lookup"><span data-stu-id="d5f01-132">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="d5f01-133">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d5f01-133">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





