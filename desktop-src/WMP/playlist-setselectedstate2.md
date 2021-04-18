---
title: PLAYLIST. setSelectedState2
description: O método setSelectedState2 define o estado selecionado do item com o índice especificado no elemento PLAYLIST.
ms.assetid: 990b834a-f7ed-45b8-99e1-3efd7f4447f4
keywords:
- PLAYLIST. setSelectedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1a4e317543765fb24755516a0637b16958ad679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771767"
---
# <a name="playlistsetselectedstate2"></a><span data-ttu-id="44320-104">PLAYLIST. setSelectedState2</span><span class="sxs-lookup"><span data-stu-id="44320-104">PLAYLIST.setSelectedState2</span></span>

<span data-ttu-id="44320-105">O método **setSelectedState2** define o estado selecionado do item com o índice especificado no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="44320-105">The **setSelectedState2** method sets the selected state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setSelectedState2(item, selected)
```

## <a name="parameters"></a><span data-ttu-id="44320-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44320-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="44320-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="44320-108">**Número** (**longo**) indicando o índice de um item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="44320-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="44320-109"><span id="selected"></span><span id="SELECTED"></span>*Selecione*</span><span class="sxs-lookup"><span data-stu-id="44320-109"><span id="selected"></span><span id="SELECTED"></span>*selected*</span></span>
</dt> <dd>

<span data-ttu-id="44320-110">**Booliano** que indica se o item especificado deve ser selecionado (true) ou não selecionado (false).</span><span class="sxs-lookup"><span data-stu-id="44320-110">**Boolean** indicating whether the specified item is to be selected (true) or unselected (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44320-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="44320-111">Return Value</span></span>

<span data-ttu-id="44320-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="44320-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44320-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="44320-113">Remarks</span></span>

<span data-ttu-id="44320-114">Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **Setselecionostate** que não pode.</span><span class="sxs-lookup"><span data-stu-id="44320-114">This method can work with nested playlists and replaces the **setSelectedState** method which cannot.</span></span> <span data-ttu-id="44320-115">Você pode definir todos os itens para o estado solicitado especificando 1 no parâmetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="44320-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="44320-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44320-116">Requirements</span></span>



| <span data-ttu-id="44320-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="44320-117">Requirement</span></span> | <span data-ttu-id="44320-118">Valor</span><span class="sxs-lookup"><span data-stu-id="44320-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="44320-119">Versão</span><span class="sxs-lookup"><span data-stu-id="44320-119">Version</span></span><br/> | <span data-ttu-id="44320-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="44320-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44320-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="44320-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44320-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="44320-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="44320-123">**PLAYLIST. setselecionostate**</span><span class="sxs-lookup"><span data-stu-id="44320-123">**PLAYLIST.setSelectedState**</span></span>](playlist-setselectedstate.md)
</dt> </dl>

 

 





