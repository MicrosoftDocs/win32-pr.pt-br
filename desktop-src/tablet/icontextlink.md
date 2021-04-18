---
description: Representa uma relação entre dois objetos IContextNode.
ms.assetid: ee81d9d7-eba9-4b11-84d0-5a6ca0df7d92
title: Interface IContextLink (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df1e0d8717ba29532486277aced19f17adb1d79c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772576"
---
# <a name="icontextlink-interface"></a><span data-ttu-id="8a5cf-103">Interface IContextLink</span><span class="sxs-lookup"><span data-stu-id="8a5cf-103">IContextLink interface</span></span>

<span data-ttu-id="8a5cf-104">Representa uma relação entre dois objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="8a5cf-104">Represents a relationship between two [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="8a5cf-105">Membros</span><span class="sxs-lookup"><span data-stu-id="8a5cf-105">Members</span></span>

<span data-ttu-id="8a5cf-106">A interface **IContextLink** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8a5cf-106">The **IContextLink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8a5cf-107">**IContextLink** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8a5cf-107">**IContextLink** also has these types of members:</span></span>

-   [<span data-ttu-id="8a5cf-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a5cf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8a5cf-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a5cf-109">Methods</span></span>

<span data-ttu-id="8a5cf-110">A interface **IContextLink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8a5cf-110">The **IContextLink** interface has these methods.</span></span>



| <span data-ttu-id="8a5cf-111">Método</span><span class="sxs-lookup"><span data-stu-id="8a5cf-111">Method</span></span>                                                                  | <span data-ttu-id="8a5cf-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a5cf-112">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a5cf-113">**GetContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="8a5cf-113">**GetContextLinkDirection**</span></span>](icontextlink-getcontextlinkdirection.md) | <span data-ttu-id="8a5cf-114">Recupera o tipo de relação que esse **IContextLink** representa.</span><span class="sxs-lookup"><span data-stu-id="8a5cf-114">Retrieves the type of relationship this **IContextLink** represents.</span></span><br/>                                         |
| [<span data-ttu-id="8a5cf-115">**GetDestinationNode**</span><span class="sxs-lookup"><span data-stu-id="8a5cf-115">**GetDestinationNode**</span></span>](icontextlink-getdestinationnode.md)           | <span data-ttu-id="8a5cf-116">Recupera o objeto [**IContextNode**](icontextnode.md) que é o destino para este **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="8a5cf-116">Retrieves the [**IContextNode**](icontextnode.md) object that is the destination for this **IContextLink**.</span></span><br/> |
| [<span data-ttu-id="8a5cf-117">**GetSourceNode**</span><span class="sxs-lookup"><span data-stu-id="8a5cf-117">**GetSourceNode**</span></span>](icontextlink-getsourcenode.md)                     | <span data-ttu-id="8a5cf-118">Recupera o objeto [**IContextNode**](icontextnode.md) que é a origem para este **IContextLink**.</span><span class="sxs-lookup"><span data-stu-id="8a5cf-118">Retrieves the [**IContextNode**](icontextnode.md) object that is the source for this **IContextLink**.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="8a5cf-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a5cf-119">Remarks</span></span>

<span data-ttu-id="8a5cf-120">Veja a seguir um exemplo de uma relação representada por um objeto **IContextLink** :</span><span class="sxs-lookup"><span data-stu-id="8a5cf-120">The following is an example of a relationship represented by an **IContextLink** object:</span></span>

-   <span data-ttu-id="8a5cf-121">Quando um nó AnalysisHint é usado na análise de tinta, a operação de análise de tinta cria um objeto **IContextLink** do tipo AnalysisHint entre o nó de dica de análise e o nó que contém a gravação dentro da área da dica.</span><span class="sxs-lookup"><span data-stu-id="8a5cf-121">When an AnalysisHint node is used in ink analysis, the ink analysis operation creates an **IContextLink** object of type AnalysisHint between the analysis hint node and the node that contains writing within the area of the hint.</span></span> <span data-ttu-id="8a5cf-122">O nó de origem é o nó de dica de análise e o nó de destino é o nó que contém a gravação.</span><span class="sxs-lookup"><span data-stu-id="8a5cf-122">The source node is the analysis hint node and the destination node is the node that contains writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a5cf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a5cf-123">Requirements</span></span>



| <span data-ttu-id="8a5cf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a5cf-124">Requirement</span></span> | <span data-ttu-id="8a5cf-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8a5cf-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5cf-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a5cf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8a5cf-127">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8a5cf-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a5cf-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a5cf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8a5cf-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8a5cf-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a5cf-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a5cf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a5cf-131"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8a5cf-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a5cf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8a5cf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a5cf-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a5cf-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a5cf-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a5cf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5cf-135">**IContextNode::GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="8a5cf-135">**IContextNode::GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)
</dt> <dt>

[<span data-ttu-id="8a5cf-136">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="8a5cf-136">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="8a5cf-137">**ContextLinkDirection**</span><span class="sxs-lookup"><span data-stu-id="8a5cf-137">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="8a5cf-138">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="8a5cf-138">Context Node Types</span></span>](context-node-types.md)
</dt> </dl>

 

