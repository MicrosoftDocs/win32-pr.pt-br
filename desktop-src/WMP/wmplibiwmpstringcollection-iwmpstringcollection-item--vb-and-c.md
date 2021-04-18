---
title: Método de item IWMPStringCollection
description: O método Item retorna a cadeia de caracteres no índice especificado.
ms.assetid: 77546cb2-eda5-4bb8-97b9-55270461815f
keywords:
- Método de item Windows Media Player
- Método de item Windows Media Player, interface IWMPStringCollection
- Interface IWMPStringCollection do Windows Media Player, método de item
topic_type:
- apiref
api_name:
- IWMPStringCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69bdc63448699a595238b9907f4b1253209ad06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784675"
---
# <a name="iwmpstringcollectionitem-method"></a><span data-ttu-id="ae25e-106">Método IWMPStringCollection:: item</span><span class="sxs-lookup"><span data-stu-id="ae25e-106">IWMPStringCollection::Item method</span></span>

<span data-ttu-id="ae25e-107">O método **Item** retorna a cadeia de caracteres no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="ae25e-107">The **Item** method returns the string at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae25e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae25e-108">Syntax</span></span>


```CSharp
public System.String Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPStringCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="ae25e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae25e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae25e-110">*Lindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae25e-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae25e-111">Um **System. Int32** que é o índice.</span><span class="sxs-lookup"><span data-stu-id="ae25e-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae25e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae25e-112">Return value</span></span>

<span data-ttu-id="ae25e-113">Um **System. String** que é a cadeia de caracteres no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="ae25e-113">A **System.String** that is the string at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae25e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae25e-114">Remarks</span></span>

<span data-ttu-id="ae25e-115">A interface **IWMPStringCollection** é usada para recuperar o conjunto de valores disponíveis para um atributo.</span><span class="sxs-lookup"><span data-stu-id="ae25e-115">The **IWMPStringCollection** interface is used to retrieve the set of values available for an attribute.</span></span> <span data-ttu-id="ae25e-116">Por exemplo, o método **IWMPMediaCollection. getAttributeStringCollection** pode ser usado para recuperar uma interface **IWMPStringCollection** representando todos os valores para o atributo gênero dentro do tipo de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="ae25e-116">For example, the **IWMPMediaCollection.getAttributeStringCollection** method can be used to retrieve an **IWMPStringCollection** interface representing all the values for the Genre attribute within the Audio media type.</span></span> <span data-ttu-id="ae25e-117">O método **Item** pode então ser usado para iterar por todos os valores possíveis para o atributo gênero.</span><span class="sxs-lookup"><span data-stu-id="ae25e-117">The **Item** method can then be used to iterate through all of the possible values for the Genre attribute.</span></span>

<span data-ttu-id="ae25e-118">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ae25e-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="ae25e-119">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ae25e-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae25e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae25e-120">Requirements</span></span>



| <span data-ttu-id="ae25e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae25e-121">Requirement</span></span> | <span data-ttu-id="ae25e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ae25e-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae25e-123">Versão</span><span class="sxs-lookup"><span data-stu-id="ae25e-123">Version</span></span><br/>   | <span data-ttu-id="ae25e-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="ae25e-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ae25e-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae25e-125">Namespace</span></span><br/> | <span data-ttu-id="ae25e-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ae25e-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ae25e-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="ae25e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ae25e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ae25e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae25e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae25e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae25e-130">**IWMPMediaCollection. getAttributeStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ae25e-130">**IWMPMediaCollection.getAttributeStringCollection (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ae25e-131">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ae25e-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ae25e-132">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ae25e-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ae25e-133">**Interface IWMPStringCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ae25e-133">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





