---
description: Cria um novo objeto filho IContextNode.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Método IContextNode:: CreateSubNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827190"
---
# <a name="icontextnodecreatesubnode-method"></a><span data-ttu-id="4d7b5-103">Método IContextNode:: CreateSubNode</span><span class="sxs-lookup"><span data-stu-id="4d7b5-103">IContextNode::CreateSubNode method</span></span>

<span data-ttu-id="4d7b5-104">Cria um novo objeto filho [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="4d7b5-104">Creates a new child [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d7b5-105">Syntax</span></span>


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="4d7b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d7b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7b5-107">*pNodeType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d7b5-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7b5-108">Um **GUID** que representa o tipo de [**IContextNode**](icontextnode.md) a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4d7b5-108">A **GUID** that represents the type of [**IContextNode**](icontextnode.md) to create.</span></span>

</dd> <dt>

<span data-ttu-id="4d7b5-109">*ppContextNodeCreated* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4d7b5-109">*ppContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7b5-110">Um ponteiro para o novo [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="4d7b5-110">A pointer to the new [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d7b5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d7b5-111">Return value</span></span>

<span data-ttu-id="4d7b5-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4d7b5-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d7b5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d7b5-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4d7b5-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextNodeCreated* quando você não precisar mais usar o nó de contexto.</span><span class="sxs-lookup"><span data-stu-id="4d7b5-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="4d7b5-115">O novo [**IContextNode**](icontextnode.md) é adicionado à coleção de nós filho do nó de contexto (consulte [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="4d7b5-115">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="4d7b5-116">Quando há nós filho existentes, o **IContextNode** recém-criado é adicionado como o último nó filho.</span><span class="sxs-lookup"><span data-stu-id="4d7b5-116">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="4d7b5-117">Para obter uma lista de tipos de nó de contexto, consulte [tipos de nó de contexto](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="4d7b5-117">For a list of context node types, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d7b5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d7b5-118">Requirements</span></span>



| <span data-ttu-id="4d7b5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d7b5-119">Requirement</span></span> | <span data-ttu-id="4d7b5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4d7b5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7b5-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d7b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4d7b5-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4d7b5-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d7b5-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d7b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4d7b5-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4d7b5-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4d7b5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d7b5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d7b5-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4d7b5-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4d7b5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4d7b5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d7b5-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d7b5-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4d7b5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d7b5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7b5-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="4d7b5-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4d7b5-131">**IContextNode::D eleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="4d7b5-131">**IContextNode::DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)
</dt> <dt>

[<span data-ttu-id="4d7b5-132">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="4d7b5-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

