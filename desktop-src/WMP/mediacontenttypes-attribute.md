---
title: Atributo MediaContentTypes
description: O atributo MediaContentTypes especifica o tipo de conteúdo no item.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Atributo MediaContentTypes Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748545"
---
# <a name="mediacontenttypes-attribute"></a><span data-ttu-id="d5db5-104">Atributo MediaContentTypes</span><span class="sxs-lookup"><span data-stu-id="d5db5-104">MediaContentTypes Attribute</span></span>

<span data-ttu-id="d5db5-105">O atributo **MediaContentTypes** especifica o tipo de conteúdo no item.</span><span class="sxs-lookup"><span data-stu-id="d5db5-105">The **MediaContentTypes** attribute specifies the type of content in the item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d5db5-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="d5db5-106">Applies To</span></span>

-   [<span data-ttu-id="d5db5-107">Playlists</span><span class="sxs-lookup"><span data-stu-id="d5db5-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="d5db5-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5db5-108">Remarks</span></span>

<span data-ttu-id="d5db5-109">Esse atributo pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="d5db5-109">This attribute can be one of the following values:</span></span>



| <span data-ttu-id="d5db5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d5db5-110">Value</span></span> | <span data-ttu-id="d5db5-111">Significado</span><span class="sxs-lookup"><span data-stu-id="d5db5-111">Meaning</span></span>                                |
|-------|----------------------------------------|
| <span data-ttu-id="d5db5-112">1</span><span class="sxs-lookup"><span data-stu-id="d5db5-112">1</span></span>     | <span data-ttu-id="d5db5-113">A lista de reprodução contém o conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="d5db5-113">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="d5db5-114">2</span><span class="sxs-lookup"><span data-stu-id="d5db5-114">2</span></span>     | <span data-ttu-id="d5db5-115">A ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="d5db5-115">To be supplied.</span></span>                        |
| <span data-ttu-id="d5db5-116">3</span><span class="sxs-lookup"><span data-stu-id="d5db5-116">3</span></span>     | <span data-ttu-id="d5db5-117">A lista de reprodução contém o conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="d5db5-117">The playlist contains audio content.</span></span>   |
| <span data-ttu-id="d5db5-118">4</span><span class="sxs-lookup"><span data-stu-id="d5db5-118">4</span></span>     | <span data-ttu-id="d5db5-119">A lista de reprodução contém conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d5db5-119">The playlist contains video content.</span></span>   |
| <span data-ttu-id="d5db5-120">5</span><span class="sxs-lookup"><span data-stu-id="d5db5-120">5</span></span>     | <span data-ttu-id="d5db5-121">A lista de reprodução contém conteúdo de imagem.</span><span class="sxs-lookup"><span data-stu-id="d5db5-121">The playlist contains picture content.</span></span> |
| <span data-ttu-id="d5db5-122">6</span><span class="sxs-lookup"><span data-stu-id="d5db5-122">6</span></span>     | <span data-ttu-id="d5db5-123">A lista de reprodução contém conteúdo de TV.</span><span class="sxs-lookup"><span data-stu-id="d5db5-123">The playlist contains TV content.</span></span>      |



 

<span data-ttu-id="d5db5-124">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d5db5-124">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5db5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5db5-125">Requirements</span></span>



| <span data-ttu-id="d5db5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5db5-126">Requirement</span></span> | <span data-ttu-id="d5db5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="d5db5-127">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="d5db5-128">Versão</span><span class="sxs-lookup"><span data-stu-id="d5db5-128">Version</span></span><br/> | <span data-ttu-id="d5db5-129">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="d5db5-129">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5db5-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5db5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5db5-131">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="d5db5-131">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





