---
title: Método mediacollection. getByAlbum
description: O método GetByAlbum recupera uma lista de reprodução que contém os itens de mídia do álbum especificado.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- método getByAlbum Windows Media Player
- método getByAlbum Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAlbum
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784191"
---
# <a name="mediacollectiongetbyalbum-method"></a><span data-ttu-id="e967f-106">Método mediacollection. getByAlbum</span><span class="sxs-lookup"><span data-stu-id="e967f-106">MediaCollection.getByAlbum method</span></span>

<span data-ttu-id="e967f-107">O método **GetByAlbum** recupera uma lista de reprodução que contém os itens de mídia do álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="e967f-107">The **GetByAlbum** method retrieves a playlist containing the media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="e967f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e967f-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a><span data-ttu-id="e967f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e967f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e967f-110">*álbum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e967f-110">*album* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e967f-111">**Cadeia de caracteres** que contém o nome do álbum.</span><span class="sxs-lookup"><span data-stu-id="e967f-111">**String** containing the name of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e967f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e967f-112">Return value</span></span>

<span data-ttu-id="e967f-113">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="e967f-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e967f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e967f-114">Remarks</span></span>

<span data-ttu-id="e967f-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e967f-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e967f-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e967f-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e967f-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e967f-117">Examples</span></span>

<span data-ttu-id="e967f-118">O exemplo a seguir usa *mediacollection*. **getByAlbum** para recuperar uma lista de reprodução de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="e967f-118">The following example uses *MediaCollection*.**getByAlbum** to retrieve a playlist of media items.</span></span> <span data-ttu-id="e967f-119">A lista de reprodução contém itens com o álbum especificado pelo usuário em um elemento de entrada de texto HTML chamado getalbum.</span><span class="sxs-lookup"><span data-stu-id="e967f-119">The playlist contains items with the album specified by the user in an HTML TEXT input element named GetAlbum.</span></span> <span data-ttu-id="e967f-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e967f-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="e967f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e967f-121">Requirements</span></span>



| <span data-ttu-id="e967f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e967f-122">Requirement</span></span> | <span data-ttu-id="e967f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e967f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e967f-124">Versão</span><span class="sxs-lookup"><span data-stu-id="e967f-124">Version</span></span><br/> | <span data-ttu-id="e967f-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e967f-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e967f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e967f-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="e967f-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e967f-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e967f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e967f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e967f-129">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="e967f-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="e967f-130">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="e967f-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="e967f-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e967f-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e967f-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e967f-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





