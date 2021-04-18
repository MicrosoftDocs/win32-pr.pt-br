---
title: PLAYLIST. getNextSelectedItem2
description: O método getNextSelectedItem2 recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- PLAYLIST. getNextSelectedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764525"
---
# <a name="playlistgetnextselecteditem2"></a><span data-ttu-id="7d95b-104">PLAYLIST. getNextSelectedItem2</span><span class="sxs-lookup"><span data-stu-id="7d95b-104">PLAYLIST.getNextSelectedItem2</span></span>

<span data-ttu-id="7d95b-105">O método **getNextSelectedItem2** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7d95b-105">The **getNextSelectedItem2** method retrieves the index of the next selected item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="7d95b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d95b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d95b-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="7d95b-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="7d95b-108">**Número** (**longo**) indicando o índice do item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="7d95b-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d95b-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7d95b-109">Return Value</span></span>

<span data-ttu-id="7d95b-110">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="7d95b-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d95b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d95b-111">Remarks</span></span>

<span data-ttu-id="7d95b-112">Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **getNextSelectedItem** , que não pode.</span><span class="sxs-lookup"><span data-stu-id="7d95b-112">This method can work with nested playlists and replaces the **getNextSelectedItem** method, which cannot.</span></span> <span data-ttu-id="7d95b-113">Passe 1 no parâmetro *Item* para localizar o primeiro item selecionado.</span><span class="sxs-lookup"><span data-stu-id="7d95b-113">Pass  1 in the *item* parameter to find the first selected item.</span></span> <span data-ttu-id="7d95b-114">Quando não há mais itens selecionados,-1 é retornado.</span><span class="sxs-lookup"><span data-stu-id="7d95b-114">When there are no further selected items, -1 is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d95b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d95b-115">Requirements</span></span>



| <span data-ttu-id="7d95b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d95b-116">Requirement</span></span> | <span data-ttu-id="7d95b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7d95b-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7d95b-118">Versão</span><span class="sxs-lookup"><span data-stu-id="7d95b-118">Version</span></span><br/> | <span data-ttu-id="7d95b-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="7d95b-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d95b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d95b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d95b-121">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="7d95b-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="7d95b-122">**PLAYLIST. getNextSelectedItem**</span><span class="sxs-lookup"><span data-stu-id="7d95b-122">**PLAYLIST.getNextSelectedItem**</span></span>](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





