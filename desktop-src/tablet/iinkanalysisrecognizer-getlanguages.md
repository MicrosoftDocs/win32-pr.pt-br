---
description: Recupera os identificadores para as localidades às quais esse IInkAnalysisRecognizer dá suporte.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'Método IInkAnalysisRecognizer:: GetLanguages (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827184"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a><span data-ttu-id="70a60-103">Método IInkAnalysisRecognizer:: GetLanguages</span><span class="sxs-lookup"><span data-stu-id="70a60-103">IInkAnalysisRecognizer::GetLanguages method</span></span>

<span data-ttu-id="70a60-104">Recupera os identificadores para as localidades às quais esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dá suporte.</span><span class="sxs-lookup"><span data-stu-id="70a60-104">Retrieves the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a60-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70a60-105">Syntax</span></span>


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a><span data-ttu-id="70a60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70a60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70a60-107">*pulLanguagesCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="70a60-107">*pulLanguagesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70a60-108">O número de identificadores em *ppulLanguages*.</span><span class="sxs-lookup"><span data-stu-id="70a60-108">The number of identifiers in *ppulLanguages*.</span></span>

</dd> <dt>

<span data-ttu-id="70a60-109">*ppulLanguages* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="70a60-109">*ppulLanguages* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70a60-110">Um ponteiro para os identificadores para as localidades às quais esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dá suporte.</span><span class="sxs-lookup"><span data-stu-id="70a60-110">A pointer to the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70a60-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70a60-111">Return value</span></span>

<span data-ttu-id="70a60-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="70a60-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70a60-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="70a60-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="70a60-114">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppulLanguages* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="70a60-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppulLanguages* when you no longer need the information.</span></span>

 

<span data-ttu-id="70a60-115">Esse método retorna uma matriz vazia para reconhecedores de objeto e de gesto.</span><span class="sxs-lookup"><span data-stu-id="70a60-115">This method returns an empty array for object and gesture recognizers.</span></span>

<span data-ttu-id="70a60-116">Para obter mais informações sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="70a60-116">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="70a60-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70a60-117">Requirements</span></span>



| <span data-ttu-id="70a60-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a60-118">Requirement</span></span> | <span data-ttu-id="70a60-119">Valor</span><span class="sxs-lookup"><span data-stu-id="70a60-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a60-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70a60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70a60-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="70a60-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70a60-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70a60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70a60-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="70a60-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="70a60-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70a60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="70a60-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="70a60-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="70a60-126">DLL</span><span class="sxs-lookup"><span data-stu-id="70a60-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70a60-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a60-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="70a60-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="70a60-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70a60-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="70a60-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="70a60-130">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="70a60-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

