---
title: Elemento seq
description: O elemento seq contém elementos que definem uma lista de reprodução estática ou elementos que definem uma lista de reprodução inteligente.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Elemento seq Windows Media Player
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751779"
---
# <a name="seq-element"></a><span data-ttu-id="ece5c-104">Elemento seq</span><span class="sxs-lookup"><span data-stu-id="ece5c-104">seq Element</span></span>

<span data-ttu-id="ece5c-105">O elemento **Seq** contém elementos que definem uma lista de reprodução estática ou elementos que definem uma lista de reprodução inteligente.</span><span class="sxs-lookup"><span data-stu-id="ece5c-105">The **seq** element contains elements that define a static playlist or elements that define a smart playlist.</span></span>

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a><span data-ttu-id="ece5c-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ece5c-106">Attributes</span></span>

<span data-ttu-id="ece5c-107">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="ece5c-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="ece5c-108">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="ece5c-108">Parent/Child Elements</span></span>



| <span data-ttu-id="ece5c-109">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="ece5c-109">Hierarchy</span></span> | <span data-ttu-id="ece5c-110">Elementos</span><span class="sxs-lookup"><span data-stu-id="ece5c-110">Elements</span></span>                                                               |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="ece5c-111">Pai</span><span class="sxs-lookup"><span data-stu-id="ece5c-111">Parent</span></span>    | [<span data-ttu-id="ece5c-112">body</span><span class="sxs-lookup"><span data-stu-id="ece5c-112">body</span></span>](body-element.md)                                               |
| <span data-ttu-id="ece5c-113">Filho</span><span class="sxs-lookup"><span data-stu-id="ece5c-113">Child</span></span>     | <span data-ttu-id="ece5c-114">[mídia](media-element.md), [smartPlaylist](smartplaylist-element.md)</span><span class="sxs-lookup"><span data-stu-id="ece5c-114">[media](media-element.md), [smartPlaylist](smartplaylist-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ece5c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ece5c-115">Remarks</span></span>

<span data-ttu-id="ece5c-116">Quando um elemento **Seq** contém apenas elementos de **mídia** que fazem referência a itens de mídia específicos, a playlist é considerada estática.</span><span class="sxs-lookup"><span data-stu-id="ece5c-116">When a **seq** element only contains **media** elements that reference specific media items, the playlist is considered to be static.</span></span> <span data-ttu-id="ece5c-117">Quando um elemento **Seq** contém um elemento **smartPlaylist** , é considerado uma lista de reprodução dinâmica "inteligente".</span><span class="sxs-lookup"><span data-stu-id="ece5c-117">When a **seq** element contains a **smartPlaylist** element, it is considered to be a dynamic "smart" playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="ece5c-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ece5c-118">Examples</span></span>


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a><span data-ttu-id="ece5c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece5c-119">Requirements</span></span>



| <span data-ttu-id="ece5c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece5c-120">Requirement</span></span> | <span data-ttu-id="ece5c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ece5c-121">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="ece5c-122">Versão</span><span class="sxs-lookup"><span data-stu-id="ece5c-122">Version</span></span><br/> | <span data-ttu-id="ece5c-123">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ece5c-123">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ece5c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ece5c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece5c-125">**Elemento body**</span><span class="sxs-lookup"><span data-stu-id="ece5c-125">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="ece5c-126">**Elemento de mídia**</span><span class="sxs-lookup"><span data-stu-id="ece5c-126">**media Element**</span></span>](media-element.md)
</dt> <dt>

[<span data-ttu-id="ece5c-127">**Elemento smartPlaylist**</span><span class="sxs-lookup"><span data-stu-id="ece5c-127">**smartPlaylist Element**</span></span>](smartplaylist-element.md)
</dt> <dt>

[<span data-ttu-id="ece5c-128">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="ece5c-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





