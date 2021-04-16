---
title: Método mediacollection. getByGenre
description: O método getByGenre recupera uma lista de reprodução dos itens de mídia com o gênero especificado.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- método getByGenre Windows Media Player
- método getByGenre Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByGenre
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779409"
---
# <a name="mediacollectiongetbygenre-method"></a><span data-ttu-id="e64d5-106">Método mediacollection. getByGenre</span><span class="sxs-lookup"><span data-stu-id="e64d5-106">MediaCollection.getByGenre method</span></span>

<span data-ttu-id="e64d5-107">O método **getByGenre** recupera uma lista de reprodução dos itens de mídia com o gênero especificado.</span><span class="sxs-lookup"><span data-stu-id="e64d5-107">The **getByGenre** method retrieves a playlist of the media items with the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="e64d5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e64d5-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a><span data-ttu-id="e64d5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e64d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e64d5-110">*gênero* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e64d5-110">*genre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e64d5-111">**Cadeia de caracteres** que contém o nome do gênero.</span><span class="sxs-lookup"><span data-stu-id="e64d5-111">**String** containing the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e64d5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e64d5-112">Return value</span></span>

<span data-ttu-id="e64d5-113">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="e64d5-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e64d5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e64d5-114">Remarks</span></span>

<span data-ttu-id="e64d5-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e64d5-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e64d5-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e64d5-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e64d5-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e64d5-117">Examples</span></span>

<span data-ttu-id="e64d5-118">O exemplo de JScript a seguir usa *mediacollection*. **getByGenre** para recuperar uma lista de reprodução de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="e64d5-118">The following JScript example uses *MediaCollection*.**getByGenre** to retrieve a playlist of media items.</span></span> <span data-ttu-id="e64d5-119">A lista de reprodução contém itens com o gênero especificado pelo usuário em um elemento de entrada de texto HTML chamado getgênero.</span><span class="sxs-lookup"><span data-stu-id="e64d5-119">The playlist contains items with the genre specified by the user in an HTML TEXT input element named GetGenre.</span></span> <span data-ttu-id="e64d5-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e64d5-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="e64d5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e64d5-121">Requirements</span></span>



| <span data-ttu-id="e64d5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e64d5-122">Requirement</span></span> | <span data-ttu-id="e64d5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e64d5-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e64d5-124">Versão</span><span class="sxs-lookup"><span data-stu-id="e64d5-124">Version</span></span><br/> | <span data-ttu-id="e64d5-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e64d5-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e64d5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e64d5-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="e64d5-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e64d5-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e64d5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e64d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e64d5-129">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="e64d5-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="e64d5-130">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="e64d5-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="e64d5-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e64d5-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e64d5-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e64d5-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





