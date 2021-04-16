---
title: Atributo UserServiceRating
description: O atributo UserServiceRating é reservado para uso futuro.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Atributo UserServiceRating Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772967"
---
# <a name="userservicerating-attribute"></a><span data-ttu-id="08ded-104">Atributo UserServiceRating</span><span class="sxs-lookup"><span data-stu-id="08ded-104">UserServiceRating Attribute</span></span>

<span data-ttu-id="08ded-105">O atributo **UserServiceRating** é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="08ded-105">The **UserServiceRating** attribute is reserved for future use.</span></span>

## <a name="applies-to"></a><span data-ttu-id="08ded-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="08ded-106">Applies To</span></span>

-   [<span data-ttu-id="08ded-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="08ded-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="08ded-108">Playlists</span><span class="sxs-lookup"><span data-stu-id="08ded-108">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="08ded-109">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="08ded-109">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="08ded-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="08ded-110">Remarks</span></span>

<span data-ttu-id="08ded-111">As classificações de usuário são representadas por valores inteiros, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="08ded-111">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="08ded-112">Ao especificar um valor, use um dos valores da coluna de valor de gravação.</span><span class="sxs-lookup"><span data-stu-id="08ded-112">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="08ded-113">Ao recuperar valores, você pode usar os intervalos na coluna valores de leitura para determinar o número de estrelas.</span><span class="sxs-lookup"><span data-stu-id="08ded-113">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="08ded-114">Classificação</span><span class="sxs-lookup"><span data-stu-id="08ded-114">Rating</span></span>  | <span data-ttu-id="08ded-115">Valor de gravação</span><span class="sxs-lookup"><span data-stu-id="08ded-115">Writing value</span></span> | <span data-ttu-id="08ded-116">Lendo valores</span><span class="sxs-lookup"><span data-stu-id="08ded-116">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="08ded-117">Sem classificação</span><span class="sxs-lookup"><span data-stu-id="08ded-117">Unrated</span></span> | <span data-ttu-id="08ded-118">0</span><span class="sxs-lookup"><span data-stu-id="08ded-118">0</span></span>             | <span data-ttu-id="08ded-119">0</span><span class="sxs-lookup"><span data-stu-id="08ded-119">0</span></span>              |
| <span data-ttu-id="08ded-120">1 estrela</span><span class="sxs-lookup"><span data-stu-id="08ded-120">1 star</span></span>  | <span data-ttu-id="08ded-121">1</span><span class="sxs-lookup"><span data-stu-id="08ded-121">1</span></span>             | <span data-ttu-id="08ded-122">1 a 12</span><span class="sxs-lookup"><span data-stu-id="08ded-122">1 to 12</span></span>        |
| <span data-ttu-id="08ded-123">2 estrelas</span><span class="sxs-lookup"><span data-stu-id="08ded-123">2 stars</span></span> | <span data-ttu-id="08ded-124">25</span><span class="sxs-lookup"><span data-stu-id="08ded-124">25</span></span>            | <span data-ttu-id="08ded-125">13 a 37</span><span class="sxs-lookup"><span data-stu-id="08ded-125">13 to 37</span></span>       |
| <span data-ttu-id="08ded-126">3 estrelas</span><span class="sxs-lookup"><span data-stu-id="08ded-126">3 stars</span></span> | <span data-ttu-id="08ded-127">50</span><span class="sxs-lookup"><span data-stu-id="08ded-127">50</span></span>            | <span data-ttu-id="08ded-128">38 a 62</span><span class="sxs-lookup"><span data-stu-id="08ded-128">38 to 62</span></span>       |
| <span data-ttu-id="08ded-129">4 estrelas</span><span class="sxs-lookup"><span data-stu-id="08ded-129">4 stars</span></span> | <span data-ttu-id="08ded-130">75</span><span class="sxs-lookup"><span data-stu-id="08ded-130">75</span></span>            | <span data-ttu-id="08ded-131">63 a 86</span><span class="sxs-lookup"><span data-stu-id="08ded-131">63 to 86</span></span>       |
| <span data-ttu-id="08ded-132">5 estrelas</span><span class="sxs-lookup"><span data-stu-id="08ded-132">5 stars</span></span> | <span data-ttu-id="08ded-133">99</span><span class="sxs-lookup"><span data-stu-id="08ded-133">99</span></span>            | <span data-ttu-id="08ded-134">87 a 99</span><span class="sxs-lookup"><span data-stu-id="08ded-134">87 to 99</span></span>       |



 

<span data-ttu-id="08ded-135">Esse atributo é armazenado somente na biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="08ded-135">This attribute is stored only in the library.</span></span>

<span data-ttu-id="08ded-136">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="08ded-136">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ded-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08ded-137">Requirements</span></span>



| <span data-ttu-id="08ded-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="08ded-138">Requirement</span></span> | <span data-ttu-id="08ded-139">Valor</span><span class="sxs-lookup"><span data-stu-id="08ded-139">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="08ded-140">Versão</span><span class="sxs-lookup"><span data-stu-id="08ded-140">Version</span></span><br/> | <span data-ttu-id="08ded-141">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="08ded-141">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="08ded-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="08ded-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ded-143">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="08ded-143">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





