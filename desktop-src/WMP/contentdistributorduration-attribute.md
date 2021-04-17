---
title: Atributo ContentDistributorDuration
description: O atributo ContentDistributorDuration é a duração da reprodução do item, em segundos.
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- Atributo ContentDistributorDuration Windows Media Player
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f17bad8ef5dd1ab4b0a3d1c7b5becec6fd34a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783620"
---
# <a name="contentdistributorduration-attribute"></a><span data-ttu-id="5f860-104">Atributo ContentDistributorDuration</span><span class="sxs-lookup"><span data-stu-id="5f860-104">ContentDistributorDuration Attribute</span></span>

<span data-ttu-id="5f860-105">O atributo **ContentDistributorDuration** é a duração da reprodução do item, em segundos.</span><span class="sxs-lookup"><span data-stu-id="5f860-105">The **ContentDistributorDuration** attribute is the playing duration of the item, in seconds.</span></span>

## <a name="applies-to"></a><span data-ttu-id="5f860-106">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="5f860-106">Applies To</span></span>

-   [<span data-ttu-id="5f860-107">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="5f860-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="5f860-108">Outros itens</span><span class="sxs-lookup"><span data-stu-id="5f860-108">Other Items</span></span>](other-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="5f860-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f860-109">Remarks</span></span>

<span data-ttu-id="5f860-110">Se o atributo **Duration** regular não for definido (NULL) ou 0, o valor desse atributo será retornado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5f860-110">If the regular **Duration** attribute is either not set (Null) or 0, then the value of this attribute will be returned instead.</span></span>

<span data-ttu-id="5f860-111">Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="5f860-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f860-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f860-112">Requirements</span></span>



| <span data-ttu-id="5f860-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f860-113">Requirement</span></span> | <span data-ttu-id="5f860-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5f860-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="5f860-115">Versão</span><span class="sxs-lookup"><span data-stu-id="5f860-115">Version</span></span><br/> | <span data-ttu-id="5f860-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="5f860-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f860-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f860-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f860-118">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="5f860-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="5f860-119">**Atributo Duration**</span><span class="sxs-lookup"><span data-stu-id="5f860-119">**Duration Attribute**</span></span>](duration-attribute.md)
</dt> </dl>

 

 





