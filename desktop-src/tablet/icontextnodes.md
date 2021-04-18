---
description: Contém uma coleção de objetos que implementam a interface IContextNode e que são o resultado de uma operação de análise de tinta.
ms.assetid: 2c4e9d84-243a-40e4-b3f9-5c4cafc5aac4
title: Interface IContextNodes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 306abcd32dcb0ee55978a6b95ee9f8a2c22cd19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793393"
---
# <a name="icontextnodes-interface"></a><span data-ttu-id="be66a-103">Interface IContextNodes</span><span class="sxs-lookup"><span data-stu-id="be66a-103">IContextNodes interface</span></span>

<span data-ttu-id="be66a-104">Contém uma coleção de objetos que implementam a interface [**IContextNode**](icontextnode.md) e que são o resultado de uma operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="be66a-104">Contains a collection of objects that implement the [**IContextNode**](icontextnode.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="be66a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="be66a-105">Members</span></span>

<span data-ttu-id="be66a-106">A interface **IContextNodes** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="be66a-106">The **IContextNodes** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be66a-107">**IContextNodes** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="be66a-107">**IContextNodes** also has these types of members:</span></span>

-   [<span data-ttu-id="be66a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="be66a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be66a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="be66a-109">Methods</span></span>

<span data-ttu-id="be66a-110">A interface **IContextNodes** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="be66a-110">The **IContextNodes** interface has these methods.</span></span>



| <span data-ttu-id="be66a-111">Método</span><span class="sxs-lookup"><span data-stu-id="be66a-111">Method</span></span>                                                       | <span data-ttu-id="be66a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="be66a-112">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be66a-113">**AddContextNode**</span><span class="sxs-lookup"><span data-stu-id="be66a-113">**AddContextNode**</span></span>](icontextnodes-addcontextnode.md)       | <span data-ttu-id="be66a-114">Adiciona um objeto [**IContextNode**](icontextnode.md) a esta coleção.</span><span class="sxs-lookup"><span data-stu-id="be66a-114">Adds an [**IContextNode**](icontextnode.md) object to this collection.</span></span> <br/>                                  |
| [<span data-ttu-id="be66a-115">**GetContextNode**</span><span class="sxs-lookup"><span data-stu-id="be66a-115">**GetContextNode**</span></span>](icontextnodes-getcontextnode.md)       | <span data-ttu-id="be66a-116">Recupera o objeto [**IContextNode**](icontextnode.md) no índice especificado dentro desta coleção.</span><span class="sxs-lookup"><span data-stu-id="be66a-116">Retrieves the [**IContextNode**](icontextnode.md) object at the specified index within this collection.</span></span> <br/> |
| [<span data-ttu-id="be66a-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="be66a-117">**GetCount**</span></span>](icontextnodes-getcount.md)                   | <span data-ttu-id="be66a-118">Recupera o número de objetos [**IContextNode**](icontextnode.md) contidos nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="be66a-118">Retrieves the number of [**IContextNode**](icontextnode.md) objects contained in this collection.</span></span> <br/>       |
| [<span data-ttu-id="be66a-119">**RemoveContextNode**</span><span class="sxs-lookup"><span data-stu-id="be66a-119">**RemoveContextNode**</span></span>](icontextnodes-removecontextnode.md) | <span data-ttu-id="be66a-120">Remove um objeto [**IContextNode**](icontextnode.md) desta coleção.</span><span class="sxs-lookup"><span data-stu-id="be66a-120">Removes an [**IContextNode**](icontextnode.md) object from this collection.</span></span> <br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="be66a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be66a-121">Requirements</span></span>



| <span data-ttu-id="be66a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="be66a-122">Requirement</span></span> | <span data-ttu-id="be66a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="be66a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be66a-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be66a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be66a-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be66a-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be66a-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be66a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be66a-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="be66a-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be66a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be66a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be66a-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be66a-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be66a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="be66a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be66a-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be66a-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be66a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="be66a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be66a-133">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="be66a-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="be66a-134">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="be66a-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

