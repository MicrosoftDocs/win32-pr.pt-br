---
title: Método IWMPMedia getItemInfo
description: O método getItemInfo retorna o valor do atributo especificado para o item de mídia.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757058"
---
# <a name="iwmpmediagetiteminfo-method"></a><span data-ttu-id="ffee5-106">Método IWMPMedia:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="ffee5-106">IWMPMedia::getItemInfo method</span></span>

<span data-ttu-id="ffee5-107">O método **getItemInfo** retorna o valor do atributo especificado para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="ffee5-107">The **getItemInfo** method returns the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffee5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ffee5-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="ffee5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ffee5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffee5-110">*bstrItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ffee5-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-111">Um **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="ffee5-111">A **System.String** that is the name of the attribute.</span></span> <span data-ttu-id="ffee5-112">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-112">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffee5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ffee5-113">Return value</span></span>

<span data-ttu-id="ffee5-114">Um **System. String** que é o valor do atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="ffee5-114">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffee5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffee5-115">Remarks</span></span>

<span data-ttu-id="ffee5-116">Esse método retorna os metadados para um item de mídia individual ou um item de mídia que faz parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="ffee5-116">This method returns the metadata for an individual media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="ffee5-117">A propriedade **attributeCount** Obtém o número de nomes de atributo disponíveis para um determinado item de mídia.</span><span class="sxs-lookup"><span data-stu-id="ffee5-117">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="ffee5-118">Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível.</span><span class="sxs-lookup"><span data-stu-id="ffee5-118">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="ffee5-119">Nomes de atributo individuais podem ser passados para **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="ffee5-119">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="ffee5-120">Para recuperar atributos com vários valores e atributos com valores complexos, use o método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="ffee5-120">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="ffee5-121">Se o item de mídia vier de uma biblioteca que foi recuperada chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o conjunto de atributos disponíveis será diferente daqueles que podem ser consultados a partir da biblioteca local recuperada chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-121">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="ffee5-122">Por exemplo, os atributos disponíveis da biblioteca local recuperados usando **IWMPLibrary** serão um subconjunto dos atributos disponíveis na biblioteca local recuperada usando **IWMPCore**.</span><span class="sxs-lookup"><span data-stu-id="ffee5-122">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **IWMPCore**.</span></span> <span data-ttu-id="ffee5-123">O conjunto de atributos disponíveis de outras fontes (bibliotecas remotas, dispositivos portáteis ou CDs) é definido pelas outras fontes.</span><span class="sxs-lookup"><span data-stu-id="ffee5-123">The set of attributes available from other sources (remote libraries, portable devices, or CDs) is defined by the other sources.</span></span>

<span data-ttu-id="ffee5-124">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ffee5-124">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ffee5-125">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-125">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffee5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffee5-126">Requirements</span></span>



| <span data-ttu-id="ffee5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffee5-127">Requirement</span></span> | <span data-ttu-id="ffee5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ffee5-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffee5-129">Versão</span><span class="sxs-lookup"><span data-stu-id="ffee5-129">Version</span></span><br/>   | <span data-ttu-id="ffee5-130">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ffee5-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ffee5-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="ffee5-131">Namespace</span></span><br/> | <span data-ttu-id="ffee5-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ffee5-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ffee5-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="ffee5-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ffee5-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ffee5-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffee5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ffee5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffee5-136">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="ffee5-136">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="ffee5-137">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ffee5-137">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ffee5-138">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ffee5-138">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ffee5-139">**IWMPMedia. GetAttributeName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ffee5-139">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ffee5-140">**IWMPMedia. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ffee5-140">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ffee5-141">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ffee5-141">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





