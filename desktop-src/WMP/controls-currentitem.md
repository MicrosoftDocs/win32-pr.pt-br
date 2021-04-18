---
title: Controls. currentItem
description: A propriedade currentItem especifica ou recupera o item de mídia atual.
ms.assetid: 77e21585-3cc8-41f5-97b5-da6eb992c7bc
keywords:
- Controls. currentItem Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentItem
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81658665cb6f31acd327f5050a733a2fc3c70371
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788182"
---
# <a name="controlscurrentitem"></a><span data-ttu-id="214c1-104">Controls. currentItem</span><span class="sxs-lookup"><span data-stu-id="214c1-104">Controls.currentItem</span></span>

<span data-ttu-id="214c1-105">A propriedade **currentItem** especifica ou recupera o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="214c1-105">The **currentItem** property specifies or retrieves the current media item.</span></span>

``` syntax
player.controls.currentItem
      
```

## <a name="possible-values"></a><span data-ttu-id="214c1-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="214c1-106">Possible Values</span></span>

<span data-ttu-id="214c1-107">Esta propriedade é um objeto de **mídia** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="214c1-107">This property is a read/write **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="214c1-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="214c1-108">Remarks</span></span>

<span data-ttu-id="214c1-109">Esse método funciona apenas com itens no *Player*. **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="214c1-109">This method works only with items in *Player*.**currentPlaylist**.</span></span> <span data-ttu-id="214c1-110">Não há suporte para chamar **currentItem** com uma referência a um item de mídia salvo.</span><span class="sxs-lookup"><span data-stu-id="214c1-110">Calling **currentItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="214c1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="214c1-111">Examples</span></span>

<span data-ttu-id="214c1-112">O exemplo de JScript a seguir usa **currentItem** para definir o item de mídia atual do controle Player para o valor selecionado em um elemento HTML SELECT.</span><span class="sxs-lookup"><span data-stu-id="214c1-112">The following JScript example uses **currentItem** to set the player control current media item to the selected value in an HTML SELECT element.</span></span> <span data-ttu-id="214c1-113">A playlist atual foi especificada pela primeira vez usando *playlistcollection*. **getByName**.</span><span class="sxs-lookup"><span data-stu-id="214c1-113">The current playlist was first specified by using *PlaylistCollection*.**getByName**.</span></span> <span data-ttu-id="214c1-114">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="214c1-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = playItem  NAME = "playItem"  LANGUAGE = "JScript"

    /* Specify the current item when the selected list value changes. */
    onChange = "Player.controls.currentItem = Player.currentPlaylist.item(playItem.value);">

    /* Fill the SELECT element list with three items that match
       the songs in the playlist. */
    <OPTION VALUE = 0 >Laure
    <OPTION VALUE = 1 >Jeanne
    <OPTION VALUE = 2 >House
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="214c1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214c1-115">Requirements</span></span>



| <span data-ttu-id="214c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="214c1-116">Requirement</span></span> | <span data-ttu-id="214c1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="214c1-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="214c1-118">Versão</span><span class="sxs-lookup"><span data-stu-id="214c1-118">Version</span></span><br/> | <span data-ttu-id="214c1-119">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="214c1-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="214c1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="214c1-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="214c1-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="214c1-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214c1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="214c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214c1-123">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="214c1-123">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="214c1-124">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="214c1-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="214c1-125">**Playlistcollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="214c1-125">**PlaylistCollection.getByName**</span></span>](playlistcollection-getbyname.md)
</dt> </dl>

 

 





