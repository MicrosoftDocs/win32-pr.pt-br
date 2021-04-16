---
description: Especifica o tipo de confirmação que pode ocorrer em um objeto IContextNode.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Enumeração confirmtype (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765327"
---
# <a name="confirmationtype-enumeration"></a><span data-ttu-id="d8e0d-103">Enumeração confirmtype</span><span class="sxs-lookup"><span data-stu-id="d8e0d-103">ConfirmationType enumeration</span></span>

<span data-ttu-id="d8e0d-104">Especifica o tipo de confirmação que pode ocorrer em um objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e0d-104">Specifies the type of confirmation that can occur on an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8e0d-105">Syntax</span></span>


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a><span data-ttu-id="d8e0d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d8e0d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d8e0d-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**Confirmation \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="d8e0d-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType\_None**</span></span>
</dt> <dd>

<span data-ttu-id="d8e0d-108">Nenhuma confirmação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-108">No confirmation is applied.</span></span> <span data-ttu-id="d8e0d-109">O [**IInkAnalyzer**](iinkanalyzer.md) é livre para alterar um nó de contexto ou qualquer um de seus descendentes, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-109">The [**IInkAnalyzer**](iinkanalyzer.md) is free to change a context node or any of its descendants as needed.</span></span>

</dd> <dt>

<span data-ttu-id="d8e0d-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**NodeTypeAndProperties de confirmações \_**</span><span class="sxs-lookup"><span data-stu-id="d8e0d-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType\_NodeTypeAndProperties**</span></span>
</dt> <dd>

<span data-ttu-id="d8e0d-111">O [**IInkAnalyzer**](iinkanalyzer.md) não pode alterar o tipo ou qualquer Propriedade do nó de contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-111">The [**IInkAnalyzer**](iinkanalyzer.md) cannot change the type or any properties of the specified context node.</span></span>

</dd> <dt>

<span data-ttu-id="d8e0d-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**TopBoundary de confirmações \_**</span><span class="sxs-lookup"><span data-stu-id="d8e0d-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType\_TopBoundary**</span></span>
</dt> <dd>

<span data-ttu-id="d8e0d-113">O [**IInkAnalyzer**](iinkanalyzer.md) não executará operações, incluindo a adição de tinta ou a mesclagem com outras [**ContextNodes**](icontextnodes.md), que fazem com que o TopBoundary se mova para além do limite superior atual.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-113">The [**IInkAnalyzer**](iinkanalyzer.md) will not perform operations, including adding ink or merging with other [**ContextNodes**](icontextnodes.md), that cause the TopBoundary to move beyond the current top boundary.</span></span> <span data-ttu-id="d8e0d-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8e0d-114">For example:</span></span>

-   <span data-ttu-id="d8e0d-115">Um aplicativo analisa um conjunto de tinta e um ParagraphNode é identificado.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-115">An application analyzes a set of Ink, and a ParagraphNode is identified.</span></span>
-   <span data-ttu-id="d8e0d-116">O aplicativo confirma a TopBoundary deste parágrafo.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-116">The application confirms the TopBoundary of this paragraph.</span></span>
-   <span data-ttu-id="d8e0d-117">O usuário do aplicativo grava a nova tinta acima do parágrafo atual.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-117">The user of the application writes new ink above the current paragraph.</span></span> <span data-ttu-id="d8e0d-118">Quando Analyze for chamado novamente, a nova tinta não será incorporada ao nó de parágrafo confirmado.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-118">When analyze is called again, the new ink will not be incorporated into the Confirmed paragraph node.</span></span>
-   <span data-ttu-id="d8e0d-119">Como apenas o limite superior é confirmado, o ContextNode pode continuar crescendo em outras direções.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-119">Since only the top boundary is confirmed, the ContextNode can continue to grow in other directions.</span></span> <span data-ttu-id="d8e0d-120">A exclusão de traços pode fazer com que o limite superior se mova para baixo.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-120">Deleting strokes can cause the top boundary to move down.</span></span> <span data-ttu-id="d8e0d-121">A tradução do ContextNode pode fazer com que o local seja alterado, mas não permitirá que a tinta adicional seja mesclada no novo local.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-121">Translating the ContextNode can cause the location to change, but will not allow additional ink to be merged in the new location.</span></span>

<span data-ttu-id="d8e0d-122">Este confirmtype é aplicável somente a nós de parágrafo.</span><span class="sxs-lookup"><span data-stu-id="d8e0d-122">This ConfirmationType is only applicable to paragraph nodes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8e0d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8e0d-123">Remarks</span></span>

<span data-ttu-id="d8e0d-124">Você pode usar o valor **NodeTypeAndProperties** somente para os nós de desenho de tinta e palavra de tinta (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="d8e0d-124">You can use the **NodeTypeAndProperties** value only for ink word and ink drawing nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="d8e0d-125">Caso contrário, um **E \_ INVALIDARG** será retornado de [**IContextNode:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="d8e0d-125">Otherwise, an **E\_INVALIDARG** is returned from [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e0d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8e0d-126">Requirements</span></span>



| <span data-ttu-id="d8e0d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e0d-127">Requirement</span></span> | <span data-ttu-id="d8e0d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e0d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e0d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8e0d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e0d-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d8e0d-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d8e0d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8e0d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e0d-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d8e0d-132">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d8e0d-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8e0d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8e0d-134"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d8e0d-134"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8e0d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8e0d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e0d-136">**IContextNode:: confirmar**</span><span class="sxs-lookup"><span data-stu-id="d8e0d-136">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="d8e0d-137">**IContextNode:: IsDeleted**</span><span class="sxs-lookup"><span data-stu-id="d8e0d-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




