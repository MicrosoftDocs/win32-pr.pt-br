---
title: Método IWMPMedia getItemInfoByAtom
description: O método getItemInfoByAtom retorna o valor do atributo com o número de índice especificado.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- método getItemInfoByAtom Windows Media Player
- método getItemInfoByAtom Windows Media Player, interface IWMPMedia
- Interface IWMPMedia Windows Media Player, método getItemInfoByAtom
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750734"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a><span data-ttu-id="e4d9c-106">Método IWMPMedia:: getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="e4d9c-106">IWMPMedia::getItemInfoByAtom method</span></span>

<span data-ttu-id="e4d9c-107">O método **getItemInfoByAtom** retorna o valor do atributo com o número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-107">The **getItemInfoByAtom** method returns the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d9c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4d9c-108">Syntax</span></span>


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a><span data-ttu-id="e4d9c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4d9c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d9c-110">*lAtom* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4d9c-110">*lAtom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d9c-111">Um **System. Int32** que especifica o índice no qual o atributo solicitado reside no conjunto de atributos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-111">A **System.Int32** that specifies the index at which the requested attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d9c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4d9c-112">Return value</span></span>

<span data-ttu-id="e4d9c-113">Um **System. String** que é o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-113">A **System.String** that is the value of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4d9c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4d9c-114">Remarks</span></span>

<span data-ttu-id="e4d9c-115">Esse método pode ser usado para recuperar metadados para um item de mídia específico usando um número de índice de atributo.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-115">This method can be used to retrieve metadata for a specific media item by using an attribute index number.</span></span> <span data-ttu-id="e4d9c-116">A propriedade **attributeCount** pode ser usada para determinar o número de atributos disponíveis para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-116">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="e4d9c-117">O método **getMediaAtom** da interface **IWMPMediaCollection** também pode ser usado para recuperar o índice de um atributo específico.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-117">The **getMediaAtom** method of the **IWMPMediaCollection** interface can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="e4d9c-118">Essa técnica geralmente é mais eficiente do que os métodos **getItemInfo** ou **getItemInfoByType** ao trabalhar com listas de reprodução grandes.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-118">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="e4d9c-119">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e4d9c-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="e4d9c-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e4d9c-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d9c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4d9c-121">Requirements</span></span>



| <span data-ttu-id="e4d9c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4d9c-122">Requirement</span></span> | <span data-ttu-id="e4d9c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e4d9c-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d9c-124">Versão</span><span class="sxs-lookup"><span data-stu-id="e4d9c-124">Version</span></span><br/>   | <span data-ttu-id="e4d9c-125">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="e4d9c-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e4d9c-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4d9c-126">Namespace</span></span><br/> | <span data-ttu-id="e4d9c-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e4d9c-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e4d9c-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="e4d9c-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e4d9c-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e4d9c-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d9c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4d9c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d9c-131">**Interface IWMPMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4d9c-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4d9c-132">**IWMPMedia. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4d9c-132">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4d9c-133">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4d9c-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4d9c-134">**IWMPMedia. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4d9c-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4d9c-135">**IWMPMedia3. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4d9c-135">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e4d9c-136">**IWMPMediaCollection. getMediaAtom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="e4d9c-136">**IWMPMediaCollection.getMediaAtom (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





