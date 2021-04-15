---
description: Recupera o IInkAnalysisRecognizer no índice especificado.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Método IInkAnalysisRecognizers:: GetInkAnalysisRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461152"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a><span data-ttu-id="7cb0c-103">Método IInkAnalysisRecognizers:: GetInkAnalysisRecognizer</span><span class="sxs-lookup"><span data-stu-id="7cb0c-103">IInkAnalysisRecognizers::GetInkAnalysisRecognizer method</span></span>

<span data-ttu-id="7cb0c-104">Recupera o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-104">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb0c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cb0c-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="7cb0c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cb0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cb0c-107">*ulIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cb0c-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb0c-108">O índice de base zero do objeto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-108">The zero-based index of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="7cb0c-109">*ppInkAnalysisRecognizer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7cb0c-109">*ppInkAnalysisRecognizer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cb0c-110">Um ponteiro para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-110">A pointer to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cb0c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cb0c-111">Return value</span></span>

<span data-ttu-id="7cb0c-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7cb0c-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb0c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cb0c-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7cb0c-114">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppInkAnalysisRecognizer* quando você não precisar mais usar o reconhecedor de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="7cb0c-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppInkAnalysisRecognizer* when you no longer need to use the ink analysis recognizer.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7cb0c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cb0c-115">Requirements</span></span>



| <span data-ttu-id="7cb0c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cb0c-116">Requirement</span></span> | <span data-ttu-id="7cb0c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7cb0c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb0c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cb0c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7cb0c-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7cb0c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7cb0c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cb0c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7cb0c-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7cb0c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7cb0c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cb0c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cb0c-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7cb0c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7cb0c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7cb0c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cb0c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cb0c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7cb0c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cb0c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb0c-127">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="7cb0c-127">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="7cb0c-128">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="7cb0c-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

