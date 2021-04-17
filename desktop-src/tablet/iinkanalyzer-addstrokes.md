---
description: Adiciona dados de traço para vários traços ao IInkAnalyzer e atribui o identificador de cultura do thread de entrada ativo aos traços.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'Método IInkAnalyzer:: AddStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811529"
---
# <a name="iinkanalyzeraddstrokes-method"></a><span data-ttu-id="fa835-103">Método IInkAnalyzer:: AddStrokes</span><span class="sxs-lookup"><span data-stu-id="fa835-103">IInkAnalyzer::AddStrokes method</span></span>

<span data-ttu-id="fa835-104">Adiciona dados de traço para vários traços ao [**IInkAnalyzer**](iinkanalyzer.md) e atribui o identificador de cultura do thread de entrada ativo aos traços.</span><span class="sxs-lookup"><span data-stu-id="fa835-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa835-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa835-105">Syntax</span></span>


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="fa835-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa835-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa835-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa835-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa835-108">O número de traços a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="fa835-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="fa835-109">*plStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa835-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa835-110">Uma matriz que contém os identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="fa835-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="fa835-111">*ulStrokePacketDescriptionCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa835-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa835-112">O número de propriedades em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="fa835-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="fa835-113">*pStrokePacketDescriptionGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa835-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa835-114">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="fa835-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="fa835-115">*pulPacketDataCountPerStroke* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa835-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa835-116">Uma matriz que contém o número de pacotes em cada traço.</span><span class="sxs-lookup"><span data-stu-id="fa835-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="fa835-117">*plStrokePacketData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa835-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa835-118">Uma matriz que contém os dados de pacote para os traços.</span><span class="sxs-lookup"><span data-stu-id="fa835-118">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="fa835-119">*ppContextNodeStrokeAddedTo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa835-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa835-120">O [**IContextNode**](icontextnode.md) para o qual o analisador de tinta adicionou os traços.</span><span class="sxs-lookup"><span data-stu-id="fa835-120">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa835-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa835-121">Return value</span></span>

<span data-ttu-id="fa835-122">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fa835-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa835-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa835-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fa835-124">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="fa835-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="fa835-125">Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="fa835-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="fa835-126">O [**IInkAnalyzer**](iinkanalyzer.md) adiciona os traços a um [**IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="fa835-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="fa835-127">Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="fa835-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="fa835-128">O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo aos traços e adiciona os traços ao primeiro nó de contexto UnclassifiedInk no nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura.</span><span class="sxs-lookup"><span data-stu-id="fa835-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="fa835-129">Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk sob seu nó raiz e adicionará os traços ao novo nó de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="fa835-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="fa835-130">*plStrokePacketData* contém dados de pacote para todos os traços.</span><span class="sxs-lookup"><span data-stu-id="fa835-130">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="fa835-131">*pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço.</span><span class="sxs-lookup"><span data-stu-id="fa835-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="fa835-132">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fa835-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="fa835-133">Somente traços com as mesmas descrições de pacote podem ser adicionados em uma única chamada para o **método IInkAnalyzer:: AddStrokes**.</span><span class="sxs-lookup"><span data-stu-id="fa835-133">Only strokes with the same packet descriptions can be added in a single call to **IInkAnalyzer::AddStrokes Method**.</span></span>

 

<span data-ttu-id="fa835-134">Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora dos traços adicionados.</span><span class="sxs-lookup"><span data-stu-id="fa835-134">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="fa835-135">Se o [**IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador de um dos traços a serem adicionados, o **IInkAnalyzer** retornará um **HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="fa835-135">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa835-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa835-136">Requirements</span></span>



| <span data-ttu-id="fa835-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa835-137">Requirement</span></span> | <span data-ttu-id="fa835-138">Valor</span><span class="sxs-lookup"><span data-stu-id="fa835-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa835-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa835-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fa835-140">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="fa835-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fa835-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa835-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fa835-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fa835-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fa835-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa835-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa835-144"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fa835-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa835-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fa835-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa835-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa835-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fa835-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa835-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa835-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fa835-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fa835-149">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="fa835-149">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="fa835-150">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="fa835-150">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="fa835-151">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="fa835-151">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="fa835-152">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="fa835-152">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="fa835-153">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="fa835-153">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="fa835-154">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="fa835-154">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

