---
title: Método Media. getItemInfoByAtom
description: O método getItemInfoByAtom recupera o valor do atributo com o número de índice especificado.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- método getItemInfoByAtom Windows Media Player
- método getItemInfoByAtom Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794618"
---
# <a name="mediagetiteminfobyatom-method"></a><span data-ttu-id="26c27-106">Método Media. getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="26c27-106">Media.getItemInfoByAtom method</span></span>

<span data-ttu-id="26c27-107">O método **getItemInfoByAtom** recupera o valor do atributo com o número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="26c27-107">The **getItemInfoByAtom** method retrieves the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="26c27-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26c27-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="26c27-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26c27-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c27-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="26c27-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26c27-111">**Número** (**longo**) que especifica o índice no qual um determinado atributo reside no conjunto de atributos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="26c27-111">**Number** (**long**) specifying the index at which a given attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26c27-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26c27-112">Return value</span></span>

<span data-ttu-id="26c27-113">Esse método retorna uma **cadeia de caracteres** que representa o valor do atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="26c27-113">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="26c27-114">Para atributos cujo valor subjacente é **booliano**, ele retorna a cadeia de caracteres "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="26c27-114">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="26c27-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="26c27-115">Remarks</span></span>

<span data-ttu-id="26c27-116">Esse método pode ser usado para recuperar metadados para um item de mídia digital específico usando um número de índice de atributo.</span><span class="sxs-lookup"><span data-stu-id="26c27-116">This method can be used to retrieve metadata for a specific digital media item by using an attribute index number.</span></span> <span data-ttu-id="26c27-117">A propriedade **attributeCount** pode ser usada para determinar o número de atributos disponíveis para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="26c27-117">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="26c27-118">O método **getMediaAtom** do objeto **mediacollection** também pode ser usado para recuperar o índice de um atributo específico.</span><span class="sxs-lookup"><span data-stu-id="26c27-118">The **getMediaAtom** method of the **MediaCollection** object can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="26c27-119">Essa técnica geralmente é mais eficiente do que os métodos **getItemInfo** ou **getItemInfoByType** ao trabalhar com listas de reprodução grandes.</span><span class="sxs-lookup"><span data-stu-id="26c27-119">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="26c27-120">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="26c27-120">To use this method, read access to the library is required.</span></span> <span data-ttu-id="26c27-121">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="26c27-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="26c27-122">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player..</span><span class="sxs-lookup"><span data-stu-id="26c27-122">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="26c27-123">**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="26c27-123">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="26c27-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26c27-124">Requirements</span></span>



| <span data-ttu-id="26c27-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="26c27-125">Requirement</span></span> | <span data-ttu-id="26c27-126">Valor</span><span class="sxs-lookup"><span data-stu-id="26c27-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26c27-127">Versão</span><span class="sxs-lookup"><span data-stu-id="26c27-127">Version</span></span><br/> | <span data-ttu-id="26c27-128">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="26c27-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="26c27-129">DLL</span><span class="sxs-lookup"><span data-stu-id="26c27-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="26c27-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26c27-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26c27-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="26c27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26c27-132">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="26c27-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="26c27-133">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="26c27-133">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="26c27-134">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="26c27-134">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="26c27-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="26c27-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="26c27-136">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="26c27-136">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="26c27-137">**Mediacollection. getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="26c27-137">**MediaCollection.getMediaAtom**</span></span>](mediacollection-getmediaatom.md)
</dt> <dt>

[<span data-ttu-id="26c27-138">**Lendo valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="26c27-138">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="26c27-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="26c27-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="26c27-140">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="26c27-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





