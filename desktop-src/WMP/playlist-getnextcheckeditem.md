---
title: PLAYLIST. getNextCheckedItem
description: O método getNextCheckedItem recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- PLAYLIST. getNextCheckedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784606"
---
# <a name="playlistgetnextcheckeditem"></a><span data-ttu-id="c6fb0-104">PLAYLIST. getNextCheckedItem</span><span class="sxs-lookup"><span data-stu-id="c6fb0-104">PLAYLIST.getNextCheckedItem</span></span>

<span data-ttu-id="c6fb0-105">O método **getNextCheckedItem** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c6fb0-105">The **getNextCheckedItem** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="c6fb0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6fb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6fb0-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="c6fb0-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="c6fb0-108">**Número** (**longo**) indicando o índice do item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="c6fb0-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6fb0-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c6fb0-109">Return Value</span></span>

<span data-ttu-id="c6fb0-110">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="c6fb0-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6fb0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6fb0-111">Remarks</span></span>

<span data-ttu-id="c6fb0-112">Quando não há itens marcados adicionais, esse método retorna 1.</span><span class="sxs-lookup"><span data-stu-id="c6fb0-112">When there are no further checked items, this method returns  1.</span></span>

<span data-ttu-id="c6fb0-113">Esse método foi substituído por **getNextCheckedItem2**, que dá suporte a listas de reprodução aninhadas.</span><span class="sxs-lookup"><span data-stu-id="c6fb0-113">This method has been replaced by **getNextCheckedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6fb0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6fb0-114">Requirements</span></span>



| <span data-ttu-id="c6fb0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6fb0-115">Requirement</span></span> | <span data-ttu-id="c6fb0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c6fb0-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c6fb0-117">Versão</span><span class="sxs-lookup"><span data-stu-id="c6fb0-117">Version</span></span><br/> | <span data-ttu-id="c6fb0-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c6fb0-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6fb0-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6fb0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fb0-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="c6fb0-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="c6fb0-121">**PLAYLIST. getNextCheckedItem2**</span><span class="sxs-lookup"><span data-stu-id="c6fb0-121">**PLAYLIST.getNextCheckedItem2**</span></span>](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





