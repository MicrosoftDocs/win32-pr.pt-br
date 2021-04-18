---
description: Modifica o tipo de confirmação, que controla o que o objeto IInkAnalyzer pode alterar sobre o IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'Método IContextNode:: Confirm (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750561"
---
# <a name="icontextnodeconfirm-method"></a><span data-ttu-id="9e5ef-103">Método IContextNode:: Confirm</span><span class="sxs-lookup"><span data-stu-id="9e5ef-103">IContextNode::Confirm method</span></span>

<span data-ttu-id="9e5ef-104">Modifica o tipo de confirmação, que controla o que o objeto [**IInkAnalyzer**](iinkanalyzer.md) pode alterar sobre o [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="9e5ef-104">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e5ef-105">Syntax</span></span>


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a><span data-ttu-id="9e5ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e5ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5ef-107">*confirmable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e5ef-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5ef-108">O [**Confirmtype**](confirmationtype.md) que é aplicado ao nó.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-108">The [**ConfirmationType**](confirmationtype.md) that is applied to the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5ef-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e5ef-109">Return value</span></span>

<span data-ttu-id="9e5ef-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9e5ef-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5ef-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e5ef-111">Remarks</span></span>

<span data-ttu-id="9e5ef-112">Use esse método para permitir que o usuário final confirme se o [**IInkAnalyzer**](iinkanalyzer.md) analisou corretamente os traços.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-112">Use this method to enable the end user to confirm that the [**IInkAnalyzer**](iinkanalyzer.md) has correctly analyzed the strokes.</span></span> <span data-ttu-id="9e5ef-113">Após **IContextNode:: Confirm** ser chamado, o **IInkAnalyzer** não alterará os objetos [**IContextNode**](icontextnode.md) para esses traços durante a análise posterior.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-113">After **IContextNode::Confirm** is called, the **IInkAnalyzer** will not change the [**IContextNode**](icontextnode.md) objects for those strokes during later analysis.</span></span>

<span data-ttu-id="9e5ef-114">Use **IContextNode:: Confirm** quando o usuário tiver confirmado os resultados da análise e não quiser que o [**IInkAnalyzer**](iinkanalyzer.md) altere um [**IContextNode**](icontextnode.md) durante a análise posterior.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-114">Use **IContextNode::Confirm** when the user has confirmed analysis results and does not want the [**IInkAnalyzer**](iinkanalyzer.md) to change an [**IContextNode**](icontextnode.md) during later analysis.</span></span> <span data-ttu-id="9e5ef-115">Por exemplo, se o usuário gravar a palavra "em" e, em seguida, o aplicativo chamar o [**método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md), o analisador de tinta gerará um nó InkWord com o valor de "to".</span><span class="sxs-lookup"><span data-stu-id="9e5ef-115">For example, if the user writes the word "to" and then the application calls [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), the ink analyzer generates an InkWord node with the value of "to".</span></span> <span data-ttu-id="9e5ef-116">Se o usuário adicionar "me" após "to", uma palavra e o aplicativo chamarão o **método IInkAnalyzer:: Analyze** novamente, o analisador de tinta poderá remover o nó InkWord anterior e criar um novo nó InkWord com o valor "Tomé".</span><span class="sxs-lookup"><span data-stu-id="9e5ef-116">If the user then adds "me" after "to" as one word and the application calls **IInkAnalyzer::Analyze Method** again, the ink analyzer may remove the previous InkWord node and create a new InkWord node with the value "tome".</span></span> <span data-ttu-id="9e5ef-117">No entanto, se após a primeira chamada para o **método IInkAnalyzer:: Analyze**, o aplicativo chama **IContextNode:: Confirm** no nó InkWord para "to" com o valor de [**confirmtype**](confirmationtype.md) **NodeTypeAndProperties**, antes que o usuário adicione o "me", quando o aplicativo chama o **método IInkAnalyzer:: Analyze**, o analisador de tinta não remove nem altera o nó "para".</span><span class="sxs-lookup"><span data-stu-id="9e5ef-117">However, if after the first call to **IInkAnalyzer::Analyze Method**, the application calls **IContextNode::Confirm** on the InkWord node for "to" with the [**ConfirmationType**](confirmationtype.md) value **NodeTypeAndProperties**, before the user adds the "me", then when the application calls **IInkAnalyzer::Analyze Method**, the ink analyzer does not remove or change the "to" node.</span></span> <span data-ttu-id="9e5ef-118">Em vez disso, o analisador de tinta pode reconhecer dois nós InkWord para "to" e "me".</span><span class="sxs-lookup"><span data-stu-id="9e5ef-118">Instead, the ink analyzer may recognize two InkWord nodes for "to" and "me".</span></span>

<span data-ttu-id="9e5ef-119">[**IContextNode**](icontextnode.md) só pode confirmar objetos do tipo InkWord e InkDrawing (consulte [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="9e5ef-119">[**IContextNode**](icontextnode.md) can only confirm objects of type InkWord and InkDrawing (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="9e5ef-120">**IContextNode:: Confirm** retorna **E \_ INVALIDARG** quando o nó não é um nó folha.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-120">**IContextNode::Confirm** returns **E\_INVALIDARG** when the node is not a leaf node.</span></span>

<span data-ttu-id="9e5ef-121">Método [**IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md) e [**IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md) não confirmam nenhum nó do qual eles removem dados de traço.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-121">[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) and [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) unconfirm any node from which they remove stroke data.</span></span>

<span data-ttu-id="9e5ef-122">[**IContextNode:: Setstrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer:: setstrokesvalue**](iinkanalyzer-setstrokestype.md)e [**IInkAnalyzer:: Setstroketype**](iinkanalyzer-setstroketype.md) retornam **Core \_ E \_ INVALIDOPERATION** se o objeto [**IContextNode**](icontextnode.md) já estiver confirmado.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-122">[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md), and [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) return **CORE\_E\_INVALIDOPERATION** if the [**IContextNode**](icontextnode.md) object is already confirmed.</span></span>

<span data-ttu-id="9e5ef-123">[**IContextNode:: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) retornará um erro se o nó de origem ou de destino for confirmado.</span><span class="sxs-lookup"><span data-stu-id="9e5ef-123">[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) returns an error if either the source or destination node is confirmed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5ef-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e5ef-124">Requirements</span></span>



| <span data-ttu-id="9e5ef-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e5ef-125">Requirement</span></span> | <span data-ttu-id="9e5ef-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9e5ef-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5ef-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e5ef-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5ef-128">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9e5ef-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9e5ef-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e5ef-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5ef-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9e5ef-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9e5ef-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e5ef-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e5ef-132"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9e5ef-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9e5ef-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9e5ef-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e5ef-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e5ef-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9e5ef-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e5ef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5ef-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9e5ef-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="9e5ef-137">**IContextNode:: IsDeleted**</span><span class="sxs-lookup"><span data-stu-id="9e5ef-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> <dt>

[<span data-ttu-id="9e5ef-138">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="9e5ef-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




