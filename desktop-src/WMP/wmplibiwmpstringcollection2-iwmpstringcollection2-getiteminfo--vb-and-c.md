---
title: Método IWMPStringCollection2 getItemInfo
description: O método getItemInfo retorna a cadeia de caracteres correspondente ao índice e nome do item de coleção de cadeia de caracteres especificado.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, interface IWMPStringCollection2
- Interface IWMPStringCollection2 Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4741c4a3ba74b03038974d8b66bc42c23830ebb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765767"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a><span data-ttu-id="a8fae-106">Método IWMPStringCollection2:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="a8fae-106">IWMPStringCollection2::getItemInfo method</span></span>

<span data-ttu-id="a8fae-107">O método **getItemInfo** retorna a cadeia de caracteres correspondente ao índice e nome do item de coleção de cadeia de caracteres especificado.</span><span class="sxs-lookup"><span data-stu-id="a8fae-107">The **getItemInfo** method returns the string corresponding to the specified string collection item index and name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8fae-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8fae-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="a8fae-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8fae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8fae-110">*lCollectionIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8fae-110">*lCollectionIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8fae-111">O **System. Int32** que especifica o índice de base zero do item de coleção de cadeia de caracteres a partir do qual obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="a8fae-111">The **System.Int32** specifying the zero-based index of the string collection item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="a8fae-112">*bstrItemName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8fae-112">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8fae-113">O **System. String** que é o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="a8fae-113">The **System.String** that is the attribute name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8fae-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8fae-114">Return value</span></span>

<span data-ttu-id="a8fae-115">O **System. String** que é o nome do item de coleção de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a8fae-115">The **System.String** that is the name of the string collection item.</span></span> <span data-ttu-id="a8fae-116">Para atributos cujo valor subjacente é **System. Boolean**, ele retorna a cadeia de caracteres "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="a8fae-116">For attributes whose underlying value is **System.Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="a8fae-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8fae-117">Remarks</span></span>

<span data-ttu-id="a8fae-118">Para recuperar atributos com vários valores e atributos com valores complexos, use o método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="a8fae-118">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="a8fae-119">Para usar esse método, é necessário ter acesso de leitura à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a8fae-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a8fae-120">Para obter mais informações, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a8fae-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8fae-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8fae-121">Requirements</span></span>



| <span data-ttu-id="a8fae-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8fae-122">Requirement</span></span> | <span data-ttu-id="a8fae-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a8fae-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fae-124">Versão</span><span class="sxs-lookup"><span data-stu-id="a8fae-124">Version</span></span><br/>   | <span data-ttu-id="a8fae-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="a8fae-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="a8fae-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8fae-126">Namespace</span></span><br/> | <span data-ttu-id="a8fae-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a8fae-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a8fae-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="a8fae-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a8fae-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a8fae-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8fae-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8fae-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fae-131">**Interface IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="a8fae-131">**IWMPStringCollection2 Interface**</span></span>](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8fae-132">**IWMPStringCollection2. getItemInfoByType (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="a8fae-132">**IWMPStringCollection2.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





