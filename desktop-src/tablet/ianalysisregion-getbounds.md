---
description: Obtém o retângulo delimitador do IAnalysisRegion.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'Método IAnalysisRegion:: GetBounds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647243"
---
# <a name="ianalysisregiongetbounds-method"></a><span data-ttu-id="e7944-103">Método IAnalysisRegion:: GetBounds</span><span class="sxs-lookup"><span data-stu-id="e7944-103">IAnalysisRegion::GetBounds method</span></span>

<span data-ttu-id="e7944-104">Obtém o retângulo delimitador do [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="e7944-104">Gets the bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7944-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7944-105">Syntax</span></span>


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="e7944-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7944-107">*pBoundingRectangle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7944-107">*pBoundingRectangle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7944-108">O retângulo delimitador do [**IAnalysisRegion**](ianalysisregion.md) nas coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="e7944-108">The bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md) in ink space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7944-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7944-109">Return value</span></span>

<span data-ttu-id="e7944-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e7944-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7944-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7944-111">Remarks</span></span>

<span data-ttu-id="e7944-112">Os limites estão em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="e7944-112">The bounds are in ink-space coordinates.</span></span>

<span data-ttu-id="e7944-113">Se [**IAnalysisRegion**](ianalysisregion.md) representar uma área infinita, os limites esquerdo e superior serão **int \_ min**; e os limites direito e inferior serão **int \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="e7944-113">If the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite area, the left and top bounds are **INT\_MIN**; and the right and bottom bounds are **INT\_MAX**.</span></span>

<span data-ttu-id="e7944-114">Se [**IAnalysisRegion**](ianalysisregion.md) representar uma área vazia, todos os limites do retângulo serão 0.</span><span class="sxs-lookup"><span data-stu-id="e7944-114">If the [**IAnalysisRegion**](ianalysisregion.md) represents an empty area, all the bounds of the rectangle are 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7944-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7944-115">Requirements</span></span>



| <span data-ttu-id="e7944-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7944-116">Requirement</span></span> | <span data-ttu-id="e7944-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e7944-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7944-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7944-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e7944-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e7944-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e7944-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7944-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e7944-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e7944-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e7944-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7944-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7944-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e7944-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e7944-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e7944-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7944-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7944-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e7944-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7944-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7944-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="e7944-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="e7944-128">**Método IAnalysisRegion:: GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="e7944-128">**IAnalysisRegion::GetRegionScans Method**</span></span>](ianalysisregion-getregionscans.md)
</dt> <dt>

[<span data-ttu-id="e7944-129">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="e7944-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




