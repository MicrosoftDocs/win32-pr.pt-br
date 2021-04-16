---
title: Método IWMPStringCollection2 getItemInfobyType
description: O método getItemInfoByType retorna o valor correspondente ao índice, nome, idioma e índice de atributo do item de coleção de cadeia de caracteres especificado.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- método getItemInfobyType Windows Media Player
- método getItemInfobyType Windows Media Player, interface IWMPStringCollection2
- Interface IWMPStringCollection2 Windows Media Player, método getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e227d6471ecf41c8f48420ded61c6f4e7eaac8cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765276"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a><span data-ttu-id="ee123-106">Método IWMPStringCollection2:: getItemInfobyType</span><span class="sxs-lookup"><span data-stu-id="ee123-106">IWMPStringCollection2::getItemInfobyType method</span></span>

<span data-ttu-id="ee123-107">O método **getItemInfoByType** retorna o valor correspondente ao índice, nome, idioma e índice de atributo do item de coleção de cadeia de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="ee123-107">The **getItemInfoByType** method returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee123-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee123-108">Syntax</span></span>


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a><span data-ttu-id="ee123-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee123-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee123-110">*lCollectionIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee123-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee123-111">O **System. Int32** que é o índice de base zero do item de coleção de cadeia de caracteres a partir do qual obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="ee123-111">The **System.Int32** that is the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ee123-112">*bstrtype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee123-112">*bstrType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee123-113">O **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="ee123-113">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="ee123-114">*bstrLanguage* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee123-114">*bstrLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee123-115">O **System. String** que indica o idioma.</span><span class="sxs-lookup"><span data-stu-id="ee123-115">The **System.String** that indicates the language.</span></span> <span data-ttu-id="ee123-116">Se o valor for definido como NULL ou para uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada.</span><span class="sxs-lookup"><span data-stu-id="ee123-116">If the value is set to null or to a zero-length string (""), the current locale string is used.</span></span> <span data-ttu-id="ee123-117">Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="ee123-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="ee123-118">*lAttributeIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee123-118">*lAttributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee123-119">Um **System. Int32** que é o índice de base zero do atributo.</span><span class="sxs-lookup"><span data-stu-id="ee123-119">A **System.Int32** that is the zero-based index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee123-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee123-120">Return value</span></span>

<span data-ttu-id="ee123-121">Um **System. Object** que é o item de coleção de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ee123-121">A **System.Object** that is the string collection item.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee123-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee123-122">Remarks</span></span>

<span data-ttu-id="ee123-123">Esse método dá suporte a atributos com vários valores e atributos com valores complexos.</span><span class="sxs-lookup"><span data-stu-id="ee123-123">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="ee123-124">O método **getItemInfo** não oferece suporte a atributos com vários valores ou atributos com valores complexos.</span><span class="sxs-lookup"><span data-stu-id="ee123-124">The **getItemInfo** method does not support attributes with multiple values or attributes with complex values.</span></span>

<span data-ttu-id="ee123-125">Ao passar o valor "childList" no parâmetro *bstrtype* , você pode recuperar uma nova coleção de cadeias de caracteres que contém os filhos de um dos itens na coleção de cadeias de caracteres pai.</span><span class="sxs-lookup"><span data-stu-id="ee123-125">By passing the value "ChildList" in the *bstrType* parameter, you can retrieve a new string collection that contains the children of one of the items in the parent string collection.</span></span> <span data-ttu-id="ee123-126">Por exemplo, se a coleção pai contiver uma lista de AlbumIDs, você poderá usar esse método para obter uma coleção de cadeia de caracteres filho que contém todas as faixas de um dos álbuns.</span><span class="sxs-lookup"><span data-stu-id="ee123-126">For instance, if the parent collection contains a list of AlbumIDs, you can use this method to obtain a child string collection that contains all the tracks for one of the albums.</span></span> <span data-ttu-id="ee123-127">Essa abordagem é mais rápida e mais eficiente do que chamar o método **IWMPMediaCollection2. getStringCollectionByQuery** duas vezes; uma vez para obter uma coleção de AlbumIDs e uma segunda vez para obter uma coleção de faixas para um albumid específico.</span><span class="sxs-lookup"><span data-stu-id="ee123-127">This approach is faster and more efficient than calling the **IWMPMediaCollection2.getStringCollectionByQuery** method twice; once to get a collection of AlbumIDs, and a second time to get a collection of tracks for a particular AlbumID.</span></span> <span data-ttu-id="ee123-128">Para usar filha na maneira descrita anteriormente, a coleção de cadeias de caracteres pai deve ser Obtida de uma coleção de mídia por meio de **IWMPLibraryServices**, e não usando a propriedade **AxWindowsMediaPlayer. mediacollection** .</span><span class="sxs-lookup"><span data-stu-id="ee123-128">To use ChildList in the way just described, the parent string collection must be obtained from a media collection through **IWMPLibraryServices**, and not by using the **AxWindowsMediaPlayer.mediaCollection** property.</span></span>

<span data-ttu-id="ee123-129">Ao usar Filhalist, passe o valor "childList" no parâmetro *bstrtype* e o valor 0 no parâmetro *lAttributeIndex* .</span><span class="sxs-lookup"><span data-stu-id="ee123-129">When using ChildList, pass the value "ChildList" in the *bstrType* parameter, and the value 0 in the *lAttributeIndex* parameter.</span></span> <span data-ttu-id="ee123-130">Em seguida, você pode converter o objeto que é retornado para uma interface **IWMPStringCollection2** para acessar a lista filho.</span><span class="sxs-lookup"><span data-stu-id="ee123-130">You can then cast the object that is returned to an **IWMPStringCollection2** interface to access the child list.</span></span>

<span data-ttu-id="ee123-131">Para usar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ee123-131">To use this method, you must have read access to the library.</span></span> <span data-ttu-id="ee123-132">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ee123-132">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee123-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee123-133">Requirements</span></span>



| <span data-ttu-id="ee123-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee123-134">Requirement</span></span> | <span data-ttu-id="ee123-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ee123-135">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee123-136">Versão</span><span class="sxs-lookup"><span data-stu-id="ee123-136">Version</span></span><br/>   | <span data-ttu-id="ee123-137">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ee123-137">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="ee123-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee123-138">Namespace</span></span><br/> | <span data-ttu-id="ee123-139">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ee123-139">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ee123-140">Assembly</span><span class="sxs-lookup"><span data-stu-id="ee123-140">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ee123-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ee123-141"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee123-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee123-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee123-143">**Atributo albumid**</span><span class="sxs-lookup"><span data-stu-id="ee123-143">**AlbumID Attribute**</span></span>](albumid-attribute.md)
</dt> <dt>

[<span data-ttu-id="ee123-144">**Interface IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee123-144">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee123-145">**IWMPMediaCollection2. getStringCollectionByQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee123-145">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee123-146">**Interface IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="ee123-146">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee123-147">**IWMPStringCollection2. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ee123-147">**IWMPStringCollection2.getItemInfo (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





