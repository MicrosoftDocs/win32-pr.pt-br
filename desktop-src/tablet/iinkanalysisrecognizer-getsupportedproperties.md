---
description: Recupera os identificadores globalmente exclusivos (GUIDs) para as propriedades que esse IInkAnalysisRecognizer pode gerar para os resultados da análise.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'Método IInkAnalysisRecognizer:: GetSupportedProperties (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920953"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a><span data-ttu-id="279ba-103">Método IInkAnalysisRecognizer:: GetSupportedProperties</span><span class="sxs-lookup"><span data-stu-id="279ba-103">IInkAnalysisRecognizer::GetSupportedProperties method</span></span>

<span data-ttu-id="279ba-104">Recupera os identificadores globalmente exclusivos (GUIDs) para as propriedades que esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pode gerar para os resultados da análise.</span><span class="sxs-lookup"><span data-stu-id="279ba-104">Retrieves the globally unique identifiers (GUIDs) for the properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

## <a name="syntax"></a><span data-ttu-id="279ba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="279ba-105">Syntax</span></span>


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="279ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="279ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="279ba-107">*pulPropertiesCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="279ba-107">*pulPropertiesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="279ba-108">O número de GUIDs em *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="279ba-108">The number of GUIDs in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="279ba-109">*ppProperties* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="279ba-109">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="279ba-110">Um ponteiro para os GUIDs de propriedades que esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pode gerar para resultados de análise.</span><span class="sxs-lookup"><span data-stu-id="279ba-110">A pointer to the GUIDs of properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="279ba-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="279ba-111">Return value</span></span>

<span data-ttu-id="279ba-112">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="279ba-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="279ba-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="279ba-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="279ba-114">Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppProperties* quando você não precisar mais das informações.</span><span class="sxs-lookup"><span data-stu-id="279ba-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppProperties* when you no longer need the information.</span></span>

 

<span data-ttu-id="279ba-115">Um reconhecedor pode dar suporte A métricas de linha, números de linha, níveis de confiança e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="279ba-115">A recognizer can support line metrics, line numbers, confidence levels, and so on.</span></span> <span data-ttu-id="279ba-116">Para obter uma lista completa das propriedades às quais um reconhecedor pode dar suporte, consulte [constantes](recognitionproperty-constants.md)recognizeproperty.</span><span class="sxs-lookup"><span data-stu-id="279ba-116">For a complete list of the properties that a recognizer can support, see [RecognitionProperty Constants](recognitionproperty-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="279ba-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="279ba-117">Requirements</span></span>



| <span data-ttu-id="279ba-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="279ba-118">Requirement</span></span> | <span data-ttu-id="279ba-119">Valor</span><span class="sxs-lookup"><span data-stu-id="279ba-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="279ba-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="279ba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="279ba-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="279ba-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="279ba-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="279ba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="279ba-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="279ba-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="279ba-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="279ba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="279ba-125"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="279ba-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="279ba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="279ba-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="279ba-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279ba-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="279ba-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="279ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279ba-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="279ba-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="279ba-130">Constantes rerecognitionproperty</span><span class="sxs-lookup"><span data-stu-id="279ba-130">RecognitionProperty Constants</span></span>](recognitionproperty-constants.md)
</dt> <dt>

[<span data-ttu-id="279ba-131">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="279ba-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

