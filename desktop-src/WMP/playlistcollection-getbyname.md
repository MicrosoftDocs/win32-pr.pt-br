---
title: Método playlistcollection. getByName
description: O método getByName recupera um objeto PlaylistArray contendo listas de reprodução com o nome especificado, se existir.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- método getByName Windows Media Player
- método getByName Windows Media Player, classe Playlistcollection
- Classe playlistcollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761558"
---
# <a name="playlistcollectiongetbyname-method"></a><span data-ttu-id="f3311-106">Método playlistcollection. getByName</span><span class="sxs-lookup"><span data-stu-id="f3311-106">PlaylistCollection.getByName method</span></span>

<span data-ttu-id="f3311-107">O método **getByName** recupera um objeto **PlaylistArray** contendo listas de reprodução com o nome especificado, se existir.</span><span class="sxs-lookup"><span data-stu-id="f3311-107">The **getByName** method retrieves a **PlaylistArray** object containing playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3311-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3311-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="f3311-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3311-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3311-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f3311-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3311-111">**Cadeia de caracteres** que contém o nome das listas de reprodução a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="f3311-111">**String** containing the name of the playlists to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3311-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3311-112">Return value</span></span>

<span data-ttu-id="f3311-113">Esse método retorna um objeto **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="f3311-113">This method returns a **PlaylistArray** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3311-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3311-114">Remarks</span></span>

<span data-ttu-id="f3311-115">Use *PlaylistArray*. **contagem** para determinar se existe uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f3311-115">Use *PlaylistArray*.**count** to determine whether a playlist exists.</span></span> <span data-ttu-id="f3311-116">Se **Count** for zero, uma playlist não existirá.</span><span class="sxs-lookup"><span data-stu-id="f3311-116">If **count** is zero, a playlist does not exist.</span></span>

<span data-ttu-id="f3311-117">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f3311-117">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f3311-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f3311-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f3311-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f3311-119">Examples</span></span>

<span data-ttu-id="f3311-120">O exemplo de JScript a seguir usa *playlistcollection*. **getByName** para verificar o objeto **playlistcollection** de uma lista de reprodução chamada "trêslist".</span><span class="sxs-lookup"><span data-stu-id="f3311-120">The following JScript example uses *playlistCollection*.**getByName** to check the **playlistCollection** object for a playlist named "ThreeList".</span></span> <span data-ttu-id="f3311-121">Se a lista de reprodução de "três listas" existir, **getByName** definirá "3list" como a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="f3311-121">If the "Threelist" playlist exists, **getByName** sets "ThreeList" as the current playlist.</span></span> <span data-ttu-id="f3311-122">O objeto de **jogador** foi criado com a ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f3311-122">The **Player** object was created with the ID = "Player".</span></span>


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a><span data-ttu-id="f3311-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3311-123">Requirements</span></span>



| <span data-ttu-id="f3311-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3311-124">Requirement</span></span> | <span data-ttu-id="f3311-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f3311-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3311-126">Versão</span><span class="sxs-lookup"><span data-stu-id="f3311-126">Version</span></span><br/> | <span data-ttu-id="f3311-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f3311-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f3311-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f3311-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f3311-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3311-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3311-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3311-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3311-131">**Objeto PlaylistArray**</span><span class="sxs-lookup"><span data-stu-id="f3311-131">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="f3311-132">**Contagem de PlaylistArray.**</span><span class="sxs-lookup"><span data-stu-id="f3311-132">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="f3311-133">**Objeto playlistcollection**</span><span class="sxs-lookup"><span data-stu-id="f3311-133">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="f3311-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f3311-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f3311-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f3311-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





