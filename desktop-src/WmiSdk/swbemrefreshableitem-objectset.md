---
description: A propriedade SWbemRefreshableItem. ObjectSet representa o conjunto de objetos a ser atualizado.
ms.assetid: f52101b1-bb6e-4798-b20f-d6efd31cf7c1
ms.tgt_platform: multiple
title: Propriedade SWbemRefreshableItem. ObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.get_ObjectSet
- ISWbemRefreshableItem.put_ObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbc611bb9e1a72f53e2178039b0ad76411e39a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297926"
---
# <a name="swbemrefreshableitemobjectset-property"></a><span data-ttu-id="a7dde-103">Propriedade SWbemRefreshableItem. ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a7dde-103">SWbemRefreshableItem.ObjectSet property</span></span>

<span data-ttu-id="a7dde-104">A propriedade **SWbemRefreshableItem. ObjectSet** representa o conjunto de objetos a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="a7dde-104">The **SWbemRefreshableItem.ObjectSet** property represents the object set to be refreshed.</span></span> <span data-ttu-id="a7dde-105">A propriedade **ObjectSet** é um enumerador ou um item de coleta contido em um objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="a7dde-105">The **ObjectSet** property is either an enumerator or a collection item that is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="a7dde-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a7dde-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a7dde-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a7dde-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7dde-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7dde-108">Syntax</span></span>


```VB
SWbemRefreshableItem.ObjectSet As Object
```



## <a name="property-value"></a><span data-ttu-id="a7dde-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a7dde-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="a7dde-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7dde-110">Remarks</span></span>

<span data-ttu-id="a7dde-111">Essa propriedade é **nula** , a menos que [**SWbemRefreshableItem. IsSet**](swbemrefreshableitem-isset.md) seja **true**.</span><span class="sxs-lookup"><span data-stu-id="a7dde-111">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7dde-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7dde-112">Requirements</span></span>



| <span data-ttu-id="a7dde-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7dde-113">Requirement</span></span> | <span data-ttu-id="a7dde-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a7dde-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7dde-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7dde-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a7dde-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7dde-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7dde-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7dde-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a7dde-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7dde-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7dde-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7dde-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7dde-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7dde-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7dde-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a7dde-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7dde-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a7dde-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a7dde-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a7dde-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7dde-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7dde-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7dde-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="a7dde-125">CLSID</span></span><br/>                    | <span data-ttu-id="a7dde-126">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="a7dde-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="a7dde-127">IID</span><span class="sxs-lookup"><span data-stu-id="a7dde-127">IID</span></span><br/>                      | <span data-ttu-id="a7dde-128">ISWbemRefreshableItem de IID \_</span><span class="sxs-lookup"><span data-stu-id="a7dde-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="a7dde-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7dde-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7dde-130">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="a7dde-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="a7dde-131">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="a7dde-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




