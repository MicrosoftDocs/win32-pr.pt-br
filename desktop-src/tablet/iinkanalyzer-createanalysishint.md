---
description: Adiciona um novo nó de dica de análise com uma área infinita ao IInkAnalyzer.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'Método IInkAnalyzer:: CreateAnalysisHint (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296390"
---
# <a name="iinkanalyzercreateanalysishint-method"></a><span data-ttu-id="1c2b1-103">Método IInkAnalyzer:: CreateAnalysisHint</span><span class="sxs-lookup"><span data-stu-id="1c2b1-103">IInkAnalyzer::CreateAnalysisHint method</span></span>

<span data-ttu-id="1c2b1-104">Adiciona um novo nó de dica de análise com uma área infinita ao [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="1c2b1-104">Adds a new analysis hint node with an infinite area to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c2b1-105">Syntax</span></span>


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="1c2b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c2b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c2b1-107">*ppAnalysisHint* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1c2b1-107">*ppAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2b1-108">O novo nó de dica de análise.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-108">The new analysis hint node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c2b1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c2b1-109">Return value</span></span>

<span data-ttu-id="1c2b1-110">Consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md) para obter uma descrição dos valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-110">See [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) for a description of the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c2b1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c2b1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1c2b1-112">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppAnalysisHint* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHint* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="1c2b1-113">Para fornecer informações adicionais de contexto para o [**IInkAnalyzer**](iinkanalyzer.md), você pode adicionar dicas de análise ao analisador de tinta.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-113">To provide extra context information for the [**IInkAnalyzer**](iinkanalyzer.md), you can add analysis hints to the ink analyzer.</span></span> <span data-ttu-id="1c2b1-114">As dicas de análise podem melhorar a precisão do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-114">Analysis hints can improve recognition accuracy.</span></span> <span data-ttu-id="1c2b1-115">Por exemplo, você pode adicionar informações de factor e de guia para campos em um aplicativo de formulário.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-115">For example, you can add factoid and guide information for fields in a form application.</span></span>

<span data-ttu-id="1c2b1-116">Esse método cria um novo [**IContextNode**](icontextnode.md) com um tipo de nó de contexto AnalysisHint (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)) e adiciona a nova dica como um subnó do nó raiz do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o método [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="1c2b1-116">This method creates a new [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)) and adds the new hint as a subnode of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="1c2b1-117">Para adicionar informações de contexto à dica, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) com o parâmetro *pPropertyDataId* definido como uma das constantes de [Propriedades de dica de análise](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="1c2b1-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="1c2b1-118">Se uma dica for atribuída a uma área infinita, com o termo de uma dica global, o [**IInkAnalyzer**](iinkanalyzer.md) aplicará o contexto da dica a toda a tinta que não está dentro da área de outra dica.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-118">If a hint is assigned an infinite area, termed a global hint, the [**IInkAnalyzer**](iinkanalyzer.md) applies the hint's context to all ink that is not within another hint's area.</span></span> <span data-ttu-id="1c2b1-119">Várias dicas podem ser anexadas a um único **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-119">Multiple hints may be attached to a single **IInkAnalyzer**.</span></span> <span data-ttu-id="1c2b1-120">No entanto, apenas uma dica global pode ser anexada a um único analisador de tinta e não há dicas globais que podem se sobrepor.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-120">However, only one global hint can be attached to a single ink analyzer, and no non-global hints can overlap.</span></span> <span data-ttu-id="1c2b1-121">Para obter mais informações sobre os tipos de informações de contexto que podem ser fornecidas por uma dica, consulte [Propriedades de dica de análise](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1c2b1-121">For more information about the types of context information that a hint can provide, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="1c2b1-122">A adição de uma dica de análise não marca a área da dica para reanálise.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-122">Adding an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="1c2b1-123">Para marcar a área dentro da dica para reanálise, use o [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para definir a região suja como a União da região suja atual e da área da dica de análise.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-123">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="1c2b1-124">Ao usar dicas para um aplicativo de formulário, o aplicativo deve evitar misturar o contexto de texto com tinta nos formulários.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-124">When using hints for a form application, the application should avoid mixing text context with ink in the forms.</span></span> <span data-ttu-id="1c2b1-125">Isso significa, por exemplo, que os nomes de campo de texto não devem ser criados na árvore de análise.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-125">This means for example that text field names should not be created in the analysis tree.</span></span> <span data-ttu-id="1c2b1-126">As dicas destinam-se a associar a tinta a áreas em páginas; qualquer contexto de texto interfere nessa associação de tinta para dica.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-126">Hints are meant to associate the ink to areas on pages; any text context interferes with this ink-to-hint association.</span></span> <span data-ttu-id="1c2b1-127">A operação de análise pode mesclar a tinta e o contexto de texto na mesma região de escrita, o que impediria que a tinta fosse associada à área de dica.</span><span class="sxs-lookup"><span data-stu-id="1c2b1-127">The analysis operation may merge the ink and the text context in the same writing region which would prevent the ink from being associated with the hint area.</span></span>

<span data-ttu-id="1c2b1-128">Para obter mais informações sobre a análise de tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1c2b1-128">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c2b1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c2b1-129">Requirements</span></span>



| <span data-ttu-id="1c2b1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c2b1-130">Requirement</span></span> | <span data-ttu-id="1c2b1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1c2b1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2b1-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c2b1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1c2b1-133">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1c2b1-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1c2b1-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c2b1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1c2b1-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1c2b1-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1c2b1-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c2b1-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c2b1-137"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1c2b1-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1c2b1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1c2b1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c2b1-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c2b1-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1c2b1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c2b1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2b1-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1c2b1-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1c2b1-142">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="1c2b1-142">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="1c2b1-143">**IInkAnalyzer: método eleteAnalysisHint de:D**</span><span class="sxs-lookup"><span data-stu-id="1c2b1-143">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="1c2b1-144">**Método IInkAnalyzer:: GetAnalysisHints**</span><span class="sxs-lookup"><span data-stu-id="1c2b1-144">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="1c2b1-145">**Método IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="1c2b1-145">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="1c2b1-146">Propriedades da dica de análise</span><span class="sxs-lookup"><span data-stu-id="1c2b1-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="1c2b1-147">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="1c2b1-147">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

