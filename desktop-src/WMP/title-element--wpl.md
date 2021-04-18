---
title: Elemento Title (WPL)
description: O elemento Title especifica um título para a lista de reprodução.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Elemento Title (WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786255"
---
# <a name="title-element-wpl"></a><span data-ttu-id="b8c30-104">Elemento Title (WPL)</span><span class="sxs-lookup"><span data-stu-id="b8c30-104">title Element (WPL)</span></span>

<span data-ttu-id="b8c30-105">O elemento **title** especifica um título para a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b8c30-105">The **title** element specifies a title for the playlist.</span></span>

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a><span data-ttu-id="b8c30-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b8c30-106">Attributes</span></span>

<span data-ttu-id="b8c30-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="b8c30-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b8c30-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="b8c30-108">Parent/Child Elements</span></span>



| <span data-ttu-id="b8c30-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="b8c30-109">Hierarchy</span></span> | <span data-ttu-id="b8c30-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="b8c30-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="b8c30-111">Pai</span><span class="sxs-lookup"><span data-stu-id="b8c30-111">Parent</span></span>    | [<span data-ttu-id="b8c30-112">principal</span><span class="sxs-lookup"><span data-stu-id="b8c30-112">head</span></span>](head-element.md) |
| <span data-ttu-id="b8c30-113">Filho</span><span class="sxs-lookup"><span data-stu-id="b8c30-113">Child</span></span>     | <span data-ttu-id="b8c30-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b8c30-114">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="b8c30-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8c30-115">Remarks</span></span>

<span data-ttu-id="b8c30-116">Ao escolher um título para uma lista de reprodução de mídia do Windows (WPL), considere que o conteúdo da lista de reprodução pode ser dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b8c30-116">When choosing a title for a Windows Media Playlist (WPL), consider that the content of the playlist can be dynamic.</span></span> <span data-ttu-id="b8c30-117">Uma boa abordagem é basear o título na lógica nos elementos de **argumento** porque isso é o que define o conteúdo da lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b8c30-117">A good approach is to base the title on the logic in the **argument** elements because this is what defines the content of the playlist.</span></span> <span data-ttu-id="b8c30-118">Exemplos disso são "minhas músicas de rock favoritas de 1966" ou "dança canções que não reproduzi recentemente".</span><span class="sxs-lookup"><span data-stu-id="b8c30-118">Examples of this are "My Favorite Rock Songs from 1966" or "Dance Songs That I Haven't Played Recently".</span></span>

## <a name="examples"></a><span data-ttu-id="b8c30-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b8c30-119">Examples</span></span>


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a><span data-ttu-id="b8c30-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8c30-120">Requirements</span></span>



| <span data-ttu-id="b8c30-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8c30-121">Requirement</span></span> | <span data-ttu-id="b8c30-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b8c30-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="b8c30-123">Versão</span><span class="sxs-lookup"><span data-stu-id="b8c30-123">Version</span></span><br/> | <span data-ttu-id="b8c30-124">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b8c30-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b8c30-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8c30-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c30-126">**Elemento Argument**</span><span class="sxs-lookup"><span data-stu-id="b8c30-126">**argument Element**</span></span>](argument-element.md)
</dt> <dt>

[<span data-ttu-id="b8c30-127">**Elemento head**</span><span class="sxs-lookup"><span data-stu-id="b8c30-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="b8c30-128">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b8c30-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





