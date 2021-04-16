---
title: Método mediacollection. getByName
description: O método getByName recupera uma lista de reprodução dos itens de mídia com o nome especificado.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- método getByName Windows Media Player
- método getByName Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758191"
---
# <a name="mediacollectiongetbyname-method"></a><span data-ttu-id="5a95d-106">Método mediacollection. getByName</span><span class="sxs-lookup"><span data-stu-id="5a95d-106">MediaCollection.getByName method</span></span>

<span data-ttu-id="5a95d-107">O método **getByName** recupera uma lista de reprodução dos itens de mídia com o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="5a95d-107">The **getByName** method retrieves a playlist of the media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a95d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a95d-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="5a95d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a95d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a95d-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5a95d-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a95d-111">**Cadeia de caracteres** que contém o nome.</span><span class="sxs-lookup"><span data-stu-id="5a95d-111">**String** containing the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a95d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a95d-112">Return value</span></span>

<span data-ttu-id="5a95d-113">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="5a95d-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a95d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a95d-114">Remarks</span></span>

<span data-ttu-id="5a95d-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5a95d-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5a95d-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5a95d-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5a95d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5a95d-117">Examples</span></span>

<span data-ttu-id="5a95d-118">O exemplo de JScript a seguir usa *mediacollection*. **getByName** para recuperar três itens da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5a95d-118">The following JScript example uses *MediaCollection*.**getByName** to retrieve three items from the library.</span></span> <span data-ttu-id="5a95d-119">Cada item é acrescentado à playlist atual.</span><span class="sxs-lookup"><span data-stu-id="5a95d-119">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="5a95d-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5a95d-120">The **Player** object was created with ID="Player".</span></span>


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

```



## <a name="requirements"></a><span data-ttu-id="5a95d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a95d-121">Requirements</span></span>



| <span data-ttu-id="5a95d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a95d-122">Requirement</span></span> | <span data-ttu-id="5a95d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5a95d-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5a95d-124">Versão</span><span class="sxs-lookup"><span data-stu-id="5a95d-124">Version</span></span><br/> | <span data-ttu-id="5a95d-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5a95d-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5a95d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5a95d-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a95d-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a95d-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a95d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a95d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a95d-129">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="5a95d-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="5a95d-130">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="5a95d-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5a95d-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5a95d-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5a95d-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5a95d-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





