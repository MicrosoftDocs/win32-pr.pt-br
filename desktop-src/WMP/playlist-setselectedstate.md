---
title: PLAYLIST. setselecionostate
description: O método setselecionostate especifica que o item indexado na lista de reprodução está selecionado.
ms.assetid: 61770053-733f-40b5-8b1f-92b6975d3ad3
keywords:
- PLAYLIST. setselecionou Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setSelectedState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09a7bb545330710ae4fe2c39eae4556207061203
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791476"
---
# <a name="playlistsetselectedstate"></a><span data-ttu-id="d1a6a-104">PLAYLIST. setselecionostate</span><span class="sxs-lookup"><span data-stu-id="d1a6a-104">PLAYLIST.setSelectedState</span></span>

<span data-ttu-id="d1a6a-105">O método **Setselecionostate** especifica que o item indexado na lista de reprodução está selecionado.</span><span class="sxs-lookup"><span data-stu-id="d1a6a-105">The **setSelectedState** method specifies that the indexed item in the playlist is selected.</span></span>

``` syntax
        elementID.setSelectedState(item)
```

## <a name="parameters"></a><span data-ttu-id="d1a6a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1a6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a6a-107"><span id="item"></span><span id="ITEM"></span>*item*</span><span class="sxs-lookup"><span data-stu-id="d1a6a-107"><span id="item"></span><span id="ITEM"></span>*item*</span></span>
</dt> <dd>

<span data-ttu-id="d1a6a-108">**Número** (**longo**) indicando o índice de um item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="d1a6a-108">**Number** (**long**) indicating the index of an item in the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a6a-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d1a6a-109">Return Value</span></span>

<span data-ttu-id="d1a6a-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d1a6a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1a6a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1a6a-111">Remarks</span></span>

<span data-ttu-id="d1a6a-112">Você pode definir todos os itens para o estado selecionado especificando 1 no parâmetro *Item* .</span><span class="sxs-lookup"><span data-stu-id="d1a6a-112">You can set all items to the selected state by specifying  1 in the *item* parameter.</span></span>

<span data-ttu-id="d1a6a-113">Esse método foi substituído por **setSelectedState2**, que dá suporte a listas de reprodução aninhadas.</span><span class="sxs-lookup"><span data-stu-id="d1a6a-113">This method has been replaced by **setSelectedState2**, which supports nested playlists.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a6a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1a6a-114">Requirements</span></span>



| <span data-ttu-id="d1a6a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1a6a-115">Requirement</span></span> | <span data-ttu-id="d1a6a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d1a6a-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d1a6a-117">Versão</span><span class="sxs-lookup"><span data-stu-id="d1a6a-117">Version</span></span><br/> | <span data-ttu-id="d1a6a-118">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d1a6a-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1a6a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1a6a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a6a-120">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="d1a6a-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="d1a6a-121">**PLAYLIST. setSelectedState2**</span><span class="sxs-lookup"><span data-stu-id="d1a6a-121">**PLAYLIST.setSelectedState2**</span></span>](playlist-setselectedstate2.md)
</dt> </dl>

 

 





