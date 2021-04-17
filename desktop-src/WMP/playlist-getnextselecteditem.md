---
title: PLAYLIST. getNextSelectedItem
description: O método getNextSelectedItem recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: d46d3a65-8863-4a2f-9add-0701c8283a6b
keywords:
- PLAYLIST. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c5e37ad5109066a11cf28a593ed69f8c86b8b639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798388"
---
# <a name="playlistgetnextselecteditem"></a><span data-ttu-id="5cb14-104">PLAYLIST. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="5cb14-104">PLAYLIST.getNextSelectedItem</span></span>

<span data-ttu-id="5cb14-105">O método **getNextSelectedItem** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5cb14-105">The **getNextSelectedItem** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(item)
```

## <a name="parameters"></a><span data-ttu-id="5cb14-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cb14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cb14-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="5cb14-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="5cb14-108">**Número** (**longo**) indicando o índice do item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="5cb14-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cb14-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5cb14-109">Return Value</span></span>

<span data-ttu-id="5cb14-110">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="5cb14-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5cb14-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cb14-111">Remarks</span></span>

<span data-ttu-id="5cb14-112">Quando não há nenhum outro item selecionado, esse método retorna 1.</span><span class="sxs-lookup"><span data-stu-id="5cb14-112">When there are no further selected items, this method returns  1.</span></span>

<span data-ttu-id="5cb14-113">Esse método foi substituído por **getNextSelectedItem2**, que dá suporte a listas de reprodução aninhadas.</span><span class="sxs-lookup"><span data-stu-id="5cb14-113">This method has been replaced by **getNextSelectedItem2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cb14-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cb14-114">Requirements</span></span>



| <span data-ttu-id="5cb14-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb14-115">Requirement</span></span> | <span data-ttu-id="5cb14-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5cb14-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5cb14-117">Versão</span><span class="sxs-lookup"><span data-stu-id="5cb14-117">Version</span></span><br/> | <span data-ttu-id="5cb14-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5cb14-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cb14-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5cb14-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb14-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="5cb14-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="5cb14-121">**PLAYLIST. getNextSelectedItem2**</span><span class="sxs-lookup"><span data-stu-id="5cb14-121">**PLAYLIST.getNextSelectedItem2**</span></span>](playlist-getnextselecteditem2.md)
</dt> </dl>

 

 





