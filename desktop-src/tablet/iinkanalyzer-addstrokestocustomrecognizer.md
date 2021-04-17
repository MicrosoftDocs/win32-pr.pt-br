---
description: Adiciona dados de traço para vários traços a um nó de reconhecedor personalizado.
ms.assetid: 77ded896-8573-42de-a41e-4866894dfe2b
title: 'Método IInkAnalyzer:: AddStrokesToCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6df1b31957f3b4087b51fbad0e7b527c2ede799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768283"
---
# <a name="iinkanalyzeraddstrokestocustomrecognizer-method"></a><span data-ttu-id="ee583-103">Método IInkAnalyzer:: AddStrokesToCustomRecognizer</span><span class="sxs-lookup"><span data-stu-id="ee583-103">IInkAnalyzer::AddStrokesToCustomRecognizer method</span></span>

<span data-ttu-id="ee583-104">Adiciona dados de traço para vários traços a um nó de reconhecedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="ee583-104">Adds stroke data for multiple strokes to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee583-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee583-105">Syntax</span></span>


```C++
HRESULT AddStrokesToCustomRecognizer(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="ee583-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee583-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee583-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-108">O número de traços a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="ee583-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="ee583-109">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee583-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-110">Uma matriz que contém os identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="ee583-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ee583-111">*ulStrokePacketDescriptionCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee583-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-112">O número de propriedades em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="ee583-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="ee583-113">*pStrokePacketDescriptionGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee583-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-114">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="ee583-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="ee583-115">*pulPacketDataCountPerStroke* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee583-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-116">Uma matriz que contém o número de pacotes em cada traço.</span><span class="sxs-lookup"><span data-stu-id="ee583-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="ee583-117">*plStrokePacketData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee583-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-118">Uma matriz que contém os dados de pacote para os traços.</span><span class="sxs-lookup"><span data-stu-id="ee583-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="ee583-119">*pCustomRecognizer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee583-119">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-120">O [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** ao qual adicionar os traços.</span><span class="sxs-lookup"><span data-stu-id="ee583-120">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="ee583-121">*ppContextNodeStrokeAddedTo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee583-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee583-122">O [**IContextNode**](icontextnode.md) para o qual o analisador de tinta adicionou os traços.</span><span class="sxs-lookup"><span data-stu-id="ee583-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee583-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee583-123">Return value</span></span>

<span data-ttu-id="ee583-124">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ee583-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee583-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee583-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ee583-126">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="ee583-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ee583-127">Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="ee583-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="ee583-128">O [**IInkAnalyzer**](iinkanalyzer.md) adiciona os traços a um [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** (consulte [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="ee583-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="ee583-129">Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="ee583-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="ee583-130">O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo aos traços e adiciona os traços ao primeiro nó **UnclassifiedInk** sob o nó **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="ee583-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="ee583-131">Se não existir nenhum nó **UnclassifiedInk** , ele será criado.</span><span class="sxs-lookup"><span data-stu-id="ee583-131">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="ee583-132">Se o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associado ao nó **CustomRecognizer** não oferecer suporte ao identificador de cultura, o **IInkAnalyzer** continuará analisando e gera um aviso de [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="ee583-132">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="ee583-133">Esse aviso tem um valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="ee583-133">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="ee583-134">*plStrokePacketData* contém dados de pacote para todos os traços.</span><span class="sxs-lookup"><span data-stu-id="ee583-134">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="ee583-135">*pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço.</span><span class="sxs-lookup"><span data-stu-id="ee583-135">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="ee583-136">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ee583-136">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="ee583-137">Somente traços com as mesmas descrições de pacote podem ser adicionados em uma única chamada para o **método IInkAnalyzer:: AddStrokesToCustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="ee583-137">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokesToCustomRecognizer Method**.</span></span>

 

<span data-ttu-id="ee583-138">Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora dos traços adicionados.</span><span class="sxs-lookup"><span data-stu-id="ee583-138">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="ee583-139">O [**IInkAnalyzer**](iinkanalyzer.md) retorna um **HRESULT** de **E \_ INVALIDARG** sob as circunstâncias a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee583-139">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="ee583-140">O [**IInkAnalyzer**](iinkanalyzer.md) já contém um traço com o mesmo identificador de um dos traços a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="ee583-140">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added.</span></span>
-   <span data-ttu-id="ee583-141">O parâmetro *pCustomRecognizer* contém um nó de reconhecedor personalizado que está associado a um objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.</span><span class="sxs-lookup"><span data-stu-id="ee583-141">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="ee583-142">O parâmetro *pCustomRecognizer* contém um [**IContextNode**](icontextnode.md) que não é do tipo **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="ee583-142">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee583-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee583-143">Requirements</span></span>



| <span data-ttu-id="ee583-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee583-144">Requirement</span></span> | <span data-ttu-id="ee583-145">Valor</span><span class="sxs-lookup"><span data-stu-id="ee583-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee583-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee583-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ee583-147">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ee583-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ee583-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ee583-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ee583-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ee583-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ee583-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee583-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee583-151"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ee583-151"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee583-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ee583-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee583-153"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee583-153"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ee583-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee583-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee583-155">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ee583-155">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ee583-156">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="ee583-156">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="ee583-157">**Método IInkAnalyzer:: AddStrokeToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="ee583-157">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ee583-158">**Método IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="ee583-158">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ee583-159">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="ee583-159">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

