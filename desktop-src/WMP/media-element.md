---
title: Elemento de mídia
description: O elemento Media especifica um dos itens de mídia em uma lista de reprodução.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Elemento de mídia Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751396"
---
# <a name="media-element"></a><span data-ttu-id="f3098-104">Elemento de mídia</span><span class="sxs-lookup"><span data-stu-id="f3098-104">media Element</span></span>

<span data-ttu-id="f3098-105">O elemento **Media** especifica um dos itens de mídia em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f3098-105">The **media** element specifies one of the media items in a playlist.</span></span>

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a><span data-ttu-id="f3098-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="f3098-106">Attributes</span></span>



| <span data-ttu-id="f3098-107">Termo</span><span class="sxs-lookup"><span data-stu-id="f3098-107">Term</span></span>                                                                                                                       | <span data-ttu-id="f3098-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3098-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3098-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="f3098-109"><span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (required)</span></span> <br/> | <span data-ttu-id="f3098-110">A URL de um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="f3098-110">The URL of a media item.</span></span><br/>                                                              |
| <span data-ttu-id="f3098-111"><span id="cid"></span><span id="CID"></span>**CID**</span><span class="sxs-lookup"><span data-stu-id="f3098-111"><span id="cid"></span><span id="CID"></span>**cid**</span></span><br/>                                                             | <span data-ttu-id="f3098-112">A ID de conteúdo que é exclusiva para este item de mídia.</span><span class="sxs-lookup"><span data-stu-id="f3098-112">The content ID that is unique to this media item.</span></span><br/>                                     |
| <span data-ttu-id="f3098-113"><span id="tid"></span><span id="TID"></span>**tid**</span><span class="sxs-lookup"><span data-stu-id="f3098-113"><span id="tid"></span><span id="TID"></span>**tid**</span></span><br/>                                                             | <span data-ttu-id="f3098-114">A ID de rastreamento que pode ser usada para rastrear o objeto do sistema de arquivos para este item de mídia.</span><span class="sxs-lookup"><span data-stu-id="f3098-114">The tracking ID that can be used to track the File System Object for this media item.</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="f3098-115">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="f3098-115">Parent/Child Elements</span></span>



| <span data-ttu-id="f3098-116">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="f3098-116">Hierarchy</span></span> | <span data-ttu-id="f3098-117">Elementos</span><span class="sxs-lookup"><span data-stu-id="f3098-117">Elements</span></span>               |
|-----------|------------------------|
| <span data-ttu-id="f3098-118">Pai</span><span class="sxs-lookup"><span data-stu-id="f3098-118">Parent</span></span>    | [<span data-ttu-id="f3098-119">Seq</span><span class="sxs-lookup"><span data-stu-id="f3098-119">seq</span></span>](seq-element.md) |
| <span data-ttu-id="f3098-120">Filho</span><span class="sxs-lookup"><span data-stu-id="f3098-120">Child</span></span>     | <span data-ttu-id="f3098-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f3098-121">None</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="f3098-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3098-122">Remarks</span></span>

<span data-ttu-id="f3098-123">O atributo **CID** (a ID de conteúdo) é preenchido pelo Windows Media Player como uma maneira de identificar exclusivamente um conteúdo de mídia, mesmo que seus atributos de metadados tenham sido alterados.</span><span class="sxs-lookup"><span data-stu-id="f3098-123">The **cid** attribute (the content ID) is populated by the Windows Media Player as a way to uniquely identify a piece of media content even if its metadata attributes have been changed.</span></span> <span data-ttu-id="f3098-124">Isso permite o compartilhamento de listas de reprodução entre computadores, pois o conteúdo pode ser identificado em outro computador e o caminho para ele pode ser "reparado automaticamente" pela lista de reprodução do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f3098-124">This allows the sharing of playlists across computers, because the content can be identified on another computer, and the path to it can be "auto-repaired" by the Windows Media Playlist.</span></span> <span data-ttu-id="f3098-125">O atributo **tid** (a ID de rastreamento) usa o sistema de arquivos do Windows para reparar automaticamente o caminho para a mídia se o nome ou o local do arquivo for alterado.</span><span class="sxs-lookup"><span data-stu-id="f3098-125">The **tid** attribute (the tracking ID) uses the Windows file system to auto-repair the path to the media if the name or location of the file is changed.</span></span>

## <a name="examples"></a><span data-ttu-id="f3098-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3098-126">Examples</span></span>


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a><span data-ttu-id="f3098-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3098-127">Requirements</span></span>



| <span data-ttu-id="f3098-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3098-128">Requirement</span></span> | <span data-ttu-id="f3098-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f3098-129">Value</span></span> |
|--------------------|----------------------------------------------------|
| <span data-ttu-id="f3098-130">Versão</span><span class="sxs-lookup"><span data-stu-id="f3098-130">Version</span></span><br/> | <span data-ttu-id="f3098-131">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f3098-131">Windows Media Player 9 Series or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3098-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3098-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3098-133">**Elemento seq**</span><span class="sxs-lookup"><span data-stu-id="f3098-133">**seq Element**</span></span>](seq-element.md)
</dt> <dt>

[<span data-ttu-id="f3098-134">**Referência de elementos da playlist do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f3098-134">**Windows Media Playlist Elements Reference**</span></span>](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





