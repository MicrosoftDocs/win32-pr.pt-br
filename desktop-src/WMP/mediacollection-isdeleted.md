---
title: Método mediacollection. IsDeleted
description: O método IsDeleted recupera um valor que indica se o item de mídia especificado está na pasta itens excluídos.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- método IsDeleted Windows Media Player
- método IsDeleted Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método IsDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813147"
---
# <a name="mediacollectionisdeleted-method"></a><span data-ttu-id="2cf4a-106">Método mediacollection. IsDeleted</span><span class="sxs-lookup"><span data-stu-id="2cf4a-106">MediaCollection.isDeleted method</span></span>

<span data-ttu-id="2cf4a-107">O método **IsDeleted** recupera um valor que indica se o item de mídia especificado está na pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-107">The **isDeleted** method retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf4a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cf4a-108">Syntax</span></span>


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="2cf4a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cf4a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cf4a-110">*Item* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="2cf4a-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cf4a-111">Objeto de **mídia** que pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-111">**Media** object that might be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cf4a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cf4a-112">Return value</span></span>

<span data-ttu-id="2cf4a-113">Esse método retorna um **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf4a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cf4a-114">Remarks</span></span>

<span data-ttu-id="2cf4a-115">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="2cf4a-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2cf4a-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2cf4a-117">**Windows Media Player 10 Mobile:** Esse método sempre retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-117">**Windows Media Player 10 Mobile:** This method always returns **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="2cf4a-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2cf4a-118">Examples</span></span>

<span data-ttu-id="2cf4a-119">O exemplo de JScript a seguir usa *mediacollection*. **IsDeleted** para testar se um item de mídia específico, armazenado na variável chamada mediaobject, está na pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-119">The following JScript example uses *MediaCollection*.**isDeleted** to test whether a particular media item, stored in the variable named mediaObject, is in the deleted items folder.</span></span> <span data-ttu-id="2cf4a-120">Se o item de mídia ainda não tiver sido excluído, ele será movido para a pasta itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-120">If the media item has not been deleted already, it is moved to the deleted items folder.</span></span> <span data-ttu-id="2cf4a-121">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2cf4a-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="2cf4a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cf4a-122">Requirements</span></span>



| <span data-ttu-id="2cf4a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf4a-123">Requirement</span></span> | <span data-ttu-id="2cf4a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2cf4a-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf4a-125">Versão</span><span class="sxs-lookup"><span data-stu-id="2cf4a-125">Version</span></span><br/> | <span data-ttu-id="2cf4a-126">Windows Media Player versão 7,0, Windows Media Player versão 7,1 ou Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-126">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="2cf4a-127">Esse método não tem suporte no Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2cf4a-127">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="2cf4a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2cf4a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="2cf4a-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cf4a-129"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="2cf4a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cf4a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf4a-131">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="2cf4a-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="2cf4a-132">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="2cf4a-132">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="2cf4a-133">**Mediacollection. setdeleted**</span><span class="sxs-lookup"><span data-stu-id="2cf4a-133">**MediaCollection.setDeleted**</span></span>](mediacollection-setdeleted.md)
</dt> <dt>

[<span data-ttu-id="2cf4a-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2cf4a-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="2cf4a-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="2cf4a-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





