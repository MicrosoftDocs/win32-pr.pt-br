---
description: Recupera o número de objetos IInkAnalysisRecognizer nesta coleção.
ms.assetid: dfb5c530-b481-4c60-b7fe-87fe162de270
title: 'Método IInkAnalysisRecognizers:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e65f8399c661d551e805abe5f1c5db33eb0b154a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501808"
---
# <a name="iinkanalysisrecognizersgetcount-method"></a><span data-ttu-id="5433b-103">Método IInkAnalysisRecognizers:: GetCount</span><span class="sxs-lookup"><span data-stu-id="5433b-103">IInkAnalysisRecognizers::GetCount method</span></span>

<span data-ttu-id="5433b-104">Recupera o número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="5433b-104">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5433b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5433b-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="5433b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5433b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5433b-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5433b-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5433b-108">O número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="5433b-108">The number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5433b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5433b-109">Return value</span></span>

<span data-ttu-id="5433b-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5433b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5433b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5433b-111">Requirements</span></span>



| <span data-ttu-id="5433b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5433b-112">Requirement</span></span> | <span data-ttu-id="5433b-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5433b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5433b-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5433b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5433b-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5433b-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5433b-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5433b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5433b-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5433b-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5433b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5433b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5433b-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5433b-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5433b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="5433b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5433b-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5433b-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5433b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5433b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5433b-123">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="5433b-123">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="5433b-124">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="5433b-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




