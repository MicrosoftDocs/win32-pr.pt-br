---
description: Move os dados de traço deste IContextNode para o IContextNode especificado.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'Método IContextNode:: ReparentStrokeByIdToNode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789607"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a><span data-ttu-id="9c696-103">Método IContextNode:: ReparentStrokeByIdToNode</span><span class="sxs-lookup"><span data-stu-id="9c696-103">IContextNode::ReparentStrokeByIdToNode method</span></span>

<span data-ttu-id="9c696-104">Move os dados de traço deste [**IContextNode**](icontextnode.md) para o **IContextNode** especificado.</span><span class="sxs-lookup"><span data-stu-id="9c696-104">Moves stroke data from this [**IContextNode**](icontextnode.md) to the specified **IContextNode**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c696-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c696-105">Syntax</span></span>


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a><span data-ttu-id="9c696-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c696-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c696-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c696-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c696-108">O identificador do traço a ser movido.</span><span class="sxs-lookup"><span data-stu-id="9c696-108">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="9c696-109">*pContextNodeDestination* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9c696-109">*pContextNodeDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c696-110">O objeto [**IContextNode**](icontextnode.md) para o qual mover os dados de traço.</span><span class="sxs-lookup"><span data-stu-id="9c696-110">The [**IContextNode**](icontextnode.md) object to which to move the stroke data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c696-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9c696-111">Return value</span></span>

<span data-ttu-id="9c696-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9c696-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c696-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c696-113">Remarks</span></span>

<span data-ttu-id="9c696-114">O objeto [**IContextNode**](icontextnode.md) especificado deve ser um dos tipos a seguir das constantes [de tipos de nó de contexto](context-node-types.md) : **InkWord**, **InkDrawing**, **InkBullet** ou **UnclassifiedInk**.</span><span class="sxs-lookup"><span data-stu-id="9c696-114">The specified [**IContextNode**](icontextnode.md) object must be one of the following types from the [Context Node Types](context-node-types.md) constants: **InkWord**, **InkDrawing**, **InkBullet**, or **UnclassifiedInk**.</span></span> <span data-ttu-id="9c696-115">A tentativa de mover um traço para qualquer outro tipo de objeto **IContextNode** resulta em um valor de retorno de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="9c696-115">Attempting to move a stroke to any other type of **IContextNode** object results in a return value of **E\_INVALIDARG**.</span></span>

<span data-ttu-id="9c696-116">Esse método pode ser chamado de qualquer objeto [**IContextNode**](icontextnode.md) , incluindo objetos **IContextNode** folha que não são de tinta.</span><span class="sxs-lookup"><span data-stu-id="9c696-116">This method can be called from any [**IContextNode**](icontextnode.md) object, including non-ink leaf **IContextNode** objects.</span></span> <span data-ttu-id="9c696-117">O traço especificado deve ser referenciado por um dos descendentes deste objeto **IContextNode** ou **E \_ INVALIDARG** é retornado.</span><span class="sxs-lookup"><span data-stu-id="9c696-117">The specified stroke must be referenced by one of the descendants of this **IContextNode** object or **E\_INVALIDARG** is returned.</span></span>

<span data-ttu-id="9c696-118">Se esse [**IContextNode**](icontextnode.md) ou **IContextNode** em *pContextNodeDestination* for confirmado, **e \_ INVALIDARG** será retornado (consulte [**IContextNode::**](icontextnode-isconfirmed.md)IsDeleted).</span><span class="sxs-lookup"><span data-stu-id="9c696-118">If either this [**IContextNode**](icontextnode.md) or the **IContextNode** in *pContextNodeDestination* is confirmed, **E\_INVALIDARG** is returned (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).</span></span>

<span data-ttu-id="9c696-119">O analisador de tinta não exclui nós de contexto vazios de sua árvore de resultados em resposta a esse método.</span><span class="sxs-lookup"><span data-stu-id="9c696-119">The ink analyzer does not delete empty context nodes from its results tree in response to this method.</span></span>

-   <span data-ttu-id="9c696-120">Um nó folha de tinta que não faz referência a nenhum dado de traço é um nó vazio.</span><span class="sxs-lookup"><span data-stu-id="9c696-120">An ink leaf node that does not reference any stroke data is an empty node.</span></span>
-   <span data-ttu-id="9c696-121">Um nó de contêiner que não faz referência a nós filho é um nó vazio.</span><span class="sxs-lookup"><span data-stu-id="9c696-121">A container node that does not reference any child nodes is an empty node.</span></span>

<span data-ttu-id="9c696-122">Um nó vazio gera erros se estiver na árvore durante uma operação de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="9c696-122">An empty node generates errors if it is in the tree during an ink analysis operation.</span></span> <span data-ttu-id="9c696-123">Para remover um nó da árvore do analisador de tinta, chame o método [**IContextNode::D eletesubnode**](icontextnode-deletesubnode.md) do nó pai (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md)).</span><span class="sxs-lookup"><span data-stu-id="9c696-123">To remove a node from the ink analyzer's tree, call the parent node's [**IContextNode::DeleteSubNode**](icontextnode-deletesubnode.md) method (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c696-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c696-124">Requirements</span></span>



| <span data-ttu-id="9c696-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c696-125">Requirement</span></span> | <span data-ttu-id="9c696-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9c696-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c696-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c696-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9c696-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9c696-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9c696-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c696-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9c696-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9c696-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9c696-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9c696-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c696-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9c696-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9c696-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9c696-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c696-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c696-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9c696-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c696-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c696-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9c696-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9c696-137">**IContextNode:: settraços**</span><span class="sxs-lookup"><span data-stu-id="9c696-137">**IContextNode::SetStrokes**</span></span>](icontextnode-setstrokes.md)
</dt> <dt>

[<span data-ttu-id="9c696-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="9c696-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




