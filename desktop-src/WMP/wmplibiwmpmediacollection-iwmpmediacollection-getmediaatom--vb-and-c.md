---
title: Método IWMPMediaCollection getMediaAtom
description: O método getMediaAtom retorna o índice de um atributo especificado dentro do conjunto de atributos disponíveis.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- método getMediaAtom Windows Media Player
- método getMediaAtom Windows Media Player, interface IWMPMediaCollection
- Interface IWMPMediaCollection Windows Media Player, método getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783803"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a><span data-ttu-id="6e9cd-106">Método IWMPMediaCollection:: getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="6e9cd-106">IWMPMediaCollection::getMediaAtom method</span></span>

<span data-ttu-id="6e9cd-107">O `getMediaAtom` método retorna o índice de um atributo especificado dentro do conjunto de atributos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6e9cd-107">The `getMediaAtom` method returns the index of a specified attribute within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9cd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e9cd-108">Syntax</span></span>


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a><span data-ttu-id="6e9cd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e9cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e9cd-110">*bstrItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e9cd-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e9cd-111">O **System. String** que é o nome do item para o qual o índice deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6e9cd-111">The **System.String** that is the name of the item for which the index should be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e9cd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e9cd-112">Return value</span></span>

<span data-ttu-id="6e9cd-113">O **System. Int32** que é o índice.</span><span class="sxs-lookup"><span data-stu-id="6e9cd-113">The **System.Int32** that is the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e9cd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e9cd-114">Remarks</span></span>

<span data-ttu-id="6e9cd-115">O número de índice recuperado com esse método pode ser passado para o **IWMPMedia. getItemInfoByAtom** para acessar valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="6e9cd-115">The index number retrieved with this method can be passed to the **IWMPMedia.getItemInfoByAtom** to access attribute values.</span></span> <span data-ttu-id="6e9cd-116">Essa técnica é geralmente mais eficiente ao trabalhar com listas de reprodução grandes do que acessar um valor de atributo pelo nome por meio de **IWMPMedia. getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="6e9cd-116">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through **IWMPMedia.getItemInfo**.</span></span>

<span data-ttu-id="6e9cd-117">Antes de chamar esse método, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6e9cd-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="6e9cd-118">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6e9cd-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e9cd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e9cd-119">Requirements</span></span>



| <span data-ttu-id="6e9cd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e9cd-120">Requirement</span></span> | <span data-ttu-id="6e9cd-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6e9cd-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9cd-122">Versão</span><span class="sxs-lookup"><span data-stu-id="6e9cd-122">Version</span></span><br/>   | <span data-ttu-id="6e9cd-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="6e9cd-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6e9cd-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="6e9cd-124">Namespace</span></span><br/> | <span data-ttu-id="6e9cd-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6e9cd-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6e9cd-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="6e9cd-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6e9cd-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6e9cd-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e9cd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e9cd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9cd-129">**IWMPMedia. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6e9cd-129">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6e9cd-130">**IWMPMedia. getItemInfoByAtom (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6e9cd-130">**IWMPMedia.getItemInfoByAtom (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6e9cd-131">**Interface IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="6e9cd-131">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





