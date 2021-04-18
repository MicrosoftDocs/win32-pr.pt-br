---
title: Método Media. getItemInfoByType
description: O método getItemInfoByType recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- método getItemInfoByType Windows Media Player
- método getItemInfoByType Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813477"
---
# <a name="mediagetiteminfobytype-method"></a><span data-ttu-id="b2571-106">Método Media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="b2571-106">Media.getItemInfoByType method</span></span>

<span data-ttu-id="b2571-107">O método **getItemInfoByType** recupera o valor do atributo correspondente ao nome do atributo, idioma e índice especificados.</span><span class="sxs-lookup"><span data-stu-id="b2571-107">The **getItemInfoByType** method retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2571-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2571-108">Syntax</span></span>


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a><span data-ttu-id="b2571-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2571-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2571-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b2571-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2571-111">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="b2571-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="b2571-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b2571-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2571-113">*idioma* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b2571-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2571-114">**Cadeia de caracteres** que representa o idioma.</span><span class="sxs-lookup"><span data-stu-id="b2571-114">**String** representing the language.</span></span> <span data-ttu-id="b2571-115">Se o valor for definido como nulo ou "" (cadeia de caracteres vazia), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="b2571-115">If the value is set to null or "" (empty string) the current locale string is used.</span></span> <span data-ttu-id="b2571-116">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="b2571-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="b2571-117">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b2571-117">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2571-118">**Número** (**longo**) que contém o índice de base zero do valor a ser recuperado do atributo.</span><span class="sxs-lookup"><span data-stu-id="b2571-118">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2571-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2571-119">Return value</span></span>

<span data-ttu-id="b2571-120">Esse método retorna um **número**, uma **cadeia de caracteres**, um objeto **MetadataPicture** ou um objeto **MetadataText** , conforme indicado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b2571-120">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="b2571-121">Atributo</span><span class="sxs-lookup"><span data-stu-id="b2571-121">Attribute</span></span>                   | <span data-ttu-id="b2571-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2571-122">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="b2571-123">**Sincronizarstate**</span><span class="sxs-lookup"><span data-stu-id="b2571-123">**SyncState**</span></span>               | <span data-ttu-id="b2571-124">**Número** (**longo sem sinal**)</span><span class="sxs-lookup"><span data-stu-id="b2571-124">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="b2571-125">**WM/letras de música \_ sincronizadas**</span><span class="sxs-lookup"><span data-stu-id="b2571-125">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="b2571-126">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="b2571-126">**MetadataText** object</span></span>        |
| <span data-ttu-id="b2571-127">**WM/imagem**</span><span class="sxs-lookup"><span data-stu-id="b2571-127">**WM/Picture**</span></span>              | <span data-ttu-id="b2571-128">Objeto **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="b2571-128">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="b2571-129">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="b2571-129">**WM/UserWebURL**</span></span>           | <span data-ttu-id="b2571-130">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="b2571-130">**MetadataText** object</span></span>        |
| <span data-ttu-id="b2571-131">Todos os outros atributos</span><span class="sxs-lookup"><span data-stu-id="b2571-131">All other attributes</span></span>        | <span data-ttu-id="b2571-132">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b2571-132">**String**</span></span>                     |



 

<span data-ttu-id="b2571-133">Para atributos cujo valor subjacente é **booliano**, esse método retorna a cadeia de caracteres "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="b2571-133">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="b2571-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2571-134">Remarks</span></span>

<span data-ttu-id="b2571-135">Esse método recupera os metadados de um item de mídia digital individual ou um item de mídia que faz parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b2571-135">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="b2571-136">Esse método dá suporte a atributos com vários valores e atributos com valores complexos.</span><span class="sxs-lookup"><span data-stu-id="b2571-136">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="b2571-137">O método **getItemInfo** não oferece suporte a atributos com vários valores e atributos com valores complexos.</span><span class="sxs-lookup"><span data-stu-id="b2571-137">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="b2571-138">A propriedade **attributeCount** contém o número de nomes de atributo disponíveis para um determinado objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="b2571-138">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="b2571-139">Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível.</span><span class="sxs-lookup"><span data-stu-id="b2571-139">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="b2571-140">Nomes de atributo individuais podem ser passados para o parâmetro *Name* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="b2571-140">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="b2571-141">O método **getAttributeCountByType** retorna o número de atributos que correspondem a um determinado nome de atributo para um determinado objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="b2571-141">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="b2571-142">Os números de índice podem então ser passados para o parâmetro de *índice* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="b2571-142">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="b2571-143">Isso é útil quando um item de mídia digital é categorizado em vários gêneros, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="b2571-143">This is useful when a digital media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="b2571-144">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b2571-144">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b2571-145">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b2571-145">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b2571-146">Esse método pode causar erros.</span><span class="sxs-lookup"><span data-stu-id="b2571-146">This method can cause errors.</span></span> <span data-ttu-id="b2571-147">Você deve incluir o código de tratamento de erros ao chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b2571-147">You should include error-handling code when you call this method.</span></span> <span data-ttu-id="b2571-148">Por exemplo, no JScript, você pode implementar o tratamento de erros usando a **tentativa... capturar... Por fim,** estrutura.</span><span class="sxs-lookup"><span data-stu-id="b2571-148">For example, in JScript you can implement error handling by using the **try...catch...finally** structure.</span></span>

<span data-ttu-id="b2571-149">**Windows Media Player 10 Mobile:** Não há suporte para esse método.</span><span class="sxs-lookup"><span data-stu-id="b2571-149">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2571-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2571-150">Requirements</span></span>



| <span data-ttu-id="b2571-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2571-151">Requirement</span></span> | <span data-ttu-id="b2571-152">Valor</span><span class="sxs-lookup"><span data-stu-id="b2571-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2571-153">Versão</span><span class="sxs-lookup"><span data-stu-id="b2571-153">Version</span></span><br/> | <span data-ttu-id="b2571-154">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b2571-154">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b2571-155">DLL</span><span class="sxs-lookup"><span data-stu-id="b2571-155">DLL</span></span><br/>     | <dl> <span data-ttu-id="b2571-156"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2571-156"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2571-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2571-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2571-158">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="b2571-158">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b2571-159">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="b2571-159">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="b2571-160">**Media. getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="b2571-160">**Media.getAttributeCountByType**</span></span>](media-getattributecountbytype.md)
</dt> <dt>

[<span data-ttu-id="b2571-161">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="b2571-161">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="b2571-162">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b2571-162">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b2571-163">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b2571-163">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b2571-164">**Objeto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="b2571-164">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="b2571-165">**Objeto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="b2571-165">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="b2571-166">**Lendo valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="b2571-166">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="b2571-167">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b2571-167">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b2571-168">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b2571-168">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





