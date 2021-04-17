---
title: Elemento body
description: O elemento body contém os elementos que definem o conteúdo de uma playlist.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Elemento body Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761482"
---
# <a name="body-element"></a><span data-ttu-id="72c66-104">Elemento body</span><span class="sxs-lookup"><span data-stu-id="72c66-104">body Element</span></span>

<span data-ttu-id="72c66-105">O elemento **Body** contém os elementos que definem o conteúdo de uma playlist.</span><span class="sxs-lookup"><span data-stu-id="72c66-105">The **body** element contains the elements that define the contents of a playlist.</span></span>

``` syntax
<body>
</body>
```

## <a name="attributes"></a><span data-ttu-id="72c66-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="72c66-106">Attributes</span></span>

<span data-ttu-id="72c66-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="72c66-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="72c66-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="72c66-108">Parent/Child Elements</span></span>



| <span data-ttu-id="72c66-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="72c66-109">Hierarchy</span></span> | <span data-ttu-id="72c66-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="72c66-110">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="72c66-111">Pai</span><span class="sxs-lookup"><span data-stu-id="72c66-111">Parent</span></span>    | [<span data-ttu-id="72c66-112">SMIL</span><span class="sxs-lookup"><span data-stu-id="72c66-112">smil</span></span>](smil-element.md) |
| <span data-ttu-id="72c66-113">Filho</span><span class="sxs-lookup"><span data-stu-id="72c66-113">Child</span></span>     | [<span data-ttu-id="72c66-114">Seq</span><span class="sxs-lookup"><span data-stu-id="72c66-114">seq</span></span>](seq-element.md)   |



 

## <a name="remarks"></a><span data-ttu-id="72c66-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="72c66-115">Remarks</span></span>

<span data-ttu-id="72c66-116">O conteúdo de uma lista de reprodução é organizado em um elemento **Seq** que está contido no elemento **Body** .</span><span class="sxs-lookup"><span data-stu-id="72c66-116">The contents of a playlist are organized within a **seq** element that is contained within the **body** element.</span></span> <span data-ttu-id="72c66-117">Normalmente, há um elemento **Seq** que define um conjunto estático de itens de mídia e contém elementos de **mídia** , ou há um que define um conjunto dinâmico de itens de mídia e contém um elemento **smartPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="72c66-117">Typically there is either one **seq** element that defines a static set of media items and contains **media** elements, or there is one that defines a dynamic set of media items and contains a **smartPlaylist** element.</span></span>

## <a name="examples"></a><span data-ttu-id="72c66-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="72c66-118">Examples</span></span>


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a><span data-ttu-id="72c66-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72c66-119">Requirements</span></span>



| <span data-ttu-id="72c66-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="72c66-120">Requirement</span></span> | <span data-ttu-id="72c66-121">Valor</span><span class="sxs-lookup"><span data-stu-id="72c66-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="72c66-122">Versão</span><span class="sxs-lookup"><span data-stu-id="72c66-122">Version</span></span><br/> | <span data-ttu-id="72c66-123">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="72c66-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72c66-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="72c66-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c66-125">**Elemento de mídia**</span><span class="sxs-lookup"><span data-stu-id="72c66-125">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="72c66-126">**Elemento seq**</span><span class="sxs-lookup"><span data-stu-id="72c66-126">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="72c66-127">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="72c66-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="72c66-128">**Elemento SMIL**</span><span class="sxs-lookup"><span data-stu-id="72c66-128">**smil Element**</span></span>](smil-element.md)
</dt> <dt>

[<span data-ttu-id="72c66-129">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="72c66-129">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





