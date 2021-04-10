---
description: Adiciona dados de traço para vários traços ao IInkAnalyzer e atribui o identificador de cultura especificado aos traços.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: 'Método IInkAnalyzer:: AddStrokesForLanguage (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7f1c8bde9f1fe9d9c7123fa3c40540d0fd2660ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164544"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a><span data-ttu-id="30b28-103">Método IInkAnalyzer:: AddStrokesForLanguage</span><span class="sxs-lookup"><span data-stu-id="30b28-103">IInkAnalyzer::AddStrokesForLanguage method</span></span>

<span data-ttu-id="30b28-104">Adiciona dados de traço para vários traços ao [**IInkAnalyzer**](iinkanalyzer.md) e atribui o identificador de cultura especificado aos traços.</span><span class="sxs-lookup"><span data-stu-id="30b28-104">Adds stroke data for multiple strokes to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the specified culture identifier to the strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b28-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30b28-105">Syntax</span></span>


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="30b28-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30b28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b28-107">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30b28-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-108">O número de traços a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="30b28-108">The number of strokes to add.</span></span>

</dd> <dt>

<span data-ttu-id="30b28-109">*plIdofStrokesToAdd* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30b28-109">*plIdofStrokesToAdd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-110">Uma matriz que contém os identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="30b28-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="30b28-111">*lStrokesLCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30b28-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-112">Um valor que representa o identificador de cultura a ser atribuído aos traços.</span><span class="sxs-lookup"><span data-stu-id="30b28-112">A value that represents the culture identifier to assign to the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="30b28-113">*ulStrokePacketDescriptionCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30b28-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-114">O número de propriedades em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="30b28-114">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="30b28-115">*pStrokePacketDescriptionGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30b28-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-116">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="30b28-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="30b28-117">*pulPacketDataCountPerStroke* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30b28-117">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-118">Uma matriz que contém o número de pacotes em cada traço.</span><span class="sxs-lookup"><span data-stu-id="30b28-118">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="30b28-119">*plStrokePacketData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30b28-119">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-120">Uma matriz que contém os dados de pacote para os traços.</span><span class="sxs-lookup"><span data-stu-id="30b28-120">An array containing the packet data for the strokes.</span></span>

</dd> <dt>

<span data-ttu-id="30b28-121">*ppContextNodeStrokeAddedTo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="30b28-121">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30b28-122">O [**IContextNode**](icontextnode.md) para o qual o analisador de tinta adicionou os traços.</span><span class="sxs-lookup"><span data-stu-id="30b28-122">The [**IContextNode**](icontextnode.md) to which the ink analyzer added the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b28-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30b28-123">Return value</span></span>

<span data-ttu-id="30b28-124">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="30b28-124">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30b28-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="30b28-125">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="30b28-126">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="30b28-126">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="30b28-127">Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="30b28-127">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="30b28-128">O [**IInkAnalyzer**](iinkanalyzer.md) adiciona os traços a um [**IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="30b28-128">The [**IInkAnalyzer**](iinkanalyzer.md) adds the strokes to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="30b28-129">Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="30b28-129">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="30b28-130">O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura *lStrokeLCID* aos traços e adiciona os traços ao primeiro nó de contexto UnclassifiedInk no nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura.</span><span class="sxs-lookup"><span data-stu-id="30b28-130">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the *lStrokeLCID* culture identifier to the strokes and adds the strokes to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="30b28-131">Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk sob seu nó raiz e adicionará os traços ao novo nó de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="30b28-131">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the strokes to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="30b28-132">*plStrokePacketData* contém dados de pacote para todos os traços.</span><span class="sxs-lookup"><span data-stu-id="30b28-132">*plStrokePacketData* contains packet data for all of the strokes.</span></span> <span data-ttu-id="30b28-133">*pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto em cada traço.</span><span class="sxs-lookup"><span data-stu-id="30b28-133">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="30b28-134">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="30b28-134">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="30b28-135">Somente traços com as mesmas descrições de pacote podem ser adicionados em uma única chamada para o [**método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md).</span><span class="sxs-lookup"><span data-stu-id="30b28-135">Only strokes with the same packet descriptions can be added in a single call to [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md).</span></span>

 

<span data-ttu-id="30b28-136">Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora dos traços adicionados.</span><span class="sxs-lookup"><span data-stu-id="30b28-136">This method expands the dirty region to the union of the region's current value and the bounding box of the added strokes.</span></span>

<span data-ttu-id="30b28-137">Se o [**IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador de um dos traços a serem adicionados, o **IInkAnalyzer** retornará um **HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="30b28-137">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same identifier as one of the strokes to be added, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b28-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b28-138">Requirements</span></span>



| <span data-ttu-id="30b28-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="30b28-139">Requirement</span></span> | <span data-ttu-id="30b28-140">Valor</span><span class="sxs-lookup"><span data-stu-id="30b28-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b28-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30b28-141">Minimum supported client</span></span><br/> | <span data-ttu-id="30b28-142">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="30b28-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30b28-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30b28-143">Minimum supported server</span></span><br/> | <span data-ttu-id="30b28-144">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="30b28-144">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="30b28-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30b28-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b28-146"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="30b28-146"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30b28-147">DLL</span><span class="sxs-lookup"><span data-stu-id="30b28-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30b28-148"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30b28-148"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="30b28-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="30b28-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b28-150">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="30b28-150">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="30b28-151">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="30b28-151">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="30b28-152">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="30b28-152">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="30b28-153">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="30b28-153">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="30b28-154">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="30b28-154">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="30b28-155">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="30b28-155">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="30b28-156">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="30b28-156">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

