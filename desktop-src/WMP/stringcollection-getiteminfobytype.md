---
title: Método StringCollection. getItemInfoByType
description: O método getItemInfoByType recupera o valor correspondente ao índice, nome, idioma e índice da StringCollection especificados.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- método getItemInfoByType Windows Media Player
- método getItemInfoByType Windows Media Player, classe StringCollection
- Classe StringCollection Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791275"
---
# <a name="stringcollectiongetiteminfobytype-method"></a><span data-ttu-id="01924-106">Método StringCollection. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="01924-106">StringCollection.getItemInfoByType method</span></span>

<span data-ttu-id="01924-107">O método **getItemInfoByType** recupera o valor correspondente ao índice, nome, idioma e índice da **StringCollection** especificados.</span><span class="sxs-lookup"><span data-stu-id="01924-107">The **getItemInfoByType** method retrieves the value corresponding to the specified **StringCollection** index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="01924-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01924-108">Syntax</span></span>


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a><span data-ttu-id="01924-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01924-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01924-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="01924-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01924-111">**Número** (**longo**) especificando o índice de base zero do item **StringCollection** do qual obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="01924-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="01924-112">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="01924-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01924-113">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="01924-113">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="01924-114">*idioma* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="01924-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01924-115">**Cadeia de caracteres** que contém o idioma.</span><span class="sxs-lookup"><span data-stu-id="01924-115">**String** containing the language.</span></span> <span data-ttu-id="01924-116">Se o valor for definido como NULL ou a cadeia de caracteres vazia (""), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="01924-116">If the value is set to null or the empty string ("") the current locale string is used.</span></span> <span data-ttu-id="01924-117">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="01924-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="01924-118">*attributeIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="01924-118">*attributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01924-119">**Número** (**longo**) que contém o índice de base zero do valor a ser recuperado do atributo.</span><span class="sxs-lookup"><span data-stu-id="01924-119">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01924-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01924-120">Return value</span></span>

<span data-ttu-id="01924-121">Esse método retorna um **número**, uma **cadeia de caracteres**, um objeto **MetadataPicture** ou um objeto **MetadataText** , conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="01924-121">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="01924-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="01924-122">Attribute</span></span>                   | <span data-ttu-id="01924-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01924-123">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="01924-124">**Sincronizarstate**</span><span class="sxs-lookup"><span data-stu-id="01924-124">**SyncState**</span></span>               | <span data-ttu-id="01924-125">**Número** (**longo sem sinal**)</span><span class="sxs-lookup"><span data-stu-id="01924-125">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="01924-126">**WM/letras de música \_ sincronizadas**</span><span class="sxs-lookup"><span data-stu-id="01924-126">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="01924-127">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="01924-127">**MetadataText** object</span></span>        |
| <span data-ttu-id="01924-128">**WM/imagem**</span><span class="sxs-lookup"><span data-stu-id="01924-128">**WM/Picture**</span></span>              | <span data-ttu-id="01924-129">Objeto **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="01924-129">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="01924-130">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="01924-130">**WM/UserWebURL**</span></span>           | <span data-ttu-id="01924-131">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="01924-131">**MetadataText** object</span></span>        |
| <span data-ttu-id="01924-132">Todos os outros atributos</span><span class="sxs-lookup"><span data-stu-id="01924-132">All other attributes</span></span>        | <span data-ttu-id="01924-133">String</span><span class="sxs-lookup"><span data-stu-id="01924-133">String</span></span>                         |



 

<span data-ttu-id="01924-134">Para atributos cujo valor subjacente é **booliano**, esse método retorna a cadeia de caracteres "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="01924-134">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="01924-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="01924-135">Remarks</span></span>

<span data-ttu-id="01924-136">Esse método dá suporte a atributos com vários valores e atributos com valores complexos.</span><span class="sxs-lookup"><span data-stu-id="01924-136">This method supports attributes with multiple values, and attributes with complex values.</span></span> <span data-ttu-id="01924-137">O método **getItemInfo** não oferece suporte a atributos com valores múltiplos ou complexos.</span><span class="sxs-lookup"><span data-stu-id="01924-137">The **getItemInfo** method does not support attributes with multiple or complex values.</span></span>

<span data-ttu-id="01924-138">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="01924-138">To use this method, read access to the library is required.</span></span> <span data-ttu-id="01924-139">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="01924-139">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01924-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01924-140">Requirements</span></span>



| <span data-ttu-id="01924-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="01924-141">Requirement</span></span> | <span data-ttu-id="01924-142">Valor</span><span class="sxs-lookup"><span data-stu-id="01924-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01924-143">Versão</span><span class="sxs-lookup"><span data-stu-id="01924-143">Version</span></span><br/> | <span data-ttu-id="01924-144">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="01924-144">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="01924-145">DLL</span><span class="sxs-lookup"><span data-stu-id="01924-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="01924-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01924-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01924-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="01924-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01924-148">**Objeto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="01924-148">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="01924-149">**Objeto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="01924-149">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="01924-150">**StringCollection. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="01924-150">**StringCollection.getItemInfo**</span></span>](stringcollection-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="01924-151">**Objeto StringCollection**</span><span class="sxs-lookup"><span data-stu-id="01924-151">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





