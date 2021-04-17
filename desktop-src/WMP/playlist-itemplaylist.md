---
title: PLAYLIST. lista de reprodução
description: O atributo doplaylist recupera a lista de reprodução para o item de mídia que é exibido no índice fornecido no elemento PLAYLIST.
ms.assetid: 094bcb5d-8a59-4531-96b8-0e993ca00be6
keywords:
- PLAYLIST. lista de reprodução do Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.itemPlaylist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d414692050e16dfd0aebe05901bcee0bc26580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782756"
---
# <a name="playlistitemplaylist"></a><span data-ttu-id="3fd44-104">PLAYLIST. lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="3fd44-104">PLAYLIST.itemPlaylist</span></span>

<span data-ttu-id="3fd44-105">O atributo **Doplaylist** recupera a lista de reprodução para o item de mídia que é exibido no índice fornecido no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="3fd44-105">The **itemPlaylist** attribute retrieves the playlist for the media item that is displayed at the given index in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.itemPlaylist(index)
```

## <a name="possible-values"></a><span data-ttu-id="3fd44-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="3fd44-106">Possible Values</span></span>

<span data-ttu-id="3fd44-107">Esse atributo é um objeto de **lista de reprodução** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3fd44-107">This attribute is a read-only **Playlist** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fd44-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fd44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd44-109"><span id="index"></span><span id="INDEX"></span>*index*</span><span class="sxs-lookup"><span data-stu-id="3fd44-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="3fd44-110">**Número**(**longo**) que contém o índice de um item da playlist.</span><span class="sxs-lookup"><span data-stu-id="3fd44-110">**Number**(**long**) containing the index of a playlist item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fd44-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fd44-111">Remarks</span></span>

<span data-ttu-id="3fd44-112">A propriedade **Doplaylist** retornará o objeto playlist que é expandido no elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="3fd44-112">The **itemPlaylist** property will return the playlist object that is expanded in the **PLAYLIST** element.</span></span> <span data-ttu-id="3fd44-113">Por exemplo, se houver duas listas de reprodução aninhadas que não são expandidas no elemento **playlist** e que contiverem três clipes **de mídia cada, a** lista de reprodução (1) retornará a playlist pai que contém as duas listas de reprodução aninhadas.</span><span class="sxs-lookup"><span data-stu-id="3fd44-113">For example, if there are two nested playlists that are not expanded in the **PLAYLIST** element, and that contain three media clips each, **itemPlaylist**(1) will return the parent playlist that contains the two nested playlists.</span></span> <span data-ttu-id="3fd44-114">Se a segunda playlist for expandida, a **lista de reprodução (1**) retornará a segunda playlist.</span><span class="sxs-lookup"><span data-stu-id="3fd44-114">If the second playlist is expanded, **itemPlaylist**(1) will return the second playlist.</span></span> <span data-ttu-id="3fd44-115">Se ambas as listas de reprodução forem expandidas, a lista **de reprodução (** 1) retornará a primeira playlist.</span><span class="sxs-lookup"><span data-stu-id="3fd44-115">If both playlists are expanded, **itemPlaylist**(1) will return the first playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd44-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd44-116">Requirements</span></span>



| <span data-ttu-id="3fd44-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd44-117">Requirement</span></span> | <span data-ttu-id="3fd44-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3fd44-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3fd44-119">Versão</span><span class="sxs-lookup"><span data-stu-id="3fd44-119">Version</span></span><br/> | <span data-ttu-id="3fd44-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="3fd44-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fd44-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fd44-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd44-122">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="3fd44-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="3fd44-123">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="3fd44-123">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





