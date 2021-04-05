---
description: Cria um objeto IContextNode filho que contém apenas informações sobre o tipo, o identificador e o local.
ms.assetid: 181028fb-f67c-4c90-bb09-94b68a887bd1
title: 'Método IContextNode:: CreatePartiallyPopulatedSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreatePartiallyPopulatedSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7947ba4665bdb101e955246fcc99352a24a4397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827191"
---
# <a name="icontextnodecreatepartiallypopulatedsubnode-method"></a><span data-ttu-id="3af10-103">Método IContextNode:: CreatePartiallyPopulatedSubNode</span><span class="sxs-lookup"><span data-stu-id="3af10-103">IContextNode::CreatePartiallyPopulatedSubNode method</span></span>

<span data-ttu-id="3af10-104">Cria um objeto [**IContextNode**](icontextnode.md) filho que contém apenas informações sobre o tipo, o identificador e o local.</span><span class="sxs-lookup"><span data-stu-id="3af10-104">Creates a child [**IContextNode**](icontextnode.md) object that contains only information about type, identifier, and location.</span></span>

## <a name="syntax"></a><span data-ttu-id="3af10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3af10-105">Syntax</span></span>


```C++
HRESULT CreatePartiallyPopulatedSubNode(
  [in]  const GUID            *pNodeType,
  [in]  const GUID            *pNodeId,
  [in]        IAnalysisRegion *pNodeLocation,
  [out]       IContextNode    **pPartiallyPopulatedContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="3af10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3af10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3af10-107">*pNodeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3af10-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3af10-108">O tipo de nó de contexto a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3af10-108">The type of context node to create.</span></span>

</dd> <dt>

<span data-ttu-id="3af10-109">*pNodeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3af10-109">*pNodeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3af10-110">O identificador do novo nó.</span><span class="sxs-lookup"><span data-stu-id="3af10-110">The identifier for the new node.</span></span>

</dd> <dt>

<span data-ttu-id="3af10-111">*pNodeLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3af10-111">*pNodeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3af10-112">O local do novo nó.</span><span class="sxs-lookup"><span data-stu-id="3af10-112">The location of the new node.</span></span>

</dd> <dt>

<span data-ttu-id="3af10-113">*pPartiallyPopulatedContextNodeCreated* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3af10-113">*pPartiallyPopulatedContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3af10-114">Um ponteiro para o novo [**IContextNode**](icontextnode.md)parcialmente preenchido.</span><span class="sxs-lookup"><span data-stu-id="3af10-114">A pointer to the new, partially populated [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3af10-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3af10-115">Return value</span></span>

<span data-ttu-id="3af10-116">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3af10-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3af10-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3af10-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3af10-118">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pPartiallyPopulatedContextNodeCreated* quando você não precisar mais usar o nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="3af10-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pPartiallyPopulatedContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="3af10-119">O novo [**IContextNode**](icontextnode.md) é adicionado à coleção de nós filho do nó de contexto (consulte [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="3af10-119">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="3af10-120">Quando há nós filho existentes, o **IContextNode** recém-criado é adicionado como o último nó filho.</span><span class="sxs-lookup"><span data-stu-id="3af10-120">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="3af10-121">Para obter mais informações sobre tipo, identificador e local, consulte [**IContextNode:: GetType**](icontextnode-gettype.md), [**IContextNode:: GetID**](icontextnode-getid.md)e [**IContextNode:: getLocation**](icontextnode-getlocation.md).</span><span class="sxs-lookup"><span data-stu-id="3af10-121">For more information about type, identifier, and location, see [**IContextNode::GetType**](icontextnode-gettype.md), [**IContextNode::GetId**](icontextnode-getid.md), and [**IContextNode::GetLocation**](icontextnode-getlocation.md).</span></span>

<span data-ttu-id="3af10-122">Esse método é usado para o proxy de dados como uma maneira de criar um objeto [**IContextNode**](icontextnode.md) na árvore de nós de contexto antes que todas as informações sobre ele estejam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3af10-122">This method is used for data proxy as a way to create an [**IContextNode**](icontextnode.md) object in the context node tree before all the information about it is available.</span></span> <span data-ttu-id="3af10-123">Para obter mais informações, consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="3af10-123">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3af10-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3af10-124">Requirements</span></span>



| <span data-ttu-id="3af10-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3af10-125">Requirement</span></span> | <span data-ttu-id="3af10-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3af10-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3af10-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3af10-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3af10-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3af10-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3af10-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3af10-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3af10-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3af10-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3af10-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3af10-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3af10-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3af10-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3af10-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3af10-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3af10-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3af10-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3af10-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3af10-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af10-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="3af10-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="3af10-137">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="3af10-137">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="3af10-138">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="3af10-138">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="3af10-139">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="3af10-139">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="3af10-140">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="3af10-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

