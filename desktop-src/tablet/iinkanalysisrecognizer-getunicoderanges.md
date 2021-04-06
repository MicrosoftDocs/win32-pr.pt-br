---
description: Recupera uma matriz de intervalos de caracteres que representa os intervalos de caracteres Unicode com suporte.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Método IInkAnalysisRecognizer:: GetUnicodeRanges (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827183"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a><span data-ttu-id="6aa89-103">Método IInkAnalysisRecognizer:: GetUnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="6aa89-103">IInkAnalysisRecognizer::GetUnicodeRanges method</span></span>

<span data-ttu-id="6aa89-104">Recupera uma matriz de intervalos de caracteres que representa os intervalos de caracteres Unicode com suporte.</span><span class="sxs-lookup"><span data-stu-id="6aa89-104">Retrieves an array of character ranges representing the supported Unicode character ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6aa89-105">Syntax</span></span>


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a><span data-ttu-id="6aa89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6aa89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa89-107">*pulNumberOfRanges* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6aa89-107">*pulNumberOfRanges* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa89-108">O número de intervalos de caracteres apontados por *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="6aa89-108">The number of character ranges pointed to by *ppulLowUnicode*.</span></span>

</dd> <dt>

<span data-ttu-id="6aa89-109">*ppulLowUnicode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6aa89-109">*ppulLowUnicode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa89-110">Ponteiro para uma matriz de intervalos de caracteres que representa os intervalos de caracteres Unicode com suporte.</span><span class="sxs-lookup"><span data-stu-id="6aa89-110">Pointer to an array of character ranges representing the supported Unicode character ranges.</span></span>

</dd> <dt>

<span data-ttu-id="6aa89-111">*ppusUnicodeRangeLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6aa89-111">*ppusUnicodeRangeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa89-112">Ponteiro para uma matriz de valores que indica o comprimento de cada ponto de matriz para por *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="6aa89-112">Pointer to an array of values indicating the length of each array point to by *ppulLowUnicode*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa89-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6aa89-113">Return value</span></span>

<span data-ttu-id="6aa89-114">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6aa89-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa89-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6aa89-115">Requirements</span></span>



| <span data-ttu-id="6aa89-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa89-116">Requirement</span></span> | <span data-ttu-id="6aa89-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6aa89-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa89-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aa89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa89-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6aa89-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6aa89-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aa89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa89-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6aa89-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6aa89-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6aa89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aa89-123"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6aa89-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6aa89-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6aa89-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aa89-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aa89-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6aa89-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6aa89-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa89-127">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="6aa89-127">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




