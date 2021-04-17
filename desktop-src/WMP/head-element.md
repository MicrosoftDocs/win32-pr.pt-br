---
title: Elemento head
description: O elemento head contém metadados que se aplicam a toda a lista de reprodução.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Elemento de cabeçalho Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759701"
---
# <a name="head-element"></a><span data-ttu-id="b4833-104">Elemento head</span><span class="sxs-lookup"><span data-stu-id="b4833-104">head Element</span></span>

<span data-ttu-id="b4833-105">O elemento **Head** contém metadados que se aplicam a toda a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b4833-105">The **head** element contains metadata that applies to the entire playlist.</span></span>

``` syntax
<head>
</head>
```

## <a name="attributes"></a><span data-ttu-id="b4833-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4833-106">Attributes</span></span>

<span data-ttu-id="b4833-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="b4833-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b4833-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="b4833-108">Parent/Child Elements</span></span>



| <span data-ttu-id="b4833-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="b4833-109">Hierarchy</span></span> | <span data-ttu-id="b4833-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="b4833-110">Elements</span></span>                                                  |
|-----------|-----------------------------------------------------------|
| <span data-ttu-id="b4833-111">Pai</span><span class="sxs-lookup"><span data-stu-id="b4833-111">Parent</span></span>    | [<span data-ttu-id="b4833-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="b4833-112">smil</span></span>](smil-element.md)                                  |
| <span data-ttu-id="b4833-113">Filho</span><span class="sxs-lookup"><span data-stu-id="b4833-113">Child</span></span>     | <span data-ttu-id="b4833-114">[título](title-element--wpl.md), [meta](meta-element.md)</span><span class="sxs-lookup"><span data-stu-id="b4833-114">[title](title-element--wpl.md), [meta](meta-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b4833-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4833-115">Remarks</span></span>

<span data-ttu-id="b4833-116">Normalmente, o elemento **Head** contém um elemento **title** e um ou mais **meta** Elements que definem características globais da playlist.</span><span class="sxs-lookup"><span data-stu-id="b4833-116">Typically the **head** element contains a **title** element and one or more **meta** elements that define global characteristics of the playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="b4833-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b4833-117">Examples</span></span>


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="b4833-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4833-118">Requirements</span></span>



| <span data-ttu-id="b4833-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4833-119">Requirement</span></span> | <span data-ttu-id="b4833-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b4833-120">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="b4833-121">Versão</span><span class="sxs-lookup"><span data-stu-id="b4833-121">Version</span></span><br/> | <span data-ttu-id="b4833-122">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b4833-122">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4833-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4833-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4833-124">**Elemento meta**</span><span class="sxs-lookup"><span data-stu-id="b4833-124">**meta Element**</span></span>](meta-element.md)
</dt> <dt>

[<span data-ttu-id="b4833-125">**Elemento Title (WPL)**</span><span class="sxs-lookup"><span data-stu-id="b4833-125">**title Element (WPL)**</span></span>](title-element--wpl.md)
</dt> <dt>

[<span data-ttu-id="b4833-126">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b4833-126">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





