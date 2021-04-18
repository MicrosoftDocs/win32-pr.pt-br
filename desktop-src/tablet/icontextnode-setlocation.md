---
description: Atualiza a área deste IContextNode.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'Método IContextNode:: SetLocation (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796232"
---
# <a name="icontextnodesetlocation-method"></a><span data-ttu-id="d2f51-103">Método IContextNode:: SetLocation</span><span class="sxs-lookup"><span data-stu-id="d2f51-103">IContextNode::SetLocation method</span></span>

<span data-ttu-id="d2f51-104">Atualiza a área deste [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="d2f51-104">Updates the area of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f51-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2f51-105">Syntax</span></span>


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a><span data-ttu-id="d2f51-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2f51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2f51-107">*pIAnalysisRegion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2f51-107">*pIAnalysisRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2f51-108">O [**IAnalysisRegion**](ianalysisregion.md) que descreve a área para a qual definir o local do objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f51-108">The [**IAnalysisRegion**](ianalysisregion.md) describing the area to which to set the [**IContextNode**](icontextnode.md) object's location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2f51-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2f51-109">Return value</span></span>

<span data-ttu-id="d2f51-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d2f51-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d2f51-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2f51-111">Remarks</span></span>

<span data-ttu-id="d2f51-112">Use este método para atualizar o local do nó de contexto (consulte [**IContextNode:: getLocation**](icontextnode-getlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="d2f51-112">Use this method to update the context node's location (see [**IContextNode::GetLocation**](icontextnode-getlocation.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2f51-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2f51-113">Requirements</span></span>



| <span data-ttu-id="d2f51-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2f51-114">Requirement</span></span> | <span data-ttu-id="d2f51-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2f51-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f51-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2f51-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d2f51-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d2f51-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d2f51-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2f51-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d2f51-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d2f51-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d2f51-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2f51-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2f51-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d2f51-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d2f51-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d2f51-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2f51-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2f51-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d2f51-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2f51-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f51-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d2f51-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="d2f51-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="d2f51-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="d2f51-127">**IContextNode:: getLocation**</span><span class="sxs-lookup"><span data-stu-id="d2f51-127">**IContextNode::GetLocation**</span></span>](icontextnode-getlocation.md)
</dt> <dt>

[<span data-ttu-id="d2f51-128">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="d2f51-128">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="d2f51-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="d2f51-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




