---
title: PLAYLIST. itemCount
description: O atributo itemCount recupera o número de itens atualmente exibidos no elemento PLAYLIST.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- PLAYLIST. itemCount Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811207"
---
# <a name="playlistitemcount"></a><span data-ttu-id="24f5d-104">PLAYLIST. itemCount</span><span class="sxs-lookup"><span data-stu-id="24f5d-104">PLAYLIST.itemCount</span></span>

<span data-ttu-id="24f5d-105">O atributo **ItemCount** recupera o número de itens atualmente exibidos no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="24f5d-105">The **itemCount** attribute retrieves the number of items currently displayed in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a><span data-ttu-id="24f5d-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="24f5d-106">Possible Values</span></span>

<span data-ttu-id="24f5d-107">Esse atributo é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="24f5d-107">This attribute is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="24f5d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="24f5d-108">Remarks</span></span>

<span data-ttu-id="24f5d-109">A propriedade **ItemCount** contará o número total de itens expandidos.</span><span class="sxs-lookup"><span data-stu-id="24f5d-109">The **itemCount** property will count the total number of expanded items.</span></span> <span data-ttu-id="24f5d-110">Por exemplo, se houver duas listas de reprodução que contenham três itens de mídia cada, **ItemCount** retornará 2 se as listas de reprodução não forem expandidas.</span><span class="sxs-lookup"><span data-stu-id="24f5d-110">For example, if there are two playlists that contain three media items each, **itemCount** will return 2 if the playlists are not expanded.</span></span> <span data-ttu-id="24f5d-111">Se apenas a primeira playlist for expandida, **ItemCount** retornará 4.</span><span class="sxs-lookup"><span data-stu-id="24f5d-111">If only the first playlist is expanded, **itemCount** will return 4.</span></span> <span data-ttu-id="24f5d-112">Se ambas as listas de reprodução forem expandidas, **ItemCount** retornará 6.</span><span class="sxs-lookup"><span data-stu-id="24f5d-112">If both playlists are expanded, **itemCount** will return 6.</span></span>

## <a name="requirements"></a><span data-ttu-id="24f5d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24f5d-113">Requirements</span></span>



| <span data-ttu-id="24f5d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="24f5d-114">Requirement</span></span> | <span data-ttu-id="24f5d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="24f5d-115">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="24f5d-116">Versão</span><span class="sxs-lookup"><span data-stu-id="24f5d-116">Version</span></span><br/> | <span data-ttu-id="24f5d-117">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="24f5d-117">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24f5d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="24f5d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24f5d-119">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="24f5d-119">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





