---
title: Método mediacollection. Remove
description: O método remove remove um item da coleção de mídia.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- remover método Windows Media Player
- Método Remove Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, remover método
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782981"
---
# <a name="mediacollectionremove-method"></a><span data-ttu-id="2e7c4-106">Método mediacollection. Remove</span><span class="sxs-lookup"><span data-stu-id="2e7c4-106">MediaCollection.remove method</span></span>

<span data-ttu-id="2e7c4-107">O método **Remove** remove um item da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-107">The **remove** method removes an item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7c4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e7c4-108">Syntax</span></span>


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a><span data-ttu-id="2e7c4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e7c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e7c4-110">*Item* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2e7c4-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e7c4-111">Objeto de **mídia** a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-111">**Media** object to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2e7c4-112">*excluir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e7c4-112">*delete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e7c4-113">**Booliano** que indica se o item deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-113">**Boolean** indicating whether to remove the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e7c4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e7c4-114">Return value</span></span>

<span data-ttu-id="2e7c4-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7c4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e7c4-116">Remarks</span></span>

<span data-ttu-id="2e7c4-117">Esse método exclui um item da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-117">This method deletes an item from the library.</span></span> <span data-ttu-id="2e7c4-118">Esse método não exclui arquivos do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="2e7c4-119">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="2e7c4-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2e7c4-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2e7c4-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2e7c4-121">Examples</span></span>

<span data-ttu-id="2e7c4-122">O exemplo de JScript a seguir, depois de solicitar o usuário, exclui permanentemente o primeiro item de mídia na coleção de mídia usando *mediacollection*. **remover**.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-122">The following JScript example, after prompting the user, permanently deletes the first media item in the media collection by using *MediaCollection*.**remove**.</span></span> <span data-ttu-id="2e7c4-123">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2e7c4-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a><span data-ttu-id="2e7c4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e7c4-124">Requirements</span></span>



| <span data-ttu-id="2e7c4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e7c4-125">Requirement</span></span> | <span data-ttu-id="2e7c4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2e7c4-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7c4-127">Versão</span><span class="sxs-lookup"><span data-stu-id="2e7c4-127">Version</span></span><br/> | <span data-ttu-id="2e7c4-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2e7c4-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2e7c4-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2e7c4-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e7c4-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e7c4-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7c4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e7c4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7c4-132">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="2e7c4-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="2e7c4-133">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="2e7c4-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="2e7c4-134">**Mediacollection. adicionar**</span><span class="sxs-lookup"><span data-stu-id="2e7c4-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="2e7c4-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2e7c4-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2e7c4-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2e7c4-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





