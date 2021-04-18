---
title: Atributo userrating
description: O atributo userrating é a classificação especificada pelo usuário na biblioteca.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Atributo userrating do Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765628"
---
# <a name="userrating-attribute"></a><span data-ttu-id="c9f79-104">Atributo userrating</span><span class="sxs-lookup"><span data-stu-id="c9f79-104">UserRating Attribute</span></span>

<span data-ttu-id="c9f79-105">O atributo **userrating** é a classificação especificada pelo usuário na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c9f79-105">The **UserRating** attribute is the rating specified by the user in the library.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c9f79-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="c9f79-106">Applies To</span></span>

-   [<span data-ttu-id="c9f79-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="c9f79-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="c9f79-108">Outros itens</span><span class="sxs-lookup"><span data-stu-id="c9f79-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="c9f79-109">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="c9f79-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="c9f79-110">Playlists</span><span class="sxs-lookup"><span data-stu-id="c9f79-110">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="c9f79-111">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="c9f79-111">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="c9f79-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9f79-112">Remarks</span></span>

<span data-ttu-id="c9f79-113">As classificações de usuário são representadas por valores inteiros, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9f79-113">User ratings are represented by integer values, as described in the following table.</span></span> <span data-ttu-id="c9f79-114">Ao especificar um valor, use um dos valores da coluna de valor de gravação.</span><span class="sxs-lookup"><span data-stu-id="c9f79-114">When specifying a value, use one of the values from the Writing value column.</span></span> <span data-ttu-id="c9f79-115">Ao recuperar valores, você pode usar os intervalos na coluna valores de leitura para determinar o número de estrelas.</span><span class="sxs-lookup"><span data-stu-id="c9f79-115">When retrieving values, you can use the ranges in the Reading values column to determine the number of stars.</span></span>



| <span data-ttu-id="c9f79-116">Classificação</span><span class="sxs-lookup"><span data-stu-id="c9f79-116">Rating</span></span>  | <span data-ttu-id="c9f79-117">Valor de gravação</span><span class="sxs-lookup"><span data-stu-id="c9f79-117">Writing value</span></span> | <span data-ttu-id="c9f79-118">Lendo valores</span><span class="sxs-lookup"><span data-stu-id="c9f79-118">Reading values</span></span> |
|---------|---------------|----------------|
| <span data-ttu-id="c9f79-119">Sem classificação</span><span class="sxs-lookup"><span data-stu-id="c9f79-119">Unrated</span></span> | <span data-ttu-id="c9f79-120">0</span><span class="sxs-lookup"><span data-stu-id="c9f79-120">0</span></span>             | <span data-ttu-id="c9f79-121">0</span><span class="sxs-lookup"><span data-stu-id="c9f79-121">0</span></span>              |
| <span data-ttu-id="c9f79-122">1 estrela</span><span class="sxs-lookup"><span data-stu-id="c9f79-122">1 star</span></span>  | <span data-ttu-id="c9f79-123">1</span><span class="sxs-lookup"><span data-stu-id="c9f79-123">1</span></span>             | <span data-ttu-id="c9f79-124">1 a 12</span><span class="sxs-lookup"><span data-stu-id="c9f79-124">1 to 12</span></span>        |
| <span data-ttu-id="c9f79-125">2 estrelas</span><span class="sxs-lookup"><span data-stu-id="c9f79-125">2 stars</span></span> | <span data-ttu-id="c9f79-126">25</span><span class="sxs-lookup"><span data-stu-id="c9f79-126">25</span></span>            | <span data-ttu-id="c9f79-127">13 a 37</span><span class="sxs-lookup"><span data-stu-id="c9f79-127">13 to 37</span></span>       |
| <span data-ttu-id="c9f79-128">3 estrelas</span><span class="sxs-lookup"><span data-stu-id="c9f79-128">3 stars</span></span> | <span data-ttu-id="c9f79-129">50</span><span class="sxs-lookup"><span data-stu-id="c9f79-129">50</span></span>            | <span data-ttu-id="c9f79-130">38 a 62</span><span class="sxs-lookup"><span data-stu-id="c9f79-130">38 to 62</span></span>       |
| <span data-ttu-id="c9f79-131">4 estrelas</span><span class="sxs-lookup"><span data-stu-id="c9f79-131">4 stars</span></span> | <span data-ttu-id="c9f79-132">75</span><span class="sxs-lookup"><span data-stu-id="c9f79-132">75</span></span>            | <span data-ttu-id="c9f79-133">63 a 86</span><span class="sxs-lookup"><span data-stu-id="c9f79-133">63 to 86</span></span>       |
| <span data-ttu-id="c9f79-134">5 estrelas</span><span class="sxs-lookup"><span data-stu-id="c9f79-134">5 stars</span></span> | <span data-ttu-id="c9f79-135">99</span><span class="sxs-lookup"><span data-stu-id="c9f79-135">99</span></span>            | <span data-ttu-id="c9f79-136">87 a 99</span><span class="sxs-lookup"><span data-stu-id="c9f79-136">87 to 99</span></span>       |



 

<span data-ttu-id="c9f79-137">Esse atributo é armazenado somente na biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="c9f79-137">This attribute is stored only in the library.</span></span>

<span data-ttu-id="c9f79-138">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c9f79-138">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9f79-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9f79-139">Requirements</span></span>



| <span data-ttu-id="c9f79-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9f79-140">Requirement</span></span> | <span data-ttu-id="c9f79-141">Valor</span><span class="sxs-lookup"><span data-stu-id="c9f79-141">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f79-142">Versão</span><span class="sxs-lookup"><span data-stu-id="c9f79-142">Version</span></span><br/> | <span data-ttu-id="c9f79-143">Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)</span><span class="sxs-lookup"><span data-stu-id="c9f79-143">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9f79-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9f79-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f79-145">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="c9f79-145">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





