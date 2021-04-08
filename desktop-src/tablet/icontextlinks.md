---
description: Contém uma coleção de objetos que implementam a interface IContextLink.
ms.assetid: 34d1bbbb-85c0-4209-97ca-c22f22a1b625
title: Interface IContextLinks (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b68563aad471a5420b1157e1c5c12d26da17b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920957"
---
# <a name="icontextlinks-interface"></a><span data-ttu-id="07c57-103">Interface IContextLinks</span><span class="sxs-lookup"><span data-stu-id="07c57-103">IContextLinks interface</span></span>

<span data-ttu-id="07c57-104">Contém uma coleção de objetos que implementam a interface [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="07c57-104">Contains a collection of objects that implement the [**IContextLink**](icontextlink.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="07c57-105">Membros</span><span class="sxs-lookup"><span data-stu-id="07c57-105">Members</span></span>

<span data-ttu-id="07c57-106">A interface **IContextLinks** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="07c57-106">The **IContextLinks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="07c57-107">**IContextLinks** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="07c57-107">**IContextLinks** also has these types of members:</span></span>

-   [<span data-ttu-id="07c57-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="07c57-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="07c57-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="07c57-109">Methods</span></span>

<span data-ttu-id="07c57-110">A interface **IContextLinks** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="07c57-110">The **IContextLinks** interface has these methods.</span></span>



| <span data-ttu-id="07c57-111">Método</span><span class="sxs-lookup"><span data-stu-id="07c57-111">Method</span></span>                                                 | <span data-ttu-id="07c57-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="07c57-112">Description</span></span>                                                                                         |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07c57-113">**GetContextLink**</span><span class="sxs-lookup"><span data-stu-id="07c57-113">**GetContextLink**</span></span>](icontextlinks-getcontextlink.md) | <span data-ttu-id="07c57-114">Recupera o [**IContextLink**](icontextlink.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="07c57-114">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span><br/>               |
| [<span data-ttu-id="07c57-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="07c57-115">**GetCount**</span></span>](icontextlinks-getcount.md)             | <span data-ttu-id="07c57-116">Recupera o número de objetos [**IContextLink**](icontextlink.md) nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="07c57-116">Retrieves the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07c57-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="07c57-117">Remarks</span></span>

<span data-ttu-id="07c57-118">Normalmente, isso é acessado por meio do método [**IContextNode:: GetContextLinks**](icontextnode-getcontextlinks.md) .</span><span class="sxs-lookup"><span data-stu-id="07c57-118">This is usually accessed through the [**IContextNode::GetContextLinks**](icontextnode-getcontextlinks.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c57-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c57-119">Requirements</span></span>



| <span data-ttu-id="07c57-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c57-120">Requirement</span></span> | <span data-ttu-id="07c57-121">Valor</span><span class="sxs-lookup"><span data-stu-id="07c57-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c57-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c57-122">Minimum supported client</span></span><br/> | <span data-ttu-id="07c57-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="07c57-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="07c57-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c57-124">Minimum supported server</span></span><br/> | <span data-ttu-id="07c57-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="07c57-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="07c57-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07c57-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c57-127"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="07c57-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="07c57-128">DLL</span><span class="sxs-lookup"><span data-stu-id="07c57-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c57-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07c57-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="07c57-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="07c57-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c57-131">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="07c57-131">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="07c57-132">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="07c57-132">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> <dt>

[<span data-ttu-id="07c57-133">**IContextNode::D eleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="07c57-133">**IContextNode::DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)
</dt> <dt>

[<span data-ttu-id="07c57-134">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="07c57-134">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="07c57-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="07c57-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

