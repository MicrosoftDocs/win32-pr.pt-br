---
title: IWMPPlaylist. attributeName (VB e C)
description: A propriedade attributeName (o \_ método Get AttributeName em C \) Obtém o nome de um atributo de playlist especificado por um índice.
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761438"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a><span data-ttu-id="8c934-104">IWMPPlaylist. attributeName (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="8c934-104">IWMPPlaylist.attributeName (VB and C#)</span></span>

<span data-ttu-id="8c934-105">A propriedade **AttributeName** (o método **Get \_ AttributeName** em C#) Obtém o nome de um atributo playlist especificado por um índice.</span><span class="sxs-lookup"><span data-stu-id="8c934-105">The **attributeName** property (the **get\_attributeName** method in C#) gets the name of a playlist attribute specified by an index.</span></span>


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a><span data-ttu-id="8c934-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c934-106">Parameters</span></span>

<span data-ttu-id="8c934-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="8c934-107">*lIndex*</span></span>

<span data-ttu-id="8c934-108">Um **System. Int32** que é o índice do atributo playlist.</span><span class="sxs-lookup"><span data-stu-id="8c934-108">A **System.Int32** that is the index of the playlist attribute.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c934-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8c934-109">Return Value</span></span>

<span data-ttu-id="8c934-110">Um **System. String** que é o nome do atributo playlist.</span><span class="sxs-lookup"><span data-stu-id="8c934-110">A **System.String** that is the name of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c934-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c934-111">Remarks</span></span>

<span data-ttu-id="8c934-112">**IWMPPlaylist. AttributeName** é uma propriedade somente leitura no Visual Basic que usa um parâmetro, enquanto em C# ele é referido como o método **IWMPPlaylist. get \_ AttributeName** .</span><span class="sxs-lookup"><span data-stu-id="8c934-112">**IWMPPlaylist.attributeName** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_attributeName** method.</span></span>

<span data-ttu-id="8c934-113">O número de atributos associados a uma playlist é retornado pela propriedade **IWMPPlaylist. attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="8c934-113">The number of attributes associated with a playlist is returned by the **IWMPPlaylist.attributeCount** property.</span></span>

<span data-ttu-id="8c934-114">O nome retornado por essa propriedade pode ser fornecido para os métodos **setItemInfo** ou **getItemInfo** para especificar ou recuperar um valor para o atributo nomeado.</span><span class="sxs-lookup"><span data-stu-id="8c934-114">The name returned by this property can be supplied to the **setItemInfo** or **getItemInfo** methods to specify or retrieve a value for the named attribute.</span></span>

<span data-ttu-id="8c934-115">Antes de usar essa propriedade, você deve ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8c934-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="8c934-116">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8c934-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="8c934-117">Para obter mais informações sobre atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8c934-117">For more information about attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8c934-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c934-118">Examples</span></span>

<span data-ttu-id="8c934-119">Consulte a propriedade [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obter o código de exemplo que usa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8c934-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c934-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c934-120">Requirements</span></span>



| <span data-ttu-id="8c934-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c934-121">Requirement</span></span> | <span data-ttu-id="8c934-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8c934-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c934-123">Versão</span><span class="sxs-lookup"><span data-stu-id="8c934-123">Version</span></span><br/>   | <span data-ttu-id="8c934-124">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="8c934-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8c934-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c934-125">Namespace</span></span><br/> | <span data-ttu-id="8c934-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8c934-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8c934-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="8c934-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8c934-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8c934-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c934-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c934-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c934-130">**Interface IWMPPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c934-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c934-131">**IWMPPlaylist. attributeCount (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c934-131">**IWMPPlaylist.attributeCount (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c934-132">**IWMPPlaylist. getItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c934-132">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8c934-133">**IWMPPlaylist. setItemInfo (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8c934-133">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





