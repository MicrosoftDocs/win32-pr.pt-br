---
title: PLAYLIST. setcheckstate
description: O método setcheckstate especifica que o item indexado na playlist está marcado.
ms.assetid: ce5de21b-6354-485e-b6f7-f4d090c149f7
keywords:
- PLAYLIST. setcheckstate do Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setCheckedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a8c86459dcf590b1ff1e884a8aa671dc1bba78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773047"
---
# <a name="playlistsetcheckedstate"></a><span data-ttu-id="2074d-104">PLAYLIST. setcheckstate</span><span class="sxs-lookup"><span data-stu-id="2074d-104">PLAYLIST.setCheckedState</span></span>

<span data-ttu-id="2074d-105">O método **Setcheckstate** especifica que o item indexado na playlist está marcado.</span><span class="sxs-lookup"><span data-stu-id="2074d-105">The **setCheckedState** method specifies that the indexed item in the playlist is checked.</span></span>

``` syntax
        elementID.setCheckedState(item)
```

## <a name="parameters"></a><span data-ttu-id="2074d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2074d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2074d-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="2074d-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="2074d-108">**Número** (**longo**) indicando o índice do item da playlist a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="2074d-108">**Number** (**long**) indicating the index of the playlist item to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2074d-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2074d-109">Return Value</span></span>

<span data-ttu-id="2074d-110">Esse método retorna um **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="2074d-110">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2074d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2074d-111">Remarks</span></span>

<span data-ttu-id="2074d-112">Você pode definir todos os itens para o estado Checked especificando 1 no parâmetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="2074d-112">You can set all items to the checked state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="2074d-113">Esse método foi substituído por **setCheckedState2**, que dá suporte a listas de reprodução aninhadas.</span><span class="sxs-lookup"><span data-stu-id="2074d-113">This method has been replaced by **setCheckedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="2074d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2074d-114">Requirements</span></span>



| <span data-ttu-id="2074d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2074d-115">Requirement</span></span> | <span data-ttu-id="2074d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2074d-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2074d-117">Versão</span><span class="sxs-lookup"><span data-stu-id="2074d-117">Version</span></span><br/> | <span data-ttu-id="2074d-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="2074d-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2074d-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2074d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2074d-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="2074d-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="2074d-121">**PLAYLIST. setCheckedState2**</span><span class="sxs-lookup"><span data-stu-id="2074d-121">**PLAYLIST.setCheckedState2**</span></span>](playlist-setcheckedstate2.md)
</dt> </dl>

 

 





