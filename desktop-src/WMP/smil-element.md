---
title: Elemento SMIL
description: O elemento SMIL é sempre o elemento de nível superior em um arquivo de lista de reprodução de mídia do Windows (WPL). Ele especifica que o arquivo usa sintaxe e gramática de SMIL (linguagem de integração multimídia sincronizada).
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- Elemento SMIL Windows Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754071"
---
# <a name="smil-element"></a><span data-ttu-id="f5a63-105">Elemento SMIL</span><span class="sxs-lookup"><span data-stu-id="f5a63-105">smil Element</span></span>

<span data-ttu-id="f5a63-106">O elemento **SMIL** é sempre o elemento de nível superior em um arquivo de lista de reprodução de mídia do Windows (WPL).</span><span class="sxs-lookup"><span data-stu-id="f5a63-106">The **smil** element is always the top level element in a Windows Media Playlist (WPL) file.</span></span> <span data-ttu-id="f5a63-107">Ele especifica que o arquivo usa sintaxe e gramática de SMIL (linguagem de integração multimídia sincronizada).</span><span class="sxs-lookup"><span data-stu-id="f5a63-107">It specifies that the file uses SMIL (Synchronized Multimedia Integration Language) syntax and grammar.</span></span>

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a><span data-ttu-id="f5a63-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="f5a63-108">Attributes</span></span>

<span data-ttu-id="f5a63-109">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="f5a63-109">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="f5a63-110">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="f5a63-110">Parent/Child Elements</span></span>



| <span data-ttu-id="f5a63-111">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="f5a63-111">Hierarchy</span></span> | <span data-ttu-id="f5a63-112">Elementos</span><span class="sxs-lookup"><span data-stu-id="f5a63-112">Elements</span></span>                                           |
|-----------|----------------------------------------------------|
| <span data-ttu-id="f5a63-113">Pai</span><span class="sxs-lookup"><span data-stu-id="f5a63-113">Parent</span></span>    | <span data-ttu-id="f5a63-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f5a63-114">None</span></span>                                               |
| <span data-ttu-id="f5a63-115">Filho</span><span class="sxs-lookup"><span data-stu-id="f5a63-115">Child</span></span>     | <span data-ttu-id="f5a63-116">[cabeçalho](head-element.md), [corpo](body-element.md)</span><span class="sxs-lookup"><span data-stu-id="f5a63-116">[head](head-element.md), [body](body-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f5a63-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5a63-117">Remarks</span></span>

<span data-ttu-id="f5a63-118">Cada playlist do Windows Media deve ter o elemento **SMIL** em sua raiz.</span><span class="sxs-lookup"><span data-stu-id="f5a63-118">Every Windows Media Playlist must have the **smil** element at its root.</span></span>

## <a name="examples"></a><span data-ttu-id="f5a63-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f5a63-119">Examples</span></span>


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a><span data-ttu-id="f5a63-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5a63-120">Requirements</span></span>



| <span data-ttu-id="f5a63-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a63-121">Requirement</span></span> | <span data-ttu-id="f5a63-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f5a63-122">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="f5a63-123">Versão</span><span class="sxs-lookup"><span data-stu-id="f5a63-123">Version</span></span><br/> | <span data-ttu-id="f5a63-124">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f5a63-124">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5a63-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5a63-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a63-126">**Elemento body**</span><span class="sxs-lookup"><span data-stu-id="f5a63-126">**body Element**</span></span>](body-element.md)
</dt> <dt>

[<span data-ttu-id="f5a63-127">**Elemento head**</span><span class="sxs-lookup"><span data-stu-id="f5a63-127">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="f5a63-128">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f5a63-128">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





