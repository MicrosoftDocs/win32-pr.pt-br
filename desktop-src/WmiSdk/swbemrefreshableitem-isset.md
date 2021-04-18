---
description: A propriedade SWbemRefreshableItem. IsSet é um valor booliano que indica se o objeto SWbemRefreshableItem representa um único objeto ou um conjunto de objetos. O objeto SWbemRefreshableItem representa um único objeto ou um conjunto de objetos.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Propriedade SWbemRefreshableItem. IsSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105790537"
---
# <a name="swbemrefreshableitemisset-property"></a><span data-ttu-id="35490-103">Propriedade SWbemRefreshableItem. IsSet</span><span class="sxs-lookup"><span data-stu-id="35490-103">SWbemRefreshableItem.IsSet property</span></span>

<span data-ttu-id="35490-104">A propriedade **SWbemRefreshableItem. IsSet** é um valor booliano que indica se o objeto [**SWbemRefreshableItem**](swbemrefreshableitem.md) representa um único objeto ou um conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="35490-104">The **SWbemRefreshableItem.IsSet** property is a Boolean value that indicates whether the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object represents a single object or an object set.</span></span>

<span data-ttu-id="35490-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="35490-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="35490-106">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="35490-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="35490-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35490-107">Syntax</span></span>


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a><span data-ttu-id="35490-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35490-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="35490-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="35490-109">Remarks</span></span>

<span data-ttu-id="35490-110">Se **SWbemRefreshableItem. IsSet** for **true**, o item representará um objeto [**SWbemObjectSet**](swbemobjectset.md) e a propriedade [**Object**](swbemrefreshableitem-object.md) será **NULL**.</span><span class="sxs-lookup"><span data-stu-id="35490-110">If **SWbemRefreshableItem.IsSet** is **TRUE**, then the item represents an [**SWbemObjectSet**](swbemobjectset.md) object and the [**Object**](swbemrefreshableitem-object.md) property will be **NULL**.</span></span> <span data-ttu-id="35490-111">Se **for false**, o item representará um objeto [**SWbemObject**](swbemobject.md) e a propriedade **Object** será **nula**.</span><span class="sxs-lookup"><span data-stu-id="35490-111">If **FALSE**, the item represents an [**SWbemObject**](swbemobject.md) object and the **Object** property is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="35490-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35490-112">Requirements</span></span>



| <span data-ttu-id="35490-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="35490-113">Requirement</span></span> | <span data-ttu-id="35490-114">Valor</span><span class="sxs-lookup"><span data-stu-id="35490-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35490-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35490-115">Minimum supported client</span></span><br/> | <span data-ttu-id="35490-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35490-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35490-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35490-117">Minimum supported server</span></span><br/> | <span data-ttu-id="35490-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35490-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35490-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35490-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="35490-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35490-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35490-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="35490-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="35490-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35490-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35490-123">DLL</span><span class="sxs-lookup"><span data-stu-id="35490-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35490-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35490-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="35490-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="35490-125">CLSID</span></span><br/>                    | <span data-ttu-id="35490-126">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="35490-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="35490-127">IID</span><span class="sxs-lookup"><span data-stu-id="35490-127">IID</span></span><br/>                      | <span data-ttu-id="35490-128">ISWbemRefreshableItem de IID \_</span><span class="sxs-lookup"><span data-stu-id="35490-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="35490-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="35490-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35490-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="35490-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="35490-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="35490-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




