---
title: PLAYLIST. setCheckedState2
description: O método setCheckedState2 define o estado de ativação do item com o índice especificado no elemento PLAYLIST.
ms.assetid: 241221a3-810b-422d-8f73-25c5b5c82c70
keywords:
- PLAYLIST. setCheckedState2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37cc9c821ae783e79d327e93b0c2f297fb75eab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762374"
---
# <a name="playlistsetcheckedstate2"></a><span data-ttu-id="10c2e-104">PLAYLIST. setCheckedState2</span><span class="sxs-lookup"><span data-stu-id="10c2e-104">PLAYLIST.setCheckedState2</span></span>

<span data-ttu-id="10c2e-105">O método **setCheckedState2** define o estado de ativação do item com o índice especificado no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="10c2e-105">The **setCheckedState2** method sets the checked state of the item with the specified index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.setCheckedState(item, checked)
```

## <a name="parameters"></a><span data-ttu-id="10c2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10c2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c2e-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="10c2e-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="10c2e-108">**Número** (**longo**) que indica o índice do item da playlist a ser marcado ou desmarcado.</span><span class="sxs-lookup"><span data-stu-id="10c2e-108">**Number** (**long**) indicating the index of the playlist item to be checked or unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="10c2e-109"><span id="checked"></span><span id="CHECKED"></span>*check*</span><span class="sxs-lookup"><span data-stu-id="10c2e-109"><span id="checked"></span><span id="CHECKED"></span>*checked*</span></span>
</dt> <dd>

<span data-ttu-id="10c2e-110">**Booliano** que indica se o item especificado deve ser marcado (true) ou desmarcado (false).</span><span class="sxs-lookup"><span data-stu-id="10c2e-110">**Boolean** indicating whether the specified item is to be checked (true) or unchecked (false).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c2e-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="10c2e-111">Return Value</span></span>

<span data-ttu-id="10c2e-112">Esse método retorna um **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="10c2e-112">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="10c2e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="10c2e-113">Remarks</span></span>

<span data-ttu-id="10c2e-114">Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **Setcheckstate** , que não pode.</span><span class="sxs-lookup"><span data-stu-id="10c2e-114">This method can work with nested playlists and replaces the **setCheckedState** method, which cannot.</span></span> <span data-ttu-id="10c2e-115">Você pode definir todos os itens para o estado solicitado especificando 1 no parâmetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="10c2e-115">You can set all items to the requested state by specifying  1 in the *item* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c2e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10c2e-116">Requirements</span></span>



| <span data-ttu-id="10c2e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="10c2e-117">Requirement</span></span> | <span data-ttu-id="10c2e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="10c2e-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="10c2e-119">Versão</span><span class="sxs-lookup"><span data-stu-id="10c2e-119">Version</span></span><br/> | <span data-ttu-id="10c2e-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="10c2e-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10c2e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="10c2e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c2e-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="10c2e-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="10c2e-123">**PLAYLIST. setcheckstate**</span><span class="sxs-lookup"><span data-stu-id="10c2e-123">**PLAYLIST.setCheckedState**</span></span>](playlist-setcheckedstate.md)
</dt> </dl>

 

 





