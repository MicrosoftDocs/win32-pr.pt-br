---
description: A propriedade SWbemRefreshableItem. Object representa uma única instância de SWbemObject que é atualizada. O item está contido em um objeto SWbemRefresher. Instância de SWbemObject que é atualizada. O item está contido em um objeto SWbemRefresher.
ms.assetid: 91a693c0-cde4-4cf6-b85a-662cfd0333e9
ms.tgt_platform: multiple
title: Propriedade SWbemRefreshableItem. Object (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Object
- ISWbemRefreshableItem.Object
- ISWbemRefreshableItem.get_Object
- ISWbemRefreshableItem.put_Object
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b8456422088e9914562b87b2b114629bd80003c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930136"
---
# <a name="swbemrefreshableitemobject-property"></a><span data-ttu-id="c6b51-105">Propriedade SWbemRefreshableItem. Object</span><span class="sxs-lookup"><span data-stu-id="c6b51-105">SWbemRefreshableItem.Object property</span></span>

<span data-ttu-id="c6b51-106">A propriedade **SWbemRefreshableItem. Object** representa uma única instância de [**SWbemObject**](swbemobject.md) que é atualizada.</span><span class="sxs-lookup"><span data-stu-id="c6b51-106">The **SWbemRefreshableItem.Object** property represents a single [**SWbemObject**](swbemobject.md) instance that is refreshed.</span></span> <span data-ttu-id="c6b51-107">O item está contido em um objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="c6b51-107">The item is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="c6b51-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c6b51-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c6b51-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c6b51-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6b51-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6b51-110">Syntax</span></span>


```VB
SWbemRefreshableItem.Object As Object
```



## <a name="property-value"></a><span data-ttu-id="c6b51-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c6b51-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b51-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6b51-112">Remarks</span></span>

<span data-ttu-id="c6b51-113">Essa propriedade é **nula** , a menos que [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) seja **false**.</span><span class="sxs-lookup"><span data-stu-id="c6b51-113">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b51-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6b51-114">Requirements</span></span>



| <span data-ttu-id="c6b51-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b51-115">Requirement</span></span> | <span data-ttu-id="c6b51-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c6b51-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b51-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6b51-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b51-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6b51-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c6b51-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6b51-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b51-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6b51-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6b51-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6b51-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b51-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b51-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6b51-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c6b51-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6b51-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c6b51-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c6b51-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c6b51-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6b51-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6b51-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c6b51-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="c6b51-127">CLSID</span></span><br/>                    | <span data-ttu-id="c6b51-128">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="c6b51-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="c6b51-129">IID</span><span class="sxs-lookup"><span data-stu-id="c6b51-129">IID</span></span><br/>                      | <span data-ttu-id="c6b51-130">ISWbemRefreshableItem de IID \_</span><span class="sxs-lookup"><span data-stu-id="c6b51-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="c6b51-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6b51-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b51-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="c6b51-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="c6b51-133">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="c6b51-133">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




