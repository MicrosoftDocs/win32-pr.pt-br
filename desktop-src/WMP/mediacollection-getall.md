---
title: Método mediacollection. getAll
description: O método getAll recupera uma lista de reprodução que contém todos os itens de mídia na biblioteca.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- método getAll Windows Media Player
- método getAll Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1681cd533be4084123cb80cdcc199ab5e1ce2981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779989"
---
# <a name="mediacollectiongetall-method"></a><span data-ttu-id="34768-106">Método mediacollection. getAll</span><span class="sxs-lookup"><span data-stu-id="34768-106">MediaCollection.getAll method</span></span>

<span data-ttu-id="34768-107">O método **getAll** recupera uma lista de reprodução que contém todos os itens de mídia na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="34768-107">The **getAll** method retrieves a playlist containing all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="34768-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="34768-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a><span data-ttu-id="34768-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34768-109">Parameters</span></span>

<span data-ttu-id="34768-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="34768-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34768-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34768-111">Return value</span></span>

<span data-ttu-id="34768-112">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="34768-112">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34768-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="34768-113">Remarks</span></span>

<span data-ttu-id="34768-114">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="34768-114">To use this method, read access to the library is required.</span></span> <span data-ttu-id="34768-115">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="34768-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="34768-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="34768-116">Examples</span></span>

<span data-ttu-id="34768-117">O exemplo de JScript a seguir usa *mediacollection*. **getAll** para reproduzir itens de mídia aleatoriamente da coleção de mídias.</span><span class="sxs-lookup"><span data-stu-id="34768-117">The following JScript example uses *MediaCollection*.**getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="34768-118">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="34768-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="34768-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34768-119">Requirements</span></span>



| <span data-ttu-id="34768-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="34768-120">Requirement</span></span> | <span data-ttu-id="34768-121">Valor</span><span class="sxs-lookup"><span data-stu-id="34768-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34768-122">Versão</span><span class="sxs-lookup"><span data-stu-id="34768-122">Version</span></span><br/> | <span data-ttu-id="34768-123">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="34768-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="34768-124">DLL</span><span class="sxs-lookup"><span data-stu-id="34768-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="34768-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34768-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34768-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="34768-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34768-127">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="34768-127">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="34768-128">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="34768-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="34768-129">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="34768-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="34768-130">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="34768-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





