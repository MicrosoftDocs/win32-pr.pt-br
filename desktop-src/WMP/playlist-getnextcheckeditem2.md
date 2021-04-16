---
title: PLAYLIST. getNextCheckedItem2
description: O método getNextCheckedItem2 recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- PLAYLIST. getNextCheckedItem2 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765233"
---
# <a name="playlistgetnextcheckeditem2"></a><span data-ttu-id="2c073-104">PLAYLIST. getNextCheckedItem2</span><span class="sxs-lookup"><span data-stu-id="2c073-104">PLAYLIST.getNextCheckedItem2</span></span>

<span data-ttu-id="2c073-105">O método **getNextCheckedItem2** recupera o índice do próximo item selecionado na lista de reprodução após o índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2c073-105">The **getNextCheckedItem2** method retrieves the index of the next checked item in the playlist following the specified index.</span></span>

``` syntax
        elementID.getNextCheckedItem2(item)
```

## <a name="parameters"></a><span data-ttu-id="2c073-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c073-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c073-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="2c073-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="2c073-108">**Número** (**longo**) indicando o índice do item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="2c073-108">**Number** (**long**) indicating the index of the item to search after.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c073-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2c073-109">Return Value</span></span>

<span data-ttu-id="2c073-110">Esse método retorna um **número** (**longo**).</span><span class="sxs-lookup"><span data-stu-id="2c073-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c073-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c073-111">Remarks</span></span>

<span data-ttu-id="2c073-112">Esse método pode trabalhar com listas de reprodução aninhadas e substituir o método **getNextCheckedItem** , que não pode.</span><span class="sxs-lookup"><span data-stu-id="2c073-112">This method can work with nested playlists and replaces the **getNextCheckedItem** method, which cannot.</span></span> <span data-ttu-id="2c073-113">Passe 1 no parâmetro *Item* para localizar o primeiro item selecionado.</span><span class="sxs-lookup"><span data-stu-id="2c073-113">Pass  1 in the *item* parameter to find the first checked item.</span></span> <span data-ttu-id="2c073-114">Quando não há itens marcados adicionais, esse método retorna 1.</span><span class="sxs-lookup"><span data-stu-id="2c073-114">When there are no further checked items, this method returns  1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c073-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c073-115">Requirements</span></span>



| <span data-ttu-id="2c073-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c073-116">Requirement</span></span> | <span data-ttu-id="2c073-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2c073-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="2c073-118">Versão</span><span class="sxs-lookup"><span data-stu-id="2c073-118">Version</span></span><br/> | <span data-ttu-id="2c073-119">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="2c073-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c073-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c073-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c073-121">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="2c073-121">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="2c073-122">**PLAYLIST. getNextCheckedItem**</span><span class="sxs-lookup"><span data-stu-id="2c073-122">**PLAYLIST.getNextCheckedItem**</span></span>](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





