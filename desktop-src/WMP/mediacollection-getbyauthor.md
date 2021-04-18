---
title: Método mediacollection. getByAuthor
description: O método getByAuthor recupera uma lista de reprodução dos itens de mídia pelo autor especificado.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- método getByAuthor Windows Media Player
- método getByAuthor Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAuthor
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7eae0928250e37e76bf3a39f38b43bef8a5691c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810830"
---
# <a name="mediacollectiongetbyauthor-method"></a><span data-ttu-id="c859e-106">Método mediacollection. getByAuthor</span><span class="sxs-lookup"><span data-stu-id="c859e-106">MediaCollection.getByAuthor method</span></span>

<span data-ttu-id="c859e-107">O método **getByAuthor** recupera uma lista de reprodução dos itens de mídia pelo autor especificado.</span><span class="sxs-lookup"><span data-stu-id="c859e-107">The **getByAuthor** method retrieves a playlist of the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="c859e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c859e-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a><span data-ttu-id="c859e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c859e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c859e-110">*criar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c859e-110">*author* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c859e-111">**Cadeia de caracteres** que contém o nome do autor.</span><span class="sxs-lookup"><span data-stu-id="c859e-111">**String** containing the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c859e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c859e-112">Return value</span></span>

<span data-ttu-id="c859e-113">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="c859e-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c859e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c859e-114">Remarks</span></span>

<span data-ttu-id="c859e-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c859e-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c859e-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c859e-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c859e-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c859e-117">Examples</span></span>

<span data-ttu-id="c859e-118">O exemplo de JScript a seguir usa *mediacollection*. **getByAuthor** para recuperar uma lista de reprodução de itens de mídia.</span><span class="sxs-lookup"><span data-stu-id="c859e-118">The following JScript example uses *MediaCollection*.**getByAuthor** to retrieve a playlist of media items.</span></span> <span data-ttu-id="c859e-119">A lista de reprodução contém itens que correspondem ao autor especificado pelo usuário em um elemento de entrada de texto HTML chamado getauthor.</span><span class="sxs-lookup"><span data-stu-id="c859e-119">The playlist contains items matching the author specified by the user in an HTML TEXT input element named GetAuthor.</span></span> <span data-ttu-id="c859e-120">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c859e-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="c859e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c859e-121">Requirements</span></span>



| <span data-ttu-id="c859e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c859e-122">Requirement</span></span> | <span data-ttu-id="c859e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c859e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c859e-124">Versão</span><span class="sxs-lookup"><span data-stu-id="c859e-124">Version</span></span><br/> | <span data-ttu-id="c859e-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c859e-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c859e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c859e-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c859e-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c859e-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c859e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c859e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c859e-129">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="c859e-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c859e-130">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="c859e-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="c859e-131">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c859e-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c859e-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c859e-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





