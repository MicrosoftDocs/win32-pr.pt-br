---
description: Contém uma coleção de objetos que implementam a interface IInkAnalysisRecognizer e que representam a capacidade de reconhecer manuscritos, objetos ou gestos.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interface IInkAnalysisRecognizers (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296392"
---
# <a name="iinkanalysisrecognizers-interface"></a><span data-ttu-id="7aa6e-103">Interface IInkAnalysisRecognizers</span><span class="sxs-lookup"><span data-stu-id="7aa6e-103">IInkAnalysisRecognizers interface</span></span>

<span data-ttu-id="7aa6e-104">Contém uma coleção de objetos que implementam a interface [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) e que representam a capacidade de reconhecer manuscritos, objetos ou gestos.</span><span class="sxs-lookup"><span data-stu-id="7aa6e-104">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span>

## <a name="members"></a><span data-ttu-id="7aa6e-105">Membros</span><span class="sxs-lookup"><span data-stu-id="7aa6e-105">Members</span></span>

<span data-ttu-id="7aa6e-106">A interface **IInkAnalysisRecognizers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7aa6e-106">The **IInkAnalysisRecognizers** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7aa6e-107">**IInkAnalysisRecognizers** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7aa6e-107">**IInkAnalysisRecognizers** also has these types of members:</span></span>

-   [<span data-ttu-id="7aa6e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7aa6e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7aa6e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7aa6e-109">Methods</span></span>

<span data-ttu-id="7aa6e-110">A interface **IInkAnalysisRecognizers** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7aa6e-110">The **IInkAnalysisRecognizers** interface has these methods.</span></span>



| <span data-ttu-id="7aa6e-111">Método</span><span class="sxs-lookup"><span data-stu-id="7aa6e-111">Method</span></span>                                                                               | <span data-ttu-id="7aa6e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aa6e-112">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7aa6e-113">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="7aa6e-113">**GetCount**</span></span>](iinkanalysisrecognizers-getcount.md)                                 | <span data-ttu-id="7aa6e-114">Recupera o número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="7aa6e-114">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span><br/> |
| [<span data-ttu-id="7aa6e-115">**GetInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="7aa6e-115">**GetInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | <span data-ttu-id="7aa6e-116">Recupera o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7aa6e-116">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="7aa6e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7aa6e-117">Remarks</span></span>

<span data-ttu-id="7aa6e-118">O método do [**método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) de [**IInkAnalyzer**](iinkanalyzer.md) retorna uma coleção **IInkAnalysisRecognizers** que contém os reconhecedores de tinta disponíveis no Tablet PC atual.</span><span class="sxs-lookup"><span data-stu-id="7aa6e-118">The [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method of [**IInkAnalyzer**](iinkanalyzer.md) returns an **IInkAnalysisRecognizers** collection containing the ink recognizers available on the current Tablet PC.</span></span>

<span data-ttu-id="7aa6e-119">Para um reconhecedor de linguagem, o método [**IInkAnalysisRecognizer:: Getlinguations**](iinkanalysisrecognizer-getlanguages.md) retorna uma matriz não vazia.</span><span class="sxs-lookup"><span data-stu-id="7aa6e-119">For a language recognizer, the [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) method returns a non-empty array.</span></span> <span data-ttu-id="7aa6e-120">Para os reconhecedores de gestores e os reconhecedores de objetos, o método **IInkAnalysisRecognizer:: GetLanguages** retorna uma matriz vazia.</span><span class="sxs-lookup"><span data-stu-id="7aa6e-120">For both gesture recognizers and object recognizers, the **IInkAnalysisRecognizer::GetLanguages** method returns an empty array.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aa6e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7aa6e-121">Requirements</span></span>



| <span data-ttu-id="7aa6e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7aa6e-122">Requirement</span></span> | <span data-ttu-id="7aa6e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7aa6e-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa6e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7aa6e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa6e-125">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7aa6e-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7aa6e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7aa6e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa6e-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7aa6e-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7aa6e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7aa6e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7aa6e-129"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7aa6e-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7aa6e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7aa6e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aa6e-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aa6e-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7aa6e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7aa6e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aa6e-133">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="7aa6e-133">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="7aa6e-134">**Método IInkAnalyzer:: GetInkAnalysisRecognizersByPriority**</span><span class="sxs-lookup"><span data-stu-id="7aa6e-134">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="7aa6e-135">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="7aa6e-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

