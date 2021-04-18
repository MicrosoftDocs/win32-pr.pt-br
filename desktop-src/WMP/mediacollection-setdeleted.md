---
title: Método mediacollection. setdeleted
description: O método setdeled move o item de mídia especificado para a pasta itens excluídos. | Método mediacollection. setdeleted
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- método setdeled Media Player do Windows
- método setdeleted Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método setdeled
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760060"
---
# <a name="mediacollectionsetdeleted-method"></a><span data-ttu-id="5f15f-107">Método mediacollection. setdeleted</span><span class="sxs-lookup"><span data-stu-id="5f15f-107">MediaCollection.setDeleted method</span></span>

<span data-ttu-id="5f15f-108">O método **Setdeled** move o item de mídia especificado para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="5f15f-108">The **setDeleted** method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f15f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f15f-109">Syntax</span></span>


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a><span data-ttu-id="5f15f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f15f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f15f-111">*Item* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="5f15f-111">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f15f-112">Objeto de **mídia** que está sendo movido.</span><span class="sxs-lookup"><span data-stu-id="5f15f-112">**Media** object being moved.</span></span>

</dd> <dt>

<span data-ttu-id="5f15f-113">*verdadeiro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f15f-113">*true* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f15f-114">Sempre Especifique esse valor.</span><span class="sxs-lookup"><span data-stu-id="5f15f-114">Always specify this value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f15f-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f15f-115">Return value</span></span>

<span data-ttu-id="5f15f-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5f15f-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f15f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f15f-117">Remarks</span></span>

<span data-ttu-id="5f15f-118">Esse método não remove arquivos do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="5f15f-118">This method does not remove files from the user's computer.</span></span>

<span data-ttu-id="5f15f-119">Para usar esse método, é necessário ter acesso completo à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5f15f-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="5f15f-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5f15f-120">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5f15f-121">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="5f15f-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="5f15f-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f15f-122">Examples</span></span>

<span data-ttu-id="5f15f-123">O exemplo de JScript a seguir usa *mediacollection*. **Setdeled** para mover um item de mídia específico, armazenado na variável chamada mediaobject, para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="5f15f-123">The following JScript example uses *MediaCollection*.**setDeleted** to move a particular media item, stored in the variable named mediaObject, to the deleted items folder.</span></span> <span data-ttu-id="5f15f-124">O *mediacollection*. o método **IsDeleted** testa primeiro se o item já foi excluído.</span><span class="sxs-lookup"><span data-stu-id="5f15f-124">The *MediaCollection*.**isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="5f15f-125">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5f15f-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="5f15f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f15f-126">Requirements</span></span>



| <span data-ttu-id="5f15f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f15f-127">Requirement</span></span> | <span data-ttu-id="5f15f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5f15f-128">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f15f-129">Versão</span><span class="sxs-lookup"><span data-stu-id="5f15f-129">Version</span></span><br/> | <span data-ttu-id="5f15f-130">Windows Media Player versão 7,0, Windows Media Player versão 7,1 ou Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5f15f-130">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="5f15f-131">Esse método não tem suporte no Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5f15f-131">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="5f15f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5f15f-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f15f-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f15f-133"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="5f15f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f15f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f15f-135">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="5f15f-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5f15f-136">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="5f15f-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="5f15f-137">**Mediacollection. IsDeleted**</span><span class="sxs-lookup"><span data-stu-id="5f15f-137">**MediaCollection.isDeleted**</span></span>](mediacollection-isdeleted.md)
</dt> <dt>

[<span data-ttu-id="5f15f-138">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5f15f-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5f15f-139">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5f15f-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





