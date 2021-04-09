---
description: Recupera os recursos do reconhecedor.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'Método IInkAnalysisRecognizer:: GetCapabilities (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090535"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a><span data-ttu-id="2c590-103">Método IInkAnalysisRecognizer:: GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="2c590-103">IInkAnalysisRecognizer::GetCapabilities method</span></span>

<span data-ttu-id="2c590-104">Recupera os recursos do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="2c590-104">Retrieves the capabilities of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c590-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c590-105">Syntax</span></span>


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="2c590-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c590-107">*pCapabilities* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2c590-107">*pCapabilities* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c590-108">Uma combinação de bits de valor [**RecognizerCapabilities**](recognizercapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="2c590-108">A bitwise combination of [**RecognizerCapabilities**](recognizercapabilities.md) values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c590-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c590-109">Return value</span></span>

<span data-ttu-id="2c590-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2c590-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c590-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c590-111">Remarks</span></span>

<span data-ttu-id="2c590-112">Esse valor é constante para cada [ **IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span><span class="sxs-lookup"><span data-stu-id="2c590-112">This value is constant for each [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="2c590-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c590-113">Requirements</span></span>



| <span data-ttu-id="2c590-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c590-114">Requirement</span></span> | <span data-ttu-id="2c590-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2c590-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c590-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c590-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2c590-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2c590-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2c590-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c590-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2c590-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2c590-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2c590-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c590-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c590-121"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2c590-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2c590-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2c590-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c590-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c590-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2c590-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c590-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c590-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="2c590-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="2c590-126">**RecognizerCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2c590-126">**RecognizerCapabilities**</span></span>](recognizercapabilities.md)
</dt> <dt>

[<span data-ttu-id="2c590-127">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="2c590-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




