---
title: Método IWMPMedia3 getItemInfoByType
description: O método getItemInfoByType retorna o valor do atributo correspondente ao tipo de atributo e ao índice especificados.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- método getItemInfoByType Windows Media Player
- método getItemInfoByType Windows Media Player, interface IWMPMedia3
- Interface IWMPMedia3 Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768422"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a><span data-ttu-id="b6194-106">Método IWMPMedia3:: getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="b6194-106">IWMPMedia3::getItemInfoByType method</span></span>

<span data-ttu-id="b6194-107">O método **getItemInfoByType** retorna o valor do atributo correspondente ao tipo de atributo e ao índice especificados.</span><span class="sxs-lookup"><span data-stu-id="b6194-107">The **getItemInfoByType** method returns the value of the attribute corresponding to the specified attribute type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6194-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6194-108">Syntax</span></span>


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a><span data-ttu-id="b6194-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6194-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6194-110">*bstrtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6194-110">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6194-111">Um **System. String** que é o tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="b6194-111">A **System.String** that is the attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="b6194-112">*bstrLanguage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6194-112">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6194-113">Um **System. String** que é o idioma.</span><span class="sxs-lookup"><span data-stu-id="b6194-113">A **System.String** that is the language.</span></span> <span data-ttu-id="b6194-114">Se o valor for definido como NULL ou uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="b6194-114">If the value is set to null or a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="b6194-115">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="b6194-115">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="b6194-116">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6194-116">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6194-117">Um **System. Int32** que é o índice de atributo.</span><span class="sxs-lookup"><span data-stu-id="b6194-117">A **System.Int32** that is the attribute index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6194-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6194-118">Return value</span></span>

<span data-ttu-id="b6194-119">Um **System. Object** que é o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="b6194-119">A **System.Object** that is the value of the attribute.</span></span> <span data-ttu-id="b6194-120">O tipo para o qual converter este objeto depende do tipo do atributo.</span><span class="sxs-lookup"><span data-stu-id="b6194-120">The type to cast this object to depends on the type of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6194-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6194-121">Remarks</span></span>

<span data-ttu-id="b6194-122">Esse método retorna os metadados de um item de mídia digital individual ou um item de mídia que faz parte de uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b6194-122">This method returns the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="b6194-123">Esse método dá suporte a atributos com vários valores e atributos com valores complexos.</span><span class="sxs-lookup"><span data-stu-id="b6194-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="b6194-124">O método **getItemInfo** não oferece suporte a atributos com vários valores e atributos com valores complexos.</span><span class="sxs-lookup"><span data-stu-id="b6194-124">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="b6194-125">A propriedade **attributeCount** Obtém o número de nomes de atributo disponíveis para um determinado item de mídia.</span><span class="sxs-lookup"><span data-stu-id="b6194-125">The **attributeCount** property gets the number of attribute names available for a given media item.</span></span> <span data-ttu-id="b6194-126">Os números de índice podem ser usados com o método **GetAttributeName** para determinar o nome de cada atributo disponível.</span><span class="sxs-lookup"><span data-stu-id="b6194-126">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="b6194-127">Nomes de atributo individuais podem ser passados para o parâmetro *Name* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="b6194-127">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="b6194-128">O método **getAttributeCountByType** retorna o número de atributos que correspondem a um determinado nome de atributo para um determinado item de mídia.</span><span class="sxs-lookup"><span data-stu-id="b6194-128">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given media item.</span></span> <span data-ttu-id="b6194-129">Os números de índice podem então ser passados para o parâmetro de *índice* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="b6194-129">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="b6194-130">Isso é útil quando um item de mídia é categorizado em vários gêneros, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="b6194-130">This is useful when a media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="b6194-131">Se o item de mídia vier de uma biblioteca que foi recuperada chamando [IWMPLibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), o conjunto de atributos disponíveis será diferente daqueles que podem ser consultados a partir da biblioteca local recuperada chamando [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="b6194-131">If the media item came from a library that was retrieved by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), the set of available attributes will differ from those which can be queried from the local library retrieved by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md).</span></span> <span data-ttu-id="b6194-132">Por exemplo, os atributos disponíveis da biblioteca local recuperados usando **IWMPLibrary** serão um subconjunto dos atributos disponíveis na biblioteca local recuperada usando **AxWindowsMediaPlayer**.</span><span class="sxs-lookup"><span data-stu-id="b6194-132">For example, the attributes available from the local library retrieved by using **IWMPLibrary** will be a subset of the attributes available from the local library retrieved by using **AxWindowsMediaPlayer**.</span></span> <span data-ttu-id="b6194-133">O conjunto de atributos disponíveis de outras fontes (bibliotecas remotas, dispositivos portáteis ou CDs é definido pelas outras fontes.</span><span class="sxs-lookup"><span data-stu-id="b6194-133">The set of attributes available from other sources (remote libraries, portable devices, or CDs is defined by the other sources.</span></span>

<span data-ttu-id="b6194-134">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b6194-134">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b6194-135">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b6194-135">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6194-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6194-136">Requirements</span></span>



| <span data-ttu-id="b6194-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6194-137">Requirement</span></span> | <span data-ttu-id="b6194-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b6194-138">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6194-139">Versão</span><span class="sxs-lookup"><span data-stu-id="b6194-139">Version</span></span><br/>   | <span data-ttu-id="b6194-140">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b6194-140">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b6194-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="b6194-141">Namespace</span></span><br/> | <span data-ttu-id="b6194-142">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b6194-142">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b6194-143">Assembly</span><span class="sxs-lookup"><span data-stu-id="b6194-143">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6194-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b6194-144"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6194-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6194-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6194-146">**Interface IWMPMedia3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b6194-146">**IWMPMedia3 Interface (VB and C#)**</span></span>](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6194-147">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b6194-147">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6194-148">**IWMPMedia. GetAttributeName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b6194-148">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6194-149">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b6194-149">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b6194-150">**IWMPMedia3. getAttributeCountByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b6194-150">**IWMPMedia3.getAttributeCountByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





