---
description: Representa as correspondências de palavras de reconhecimento de manuscrito possíveis para objetos IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interface IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164560"
---
# <a name="ianalysisalternate-interface"></a><span data-ttu-id="0bed5-103">Interface IAnalysisAlternate</span><span class="sxs-lookup"><span data-stu-id="0bed5-103">IAnalysisAlternate interface</span></span>

<span data-ttu-id="0bed5-104">Representa as correspondências de palavras de reconhecimento de manuscrito possíveis para objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="0bed5-104">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="0bed5-105">Membros</span><span class="sxs-lookup"><span data-stu-id="0bed5-105">Members</span></span>

<span data-ttu-id="0bed5-106">A interface **IAnalysisAlternate** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0bed5-106">The **IAnalysisAlternate** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0bed5-107">**IAnalysisAlternate** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0bed5-107">**IAnalysisAlternate** also has these types of members:</span></span>

-   [<span data-ttu-id="0bed5-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="0bed5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0bed5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="0bed5-109">Methods</span></span>

<span data-ttu-id="0bed5-110">A interface **IAnalysisAlternate** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0bed5-110">The **IAnalysisAlternate** interface has these methods.</span></span>



| <span data-ttu-id="0bed5-111">Método</span><span class="sxs-lookup"><span data-stu-id="0bed5-111">Method</span></span>                                                                          | <span data-ttu-id="0bed5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bed5-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0bed5-113">**GetAlternateNodes**</span><span class="sxs-lookup"><span data-stu-id="0bed5-113">**GetAlternateNodes**</span></span>](ianalysisalternate-getalternatenodes.md)               | <span data-ttu-id="0bed5-114">Recupera os objetos [**IContextNode**](icontextnode.md) que estão associados a essa alternativa.</span><span class="sxs-lookup"><span data-stu-id="0bed5-114">Retrieves the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span><br/>                                                       |
| [<span data-ttu-id="0bed5-115">**GetRecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="0bed5-115">**GetRecognitionConfidence**</span></span>](ianalysisalternate-getrecognitionconfidence.md) | <span data-ttu-id="0bed5-116">Recupera um valor que indica o nível de confiança que o [**IInkAnalyzer**](iinkanalyzer.md) tem na precisão do **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="0bed5-116">Retrieves a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the **IAnalysisAlternate**.</span></span><br/> |
| [<span data-ttu-id="0bed5-117">**Reconhecívelstring**</span><span class="sxs-lookup"><span data-stu-id="0bed5-117">**GetRecognizedString**</span></span>](ianalysisalternate-getrecognizedstring.md)           | <span data-ttu-id="0bed5-118">Recupera o valor de cadeia de caracteres reconhecido do objeto **IAnalysisAlternate** .</span><span class="sxs-lookup"><span data-stu-id="0bed5-118">Retrieves the recognized string value of the **IAnalysisAlternate** object.</span></span><br/>                                                                               |
| [<span data-ttu-id="0bed5-119">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="0bed5-119">**GetStrokeIds**</span></span>](ianalysisalternate-getstrokeids.md)                         | <span data-ttu-id="0bed5-120">Recupera os identificadores de traço associados a este **IAnalysisAlternate**.</span><span class="sxs-lookup"><span data-stu-id="0bed5-120">Retrieves the stroke identifiers that are associated with this **IAnalysisAlternate**.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0bed5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bed5-121">Remarks</span></span>

<span data-ttu-id="0bed5-122">Há muitas variações no manuscrito dos usuários.</span><span class="sxs-lookup"><span data-stu-id="0bed5-122">There are many variations in users' handwriting.</span></span> <span data-ttu-id="0bed5-123">Por esse motivo, os reconhecedores de manuscrito podem, às vezes, converter manuscrito em texto diferente do que o usuário pretendia.</span><span class="sxs-lookup"><span data-stu-id="0bed5-123">For that reason, handwriting recognizers can sometimes convert handwriting into text that is different from what the user intended.</span></span> <span data-ttu-id="0bed5-124">Quando um [**IInkAnalyzer**](iinkanalyzer.md) executa uma análise em uma coleção de traços, o **IInkAnalyzer** encontra o conjunto de palavras mais provável que o manuscrito representa.</span><span class="sxs-lookup"><span data-stu-id="0bed5-124">When an [**IInkAnalyzer**](iinkanalyzer.md) performs analysis on a collection of strokes, the **IInkAnalyzer** finds the most likely set of words that the handwriting represents.</span></span> <span data-ttu-id="0bed5-125">Além disso, o **IInkAnalyzer** também localiza conjuntos de correspondências de reconhecimento alternativas, que são armazenados em uma coleção [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="0bed5-125">In addition, the **IInkAnalyzer** also finds sets of alternative recognition matches, which are stored in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span> <span data-ttu-id="0bed5-126">Para que um usuário aproveite as alternativas de reconhecimento, você deve criar uma interface do usuário que permita ao usuário selecionar o **IAnalysisAlternate** correto.</span><span class="sxs-lookup"><span data-stu-id="0bed5-126">In order for a user to take advantage of recognition alternates, you must create a user interface that allows the user to select the correct **IAnalysisAlternate**.</span></span>

<span data-ttu-id="0bed5-127">Os objetos **IAnalysisAlternate** geralmente são obtidos por meio do [**método IInkAnalyzer:: getalternativos**](iinkanalyzer-getalternates.md).</span><span class="sxs-lookup"><span data-stu-id="0bed5-127">**IAnalysisAlternate** objects are generally obtained through [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md).</span></span> <span data-ttu-id="0bed5-128">O primeiro objeto **IAnalysisAlternate** na coleção é o que o [**IInkAnalyzer**](iinkanalyzer.md) considera como a alternativa mais provável.</span><span class="sxs-lookup"><span data-stu-id="0bed5-128">The first **IAnalysisAlternate** object in the collection is what the [**IInkAnalyzer**](iinkanalyzer.md) considers to be the most likely alternate.</span></span>

<span data-ttu-id="0bed5-129">Essa interface é equivalente a [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) na .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0bed5-129">This interface is equivalent to [System.Windows.Ink.AnalysisCore.AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bed5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bed5-130">Requirements</span></span>



| <span data-ttu-id="0bed5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bed5-131">Requirement</span></span> | <span data-ttu-id="0bed5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0bed5-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bed5-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bed5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0bed5-134">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0bed5-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0bed5-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0bed5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0bed5-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0bed5-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0bed5-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bed5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bed5-138"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0bed5-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0bed5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0bed5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bed5-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bed5-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0bed5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bed5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bed5-142">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="0bed5-142">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="0bed5-143">**Método IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="0bed5-143">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="0bed5-144">**Método IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="0bed5-144">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="0bed5-145">**Método IInkAnalyzer:: getalternations**</span><span class="sxs-lookup"><span data-stu-id="0bed5-145">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="0bed5-146">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="0bed5-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

