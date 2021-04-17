---
title: Elemento meta
description: O elemento meta especifica os metadados que se aplicam à lista de reprodução inteira.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Elemento meta do Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749555"
---
# <a name="meta-element"></a><span data-ttu-id="77135-104">Elemento meta</span><span class="sxs-lookup"><span data-stu-id="77135-104">meta Element</span></span>

<span data-ttu-id="77135-105">O elemento **meta** especifica os metadados que se aplicam à lista de reprodução inteira.</span><span class="sxs-lookup"><span data-stu-id="77135-105">The **meta** element specifies metadata that applies to the entire playlist.</span></span>

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a><span data-ttu-id="77135-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="77135-106">Attributes</span></span>



| <span data-ttu-id="77135-107">Termo</span><span class="sxs-lookup"><span data-stu-id="77135-107">Term</span></span>                                                                       | <span data-ttu-id="77135-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="77135-108">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77135-109"><span id="name"></span><span id="NAME"></span>**nomes**</span><span class="sxs-lookup"><span data-stu-id="77135-109"><span id="name"></span><span id="NAME"></span>**name**</span></span><br/>          | <span data-ttu-id="77135-110">O nome de um item de metadados.</span><span class="sxs-lookup"><span data-stu-id="77135-110">The name of an item of metadata.</span></span><br/>                                                                                       |
| <span data-ttu-id="77135-111"><span id="content"></span><span id="CONTENT"></span>**disputa**</span><span class="sxs-lookup"><span data-stu-id="77135-111"><span id="content"></span><span id="CONTENT"></span>**content**</span></span><br/> | <span data-ttu-id="77135-112">O valor de um item de metadados.</span><span class="sxs-lookup"><span data-stu-id="77135-112">The value of an item of metadata.</span></span> <span data-ttu-id="77135-113">Por exemplo, se o atributo name for "gênero", o atributo Content poderá ser "rock".</span><span class="sxs-lookup"><span data-stu-id="77135-113">For example, if the name attribute is "Genre" the content attribute could be "Rock".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="77135-114">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="77135-114">Parent/Child Elements</span></span>



| <span data-ttu-id="77135-115">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="77135-115">Hierarchy</span></span> | <span data-ttu-id="77135-116">Elementos</span><span class="sxs-lookup"><span data-stu-id="77135-116">Elements</span></span>                 |
|-----------|--------------------------|
| <span data-ttu-id="77135-117">Pai</span><span class="sxs-lookup"><span data-stu-id="77135-117">Parent</span></span>    | [<span data-ttu-id="77135-118">principal</span><span class="sxs-lookup"><span data-stu-id="77135-118">head</span></span>](head-element.md) |
| <span data-ttu-id="77135-119">Filho</span><span class="sxs-lookup"><span data-stu-id="77135-119">Child</span></span>     | <span data-ttu-id="77135-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="77135-120">None</span></span>                     |



 

## <a name="remarks"></a><span data-ttu-id="77135-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="77135-121">Remarks</span></span>

<span data-ttu-id="77135-122">O criador de uma playlist do Windows Media pode definir o atributo Name de um elemento meta para qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="77135-122">The creator of a Windows Media Playlist can set the name attribute of a meta element to any string.</span></span> <span data-ttu-id="77135-123">A lista a seguir mostra alguns atributos de nome típicos que são encontrados nas listas de reprodução do Windows Media criadas pelo Windows Media Player e outros componentes da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="77135-123">The following list shows some typical name attributes that are found in Windows Media Playlists created by Windows Media Player and other Microsoft components.</span></span>

-   <span data-ttu-id="77135-124">Autor</span><span class="sxs-lookup"><span data-stu-id="77135-124">Author</span></span>
-   <span data-ttu-id="77135-125">Categoria</span><span class="sxs-lookup"><span data-stu-id="77135-125">Category</span></span>
-   <span data-ttu-id="77135-126">Gênero</span><span class="sxs-lookup"><span data-stu-id="77135-126">Genre</span></span>
-   <span data-ttu-id="77135-127">UserName</span><span class="sxs-lookup"><span data-stu-id="77135-127">UserName</span></span>
-   <span data-ttu-id="77135-128">UserRating</span><span class="sxs-lookup"><span data-stu-id="77135-128">UserRating</span></span>
-   <span data-ttu-id="77135-129">Gerador</span><span class="sxs-lookup"><span data-stu-id="77135-129">Generator</span></span>

## <a name="examples"></a><span data-ttu-id="77135-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="77135-130">Examples</span></span>


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a><span data-ttu-id="77135-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77135-131">Requirements</span></span>



| <span data-ttu-id="77135-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="77135-132">Requirement</span></span> | <span data-ttu-id="77135-133">Valor</span><span class="sxs-lookup"><span data-stu-id="77135-133">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="77135-134">Versão</span><span class="sxs-lookup"><span data-stu-id="77135-134">Version</span></span><br/> | <span data-ttu-id="77135-135">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="77135-135">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77135-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="77135-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77135-137">**Elemento head**</span><span class="sxs-lookup"><span data-stu-id="77135-137">**head Element**</span></span>](head-element.md)
</dt> <dt>

[<span data-ttu-id="77135-138">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="77135-138">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





