---
title: Atributo UserEffectiveRating
description: O atributo UserEffectiveRating é a classificação calculada pelo Windows Media Player com base na frequência com que o item foi reproduzido.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Atributo UserEffectiveRating Windows Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94abda9f8237c169845683263081566957a10b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812012"
---
# <a name="usereffectiverating-attribute"></a><span data-ttu-id="1dda9-104">Atributo UserEffectiveRating</span><span class="sxs-lookup"><span data-stu-id="1dda9-104">UserEffectiveRating Attribute</span></span>

<span data-ttu-id="1dda9-105">O atributo **UserEffectiveRating** é a classificação calculada pelo Windows Media Player com base na frequência com que o item foi reproduzido.</span><span class="sxs-lookup"><span data-stu-id="1dda9-105">The **UserEffectiveRating** attribute is the rating computed by Windows Media Player based on how often the item has been played.</span></span>

## <a name="applies-to"></a><span data-ttu-id="1dda9-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="1dda9-106">Applies To</span></span>

-   [<span data-ttu-id="1dda9-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="1dda9-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="1dda9-108">Outros itens</span><span class="sxs-lookup"><span data-stu-id="1dda9-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="1dda9-109">Playlists</span><span class="sxs-lookup"><span data-stu-id="1dda9-109">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="1dda9-110">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="1dda9-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="1dda9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dda9-111">Remarks</span></span>

<span data-ttu-id="1dda9-112">As classificações de usuário são representadas por valores inteiros, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1dda9-112">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="1dda9-113">Ao especificar um valor, use um dos valores da coluna de valor de gravação.</span><span class="sxs-lookup"><span data-stu-id="1dda9-113">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="1dda9-114">Ao recuperar valores, você pode usar os intervalos na coluna valores de leitura para determinar o número de estrelas.</span><span class="sxs-lookup"><span data-stu-id="1dda9-114">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="1dda9-115">Classificação</span><span class="sxs-lookup"><span data-stu-id="1dda9-115">Rating</span></span>  | <span data-ttu-id="1dda9-116">Valor de gravação</span><span class="sxs-lookup"><span data-stu-id="1dda9-116">Writing value</span></span> | <span data-ttu-id="1dda9-117">Lendo valores</span><span class="sxs-lookup"><span data-stu-id="1dda9-117">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="1dda9-118">Sem classificação</span><span class="sxs-lookup"><span data-stu-id="1dda9-118">Unrated</span></span> | <span data-ttu-id="1dda9-119">0</span><span class="sxs-lookup"><span data-stu-id="1dda9-119">0</span></span>             | <span data-ttu-id="1dda9-120">0</span><span class="sxs-lookup"><span data-stu-id="1dda9-120">0</span></span>              |
| <span data-ttu-id="1dda9-121">1 estrela</span><span class="sxs-lookup"><span data-stu-id="1dda9-121">1 star</span></span>  | <span data-ttu-id="1dda9-122">1</span><span class="sxs-lookup"><span data-stu-id="1dda9-122">1</span></span>             | <span data-ttu-id="1dda9-123">1 a 12</span><span class="sxs-lookup"><span data-stu-id="1dda9-123">1 to 12</span></span>        |
| <span data-ttu-id="1dda9-124">2 estrelas</span><span class="sxs-lookup"><span data-stu-id="1dda9-124">2 stars</span></span> | <span data-ttu-id="1dda9-125">25</span><span class="sxs-lookup"><span data-stu-id="1dda9-125">25</span></span>            | <span data-ttu-id="1dda9-126">13 a 37</span><span class="sxs-lookup"><span data-stu-id="1dda9-126">13 to 37</span></span>       |
| <span data-ttu-id="1dda9-127">3 estrelas</span><span class="sxs-lookup"><span data-stu-id="1dda9-127">3 stars</span></span> | <span data-ttu-id="1dda9-128">50</span><span class="sxs-lookup"><span data-stu-id="1dda9-128">50</span></span>            | <span data-ttu-id="1dda9-129">38 a 62</span><span class="sxs-lookup"><span data-stu-id="1dda9-129">38 to 62</span></span>       |
| <span data-ttu-id="1dda9-130">4 estrelas</span><span class="sxs-lookup"><span data-stu-id="1dda9-130">4 stars</span></span> | <span data-ttu-id="1dda9-131">75</span><span class="sxs-lookup"><span data-stu-id="1dda9-131">75</span></span>            | <span data-ttu-id="1dda9-132">63 a 86</span><span class="sxs-lookup"><span data-stu-id="1dda9-132">63 to 86</span></span>       |
| <span data-ttu-id="1dda9-133">5 estrelas</span><span class="sxs-lookup"><span data-stu-id="1dda9-133">5 stars</span></span> | <span data-ttu-id="1dda9-134">99</span><span class="sxs-lookup"><span data-stu-id="1dda9-134">99</span></span>            | <span data-ttu-id="1dda9-135">87 a 99</span><span class="sxs-lookup"><span data-stu-id="1dda9-135">87 to 99</span></span>       |



 

<span data-ttu-id="1dda9-136">Esse atributo é armazenado somente na biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="1dda9-136">This attribute is stored only in the library.</span></span>

<span data-ttu-id="1dda9-137">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="1dda9-137">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dda9-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dda9-138">Requirements</span></span>



| <span data-ttu-id="1dda9-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dda9-139">Requirement</span></span> | <span data-ttu-id="1dda9-140">Valor</span><span class="sxs-lookup"><span data-stu-id="1dda9-140">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1dda9-141">Versão</span><span class="sxs-lookup"><span data-stu-id="1dda9-141">Version</span></span><br/> | <span data-ttu-id="1dda9-142">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="1dda9-142">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1dda9-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dda9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dda9-144">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="1dda9-144">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





