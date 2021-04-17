---
title: Método playlist. Item
description: O método item recupera o item de mídia no índice especificado.
ms.assetid: a564f6db-ede4-4c85-87ca-0e2539d914c2
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe playlist
- Classe playlist Windows Media Player, método item
topic_type:
- apiref
api_name:
- Playlist.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c69386871aeec33dbc36a066ce3f75e80d7514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784676"
---
# <a name="playlistitem-method"></a><span data-ttu-id="7b347-106">Método playlist. Item</span><span class="sxs-lookup"><span data-stu-id="7b347-106">Playlist.item method</span></span>

<span data-ttu-id="7b347-107">O método **Item** recupera o item de mídia no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7b347-107">The **item** method retrieves the media item at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b347-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b347-108">Syntax</span></span>


```JScript
retVal = Playlist.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="7b347-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b347-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b347-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7b347-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b347-111">**Número** (**longo**) que contém o índice do item a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="7b347-111">**Number** (**long**) containing the index of the item to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b347-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b347-112">Return value</span></span>

<span data-ttu-id="7b347-113">Esse método retorna um objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="7b347-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b347-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b347-114">Remarks</span></span>

<span data-ttu-id="7b347-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7b347-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7b347-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7b347-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7b347-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b347-117">Examples</span></span>

<span data-ttu-id="7b347-118">O exemplo de JScript a seguir usa a *lista de reprodução*. **Item** para recuperar um item de mídia da playlist atual com base em uma seleção de usuário.</span><span class="sxs-lookup"><span data-stu-id="7b347-118">The following JScript example uses *Playlist*.**item** to retrieve a media item from the current playlist based on a user selection.</span></span> <span data-ttu-id="7b347-119">Um elemento HTML SELECT foi criado com o nome "weblist" e preenchido com os títulos da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="7b347-119">An HTML SELECT element was created with name "weblist", and filled with the titles from the current playlist.</span></span> <span data-ttu-id="7b347-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7b347-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the value of the selected item in the list box
// using the selectedIndex property.
var index = weblist.selectedIndex;

// Store the corresponding digital media object from the current playlist.
var listItem = Player.currentPlaylist.item(index);

// Set the URL using the listItem variable.
Player.URL = listItem.sourceURL;

```



## <a name="requirements"></a><span data-ttu-id="7b347-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b347-121">Requirements</span></span>



| <span data-ttu-id="7b347-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b347-122">Requirement</span></span> | <span data-ttu-id="7b347-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7b347-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b347-124">Versão</span><span class="sxs-lookup"><span data-stu-id="7b347-124">Version</span></span><br/> | <span data-ttu-id="7b347-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7b347-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7b347-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7b347-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b347-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b347-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b347-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b347-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b347-129">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="7b347-129">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7b347-130">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="7b347-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="7b347-131">**Playlist. insertItem**</span><span class="sxs-lookup"><span data-stu-id="7b347-131">**Playlist.insertItem**</span></span>](playlist-insertitem.md)
</dt> <dt>

[<span data-ttu-id="7b347-132">**Playlist. removeItem**</span><span class="sxs-lookup"><span data-stu-id="7b347-132">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="7b347-133">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7b347-133">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7b347-134">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7b347-134">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





