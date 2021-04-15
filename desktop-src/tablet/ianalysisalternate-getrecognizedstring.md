---
description: Obtém o valor de cadeia de caracteres reconhecido do objeto IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'Método IAnalysisAlternate:: reconhecívelstring (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501828"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a><span data-ttu-id="fa348-103">Método IAnalysisAlternate:: reconhecívelstring</span><span class="sxs-lookup"><span data-stu-id="fa348-103">IAnalysisAlternate::GetRecognizedString method</span></span>

<span data-ttu-id="fa348-104">Obtém o valor de cadeia de caracteres reconhecido do objeto [**IAnalysisAlternate**](ianalysisalternate.md) .</span><span class="sxs-lookup"><span data-stu-id="fa348-104">Gets the recognized string value of the [**IAnalysisAlternate**](ianalysisalternate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa348-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa348-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="fa348-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa348-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa348-107">*pbstrRecognizedString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa348-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa348-108">Um ponteiro para o **BSTR** que é definido como o valor de cadeia de caracteres reconhecido.</span><span class="sxs-lookup"><span data-stu-id="fa348-108">A pointer to the **BSTR** that is set to the recognized string value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa348-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa348-109">Return value</span></span>

<span data-ttu-id="fa348-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fa348-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa348-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa348-111">Requirements</span></span>



| <span data-ttu-id="fa348-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa348-112">Requirement</span></span> | <span data-ttu-id="fa348-113">Valor</span><span class="sxs-lookup"><span data-stu-id="fa348-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa348-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa348-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fa348-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fa348-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fa348-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa348-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fa348-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fa348-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fa348-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa348-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa348-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fa348-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa348-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fa348-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa348-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa348-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fa348-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa348-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa348-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="fa348-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="fa348-124">**Método IInkAnalyzer:: reconhecívelstring**</span><span class="sxs-lookup"><span data-stu-id="fa348-124">**IInkAnalyzer::GetRecognizedString Method**</span></span>](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




