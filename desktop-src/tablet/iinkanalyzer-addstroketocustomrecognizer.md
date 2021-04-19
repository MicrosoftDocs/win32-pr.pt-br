---
description: Adiciona dados de traço para um único traço para um nó de reconhecedor personalizado.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'Método IInkAnalyzer:: AddStrokeToCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772538"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a><span data-ttu-id="8cb81-103">Método IInkAnalyzer:: AddStrokeToCustomRecognizer</span><span class="sxs-lookup"><span data-stu-id="8cb81-103">IInkAnalyzer::AddStrokeToCustomRecognizer method</span></span>

<span data-ttu-id="8cb81-104">Adiciona dados de traço para um único traço para um nó de reconhecedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="8cb81-104">Adds stroke data for a single stroke to a custom recognizer node.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb81-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cb81-105">Syntax</span></span>


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="8cb81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cb81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cb81-107">*ulStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-107">*ulStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb81-108">O identificador do traço a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="8cb81-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="8cb81-109">*ulStrokePacketDataCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb81-110">O número de pacotes no traço.</span><span class="sxs-lookup"><span data-stu-id="8cb81-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8cb81-111">*plStrokePacketData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb81-112">Uma matriz que contém os dados de pacote para o traço.</span><span class="sxs-lookup"><span data-stu-id="8cb81-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8cb81-113">*ulStrokePacketDescriptionCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb81-114">O número de propriedades do pacote em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="8cb81-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="8cb81-115">*pStrokePacketDescriptionGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb81-116">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="8cb81-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="8cb81-117">*pCustomRecognizer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-117">*pCustomRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb81-118">O [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** ao qual adicionar o traço.</span><span class="sxs-lookup"><span data-stu-id="8cb81-118">The [**IContextNode**](icontextnode.md) of type **CustomRecognizer** to which to add the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="8cb81-119">*ppContextNodeStrokeAddedTo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8cb81-120">O [**IContextNode**](icontextnode.md) para o qual o analisador de tinta adicionou o traço.</span><span class="sxs-lookup"><span data-stu-id="8cb81-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cb81-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cb81-121">Return value</span></span>

<span data-ttu-id="8cb81-122">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8cb81-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cb81-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cb81-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8cb81-124">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="8cb81-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="8cb81-125">Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="8cb81-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="8cb81-126">O [**IInkAnalyzer**](iinkanalyzer.md) adiciona o traço a um [**IContextNode**](icontextnode.md) do tipo **CustomRecognizer** (consulte [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="8cb81-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type **CustomRecognizer** (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="8cb81-127">Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="8cb81-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="8cb81-128">O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo ao traço e adiciona o traço ao primeiro nó **UnclassifiedInk** sob o nó **CustomRecognizer** .</span><span class="sxs-lookup"><span data-stu-id="8cb81-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first **UnclassifiedInk** node under the **CustomRecognizer** node.</span></span> <span data-ttu-id="8cb81-129">Se não existir nenhum nó **UnclassifiedInk** , ele será criado.</span><span class="sxs-lookup"><span data-stu-id="8cb81-129">If no **UnclassifiedInk** node exists, it is created.</span></span> <span data-ttu-id="8cb81-130">Se o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associado ao nó **CustomRecognizer** não oferecer suporte ao identificador de cultura, o **IInkAnalyzer** continuará analisando e gera um aviso de [**IAnalysisWarning**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="8cb81-130">If the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associated with the **CustomRecognizer** node does not support the culture identifier, the **IInkAnalyzer** continues analyzing and generates an [**IAnalysisWarning**](ianalysiswarning.md) warning.</span></span> <span data-ttu-id="8cb81-131">Esse aviso tem um valor [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ LanguageIdNotRespected**.</span><span class="sxs-lookup"><span data-stu-id="8cb81-131">This warning has an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_LanguageIdNotRespected**.</span></span>

<span data-ttu-id="8cb81-132">*plStrokePacketData* contém dados de pacote para todos os pontos no traço.</span><span class="sxs-lookup"><span data-stu-id="8cb81-132">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="8cb81-133">*pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço.</span><span class="sxs-lookup"><span data-stu-id="8cb81-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="8cb81-134">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8cb81-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="8cb81-135">Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora do traço adicionado.</span><span class="sxs-lookup"><span data-stu-id="8cb81-135">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="8cb81-136">O [**IInkAnalyzer**](iinkanalyzer.md) retorna um **HRESULT** de **E \_ INVALIDARG** sob as circunstâncias a seguir.</span><span class="sxs-lookup"><span data-stu-id="8cb81-136">The [**IInkAnalyzer**](iinkanalyzer.md) returns an **HRESULT** of **E\_INVALIDARG** under the following circumstances.</span></span>

-   <span data-ttu-id="8cb81-137">O [**IInkAnalyzer**](iinkanalyzer.md) já contém um traço com o mesmo identificador que o traço a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="8cb81-137">The [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as the stroke to be added.</span></span>
-   <span data-ttu-id="8cb81-138">O parâmetro *pCustomRecognizer* contém um nó de reconhecedor personalizado que está associado a um objeto [**IInkAnalyzer**](iinkanalyzer.md) diferente.</span><span class="sxs-lookup"><span data-stu-id="8cb81-138">The *pCustomRecognizer* parameter contains a custom recognizer node that is associated with a different [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>
-   <span data-ttu-id="8cb81-139">O parâmetro *pCustomRecognizer* contém um [**IContextNode**](icontextnode.md) que não é do tipo **CustomRecognizer**.</span><span class="sxs-lookup"><span data-stu-id="8cb81-139">The *pCustomRecognizer* parameter contains an [**IContextNode**](icontextnode.md) that is not of type **CustomRecognizer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cb81-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cb81-140">Requirements</span></span>



| <span data-ttu-id="8cb81-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb81-141">Requirement</span></span> | <span data-ttu-id="8cb81-142">Valor</span><span class="sxs-lookup"><span data-stu-id="8cb81-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb81-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb81-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb81-144">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8cb81-144">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8cb81-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb81-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb81-146">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8cb81-146">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8cb81-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cb81-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cb81-148"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8cb81-148"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8cb81-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8cb81-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cb81-150"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cb81-150"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8cb81-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cb81-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb81-152">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="8cb81-152">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="8cb81-153">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="8cb81-153">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="8cb81-154">**Método IInkAnalyzer:: AddStrokesToCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="8cb81-154">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8cb81-155">**Método IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="8cb81-155">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8cb81-156">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="8cb81-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

