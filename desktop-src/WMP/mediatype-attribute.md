---
title: Atributo MediaType
description: O atributo MediaType é o tipo de conteúdo no item.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Atributo de MediaType Windows Media Player
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748544"
---
# <a name="mediatype-attribute"></a><span data-ttu-id="52c00-104">Atributo MediaType</span><span class="sxs-lookup"><span data-stu-id="52c00-104">MediaType Attribute</span></span>

<span data-ttu-id="52c00-105">O atributo **MediaType** é o tipo de conteúdo no item.</span><span class="sxs-lookup"><span data-stu-id="52c00-105">The **MediaType** attribute is the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="52c00-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="52c00-106">Applies To</span></span>

-   [<span data-ttu-id="52c00-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="52c00-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="52c00-108">Outros itens</span><span class="sxs-lookup"><span data-stu-id="52c00-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="52c00-109">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="52c00-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="52c00-110">Playlists</span><span class="sxs-lookup"><span data-stu-id="52c00-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="52c00-111">Itens de rádio</span><span class="sxs-lookup"><span data-stu-id="52c00-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="52c00-112">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="52c00-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="52c00-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="52c00-113">Remarks</span></span>

<span data-ttu-id="52c00-114">Esse atributo é armazenado somente na biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="52c00-114">This attribute is stored only in the library.</span></span>

<span data-ttu-id="52c00-115">Esse atributo tem um dos seguintes valores: "áudio", "outro", "foto", "playlist", "rádio" ou "vídeo".</span><span class="sxs-lookup"><span data-stu-id="52c00-115">This attribute has one of the following values: "audio", "other", "photo", "playlist", "radio", or "video".</span></span> <span data-ttu-id="52c00-116">Use esse atributo com *mediacollection*. método **getByAttribute** para recuperar uma lista de reprodução que contém todos os itens de um tipo específico.</span><span class="sxs-lookup"><span data-stu-id="52c00-116">Use this attribute with the *MediaCollection*.**getByAttribute** method to retrieve a playlist containing all of the items of a particular type.</span></span>

<span data-ttu-id="52c00-117">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="52c00-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="52c00-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52c00-118">Requirements</span></span>



| <span data-ttu-id="52c00-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c00-119">Requirement</span></span> | <span data-ttu-id="52c00-120">Valor</span><span class="sxs-lookup"><span data-stu-id="52c00-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="52c00-121">Versão</span><span class="sxs-lookup"><span data-stu-id="52c00-121">Version</span></span><br/> | <span data-ttu-id="52c00-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="52c00-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52c00-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="52c00-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c00-124">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="52c00-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="52c00-125">**Mediacollection. getByAttribute**</span><span class="sxs-lookup"><span data-stu-id="52c00-125">**MediaCollection.getByAttribute**</span></span>](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





