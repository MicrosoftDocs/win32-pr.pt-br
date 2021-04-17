---
description: Cria uma cópia do IAnalysisRegion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'Método IAnalysisRegion:: clone (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811389"
---
# <a name="ianalysisregionclone-method"></a><span data-ttu-id="1d235-103">Método IAnalysisRegion:: clone</span><span class="sxs-lookup"><span data-stu-id="1d235-103">IAnalysisRegion::Clone method</span></span>

<span data-ttu-id="1d235-104">Cria uma cópia do [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="1d235-104">Creates a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d235-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d235-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="1d235-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d235-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d235-107">*pClonedRegion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1d235-107">*pClonedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d235-108">Um ponteiro para uma cópia do [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="1d235-108">A pointer to a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d235-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d235-109">Return value</span></span>

<span data-ttu-id="1d235-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1d235-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d235-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d235-111">Remarks</span></span>

<span data-ttu-id="1d235-112">Esse método é eqivalent para o método System. Windows. Ink. AnalysisCore. AnalysisRegionBase. Clone no .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1d235-112">This method is eqivalent to theSystem.Windows.Ink.AnalysisCore.AnalysisRegionBase.Clone Method in the .NET Framework.</span></span>

> [!Caution]  
> <span data-ttu-id="1d235-113">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *pClonedRegion* quando você não precisar mais usar a região de análise clonada.</span><span class="sxs-lookup"><span data-stu-id="1d235-113">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pClonedRegion* when you no longer need to use the cloned analysis region.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d235-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d235-114">Requirements</span></span>



| <span data-ttu-id="1d235-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d235-115">Requirement</span></span> | <span data-ttu-id="1d235-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1d235-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d235-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d235-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d235-118">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1d235-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d235-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d235-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d235-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1d235-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1d235-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d235-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d235-122"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1d235-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1d235-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1d235-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d235-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d235-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1d235-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d235-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d235-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="1d235-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="1d235-127">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="1d235-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

