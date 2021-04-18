---
title: Método cdromCollection. Item
description: O método item recupera o objeto cdrom no índice fornecido.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- método de item Windows Media Player
- método de item Windows Media Player, classe cdromCollection
- Classe cdromCollection Windows Media Player, método de item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796438"
---
# <a name="cdromcollectionitem-method"></a><span data-ttu-id="f189b-106">Método cdromCollection. Item</span><span class="sxs-lookup"><span data-stu-id="f189b-106">CdromCollection.item method</span></span>

<span data-ttu-id="f189b-107">O método **Item** recupera o objeto **cdrom** no índice fornecido.</span><span class="sxs-lookup"><span data-stu-id="f189b-107">The **item** method retrieves the **Cdrom** object at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f189b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f189b-108">Syntax</span></span>


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="f189b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f189b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f189b-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f189b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f189b-111">**Número** (**longo**) que contém o índice.</span><span class="sxs-lookup"><span data-stu-id="f189b-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f189b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f189b-112">Return value</span></span>

<span data-ttu-id="f189b-113">Esse método retorna um objeto de **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="f189b-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f189b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f189b-114">Remarks</span></span>

<span data-ttu-id="f189b-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f189b-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f189b-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f189b-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f189b-117">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="f189b-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f189b-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f189b-118">Examples</span></span>

<span data-ttu-id="f189b-119">O exemplo de JScript a seguir usa *cdromCollection*. **Item** para imprimir o nome da playlist de cada CD disponível no computador.</span><span class="sxs-lookup"><span data-stu-id="f189b-119">The following JScript example uses *CdromCollection*.**item** to print the playlist name from each CD available on the computer.</span></span> <span data-ttu-id="f189b-120">Se a unidade realmente contiver conteúdo de DVD, o Windows XP ou posterior será necessário.</span><span class="sxs-lookup"><span data-stu-id="f189b-120">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="f189b-121">Um elemento de TextArea HTML foi criado com ID = "playlists".</span><span class="sxs-lookup"><span data-stu-id="f189b-121">An HTML TextArea element was created with ID = "playlists".</span></span> <span data-ttu-id="f189b-122">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f189b-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="f189b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f189b-123">Requirements</span></span>



| <span data-ttu-id="f189b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f189b-124">Requirement</span></span> | <span data-ttu-id="f189b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f189b-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f189b-126">Versão</span><span class="sxs-lookup"><span data-stu-id="f189b-126">Version</span></span><br/> | <span data-ttu-id="f189b-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="f189b-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f189b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f189b-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f189b-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f189b-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f189b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f189b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f189b-131">**Cdrom. driveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="f189b-131">**Cdrom.driveSpecifier**</span></span>](cdrom-drivespecifier.md)
</dt> <dt>

[<span data-ttu-id="f189b-132">**Objeto cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="f189b-132">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="f189b-133">**CdromCollection. contagem**</span><span class="sxs-lookup"><span data-stu-id="f189b-133">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="f189b-134">**Playlist.name**</span><span class="sxs-lookup"><span data-stu-id="f189b-134">**Playlist.name**</span></span>](playlist-name.md)
</dt> <dt>

[<span data-ttu-id="f189b-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f189b-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f189b-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f189b-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





