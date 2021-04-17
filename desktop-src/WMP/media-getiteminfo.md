---
title: Método Media. getItemInfo
description: O método getItemInfo recupera o valor do atributo especificado para o item de mídia atual.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763472"
---
# <a name="mediagetiteminfo-method"></a><span data-ttu-id="22214-106">Método Media. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="22214-106">Media.getItemInfo method</span></span>

<span data-ttu-id="22214-107">O método **getItemInfo** recupera o valor do atributo especificado para o item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="22214-107">The **getItemInfo** method retrieves the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="22214-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22214-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="22214-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22214-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22214-110">*nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="22214-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22214-111">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="22214-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="22214-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="22214-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22214-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22214-113">Return value</span></span>

<span data-ttu-id="22214-114">Esse método retorna uma **cadeia de caracteres** que representa o valor do atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="22214-114">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="22214-115">Para atributos cujo valor subjacente é **booliano**, ele retorna a cadeia de caracteres "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="22214-115">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="22214-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="22214-116">Remarks</span></span>

<span data-ttu-id="22214-117">Esse método recupera os metadados de um item de mídia digital individual ou um item de mídia que faz parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="22214-117">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="22214-118">A propriedade **attributeCount** contém o número de nomes de atributo disponíveis para um determinado objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="22214-118">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="22214-119">Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível.</span><span class="sxs-lookup"><span data-stu-id="22214-119">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="22214-120">Nomes de atributo individuais podem ser passados para **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="22214-120">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="22214-121">Para recuperar atributos com vários valores e atributos com valores complexos, use o método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="22214-121">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="22214-122">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="22214-122">To use this method, read access to the library is required.</span></span> <span data-ttu-id="22214-123">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="22214-123">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="22214-124">Para compartilhar as bibliotecas de mídia do Windows por UPnP, o Windows Media Player cria um serviço de diretório de conteúdo (CDS) que é exposto por UPnP.</span><span class="sxs-lookup"><span data-stu-id="22214-124">To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that is exposed over UPnP.</span></span> <span data-ttu-id="22214-125">Outros dispositivos podem, então, navegar e navegar pelas bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="22214-125">Other devices can then navigate and browse the libraries.</span></span>

<span data-ttu-id="22214-126">No Windows 7, um aplicativo pode usar os atributos Windows Media Player [**TrackingID**](trackingid-attribute.md) e [**MediaType**](mediatype-attribute.md) para construir a ID de objeto de cada item no CDs.</span><span class="sxs-lookup"><span data-stu-id="22214-126">In Windows 7, an application can use the Windows Media Player [**TrackingID**](trackingid-attribute.md) and [**MediaType**](mediatype-attribute.md) attributes to construct the object ID of each item in the CDS.</span></span> <span data-ttu-id="22214-127">Observe que essa construção pode mudar em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="22214-127">Note that this construction might change in future versions of Windows.</span></span> <span data-ttu-id="22214-128">O aplicativo passa cada uma dessas cadeias de caracteres de atributo no parâmetro *Name* em uma chamada para **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="22214-128">The application passes each of these attribute strings in the *name* parameter in a call to **getItemInfo**.</span></span> <span data-ttu-id="22214-129">**getItemInfo** retorna o valor para cada atributo no valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="22214-129">**getItemInfo** returns the value for each attribute in the return value.</span></span> <span data-ttu-id="22214-130">O aplicativo usa a seguinte sintaxe para construir cada ID de objeto:</span><span class="sxs-lookup"><span data-stu-id="22214-130">The application then uses the following syntax to construct each object ID:</span></span>

<span data-ttu-id="22214-131">*TrackingID*. 0. *Mediatypeid*</span><span class="sxs-lookup"><span data-stu-id="22214-131">*TrackingID*.0.*MediaTypeID*</span></span>

<span data-ttu-id="22214-132">Essa sintaxe tem o seguinte significado:</span><span class="sxs-lookup"><span data-stu-id="22214-132">This syntax has the following meaning:</span></span>

-   <span data-ttu-id="22214-133">*TrackingID* é a cadeia de caracteres que é armazenada no atributo [**TrackingID**](trackingid-attribute.md) do Windows Media Player do item de mídia.</span><span class="sxs-lookup"><span data-stu-id="22214-133">*TrackingID* is the string that is stored in the Windows Media Player [**TrackingID**](trackingid-attribute.md) attribute of the media item.</span></span>
-   <span data-ttu-id="22214-134">*Mediatypeid* depende do valor do atributo [**MediaType**](mediatype-attribute.md) , conforme mostrado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="22214-134">*MediaTypeID* depends on the value of the [**MediaType**](mediatype-attribute.md) attribute, as shown in the following table:</span></span>

    | <span data-ttu-id="22214-135">Atributo MediaType</span><span class="sxs-lookup"><span data-stu-id="22214-135">MediaType attribute</span></span>                      | <span data-ttu-id="22214-136">MediaTypeid</span><span class="sxs-lookup"><span data-stu-id="22214-136">MediaTypeID</span></span> |
    |------------------------------------------|-------------|
    | [<span data-ttu-id="22214-137">Itens de áudio</span><span class="sxs-lookup"><span data-stu-id="22214-137">Audio Items</span></span>](audio-item-attributes.md) | <span data-ttu-id="22214-138">4</span><span class="sxs-lookup"><span data-stu-id="22214-138">4</span></span>           |
    | [<span data-ttu-id="22214-139">Itens de foto</span><span class="sxs-lookup"><span data-stu-id="22214-139">Photo Items</span></span>](photo-item-attributes.md) | <span data-ttu-id="22214-140">B</span><span class="sxs-lookup"><span data-stu-id="22214-140">B</span></span>           |
    | [<span data-ttu-id="22214-141">Itens de vídeo</span><span class="sxs-lookup"><span data-stu-id="22214-141">Video Items</span></span>](video-item-attributes.md) | <span data-ttu-id="22214-142">8</span><span class="sxs-lookup"><span data-stu-id="22214-142">8</span></span>           |

    

     

<span data-ttu-id="22214-143">**Windows Media Player 10 Mobile:** Os atributos de um item de mídia estão disponíveis somente durante a reprodução, a menos que sejam recuperados do item por meio da coleção de mídia.</span><span class="sxs-lookup"><span data-stu-id="22214-143">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="22214-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22214-144">Requirements</span></span>



| <span data-ttu-id="22214-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="22214-145">Requirement</span></span> | <span data-ttu-id="22214-146">Valor</span><span class="sxs-lookup"><span data-stu-id="22214-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22214-147">Versão</span><span class="sxs-lookup"><span data-stu-id="22214-147">Version</span></span><br/> | <span data-ttu-id="22214-148">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="22214-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="22214-149">DLL</span><span class="sxs-lookup"><span data-stu-id="22214-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="22214-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22214-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22214-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="22214-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22214-152">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="22214-152">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="22214-153">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="22214-153">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="22214-154">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="22214-154">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="22214-155">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="22214-155">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="22214-156">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="22214-156">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="22214-157">**Lendo valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="22214-157">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="22214-158">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="22214-158">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="22214-159">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="22214-159">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





