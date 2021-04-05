---
description: Adiciona dados de traço para um único traço para o IInkAnalyzer e atribui um identificador de cultura específico ao traço.
ms.assetid: 65eb805e-05ed-4144-b17e-872c47ab33fa
title: 'Método IInkAnalyzer:: AddStrokeForLanguage (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 674a58ef891d919d09f86f28a35748de3537db91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827181"
---
# <a name="iinkanalyzeraddstrokeforlanguage-method"></a><span data-ttu-id="73884-103">Método IInkAnalyzer:: AddStrokeForLanguage</span><span class="sxs-lookup"><span data-stu-id="73884-103">IInkAnalyzer::AddStrokeForLanguage method</span></span>

<span data-ttu-id="73884-104">Adiciona dados de traço para um único traço para o [**IInkAnalyzer**](iinkanalyzer.md) e atribui um identificador de cultura específico ao traço.</span><span class="sxs-lookup"><span data-stu-id="73884-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns a specific culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="73884-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73884-105">Syntax</span></span>


```C++
HRESULT AddStrokeForLanguage(
  [in]  LONG         lStrokeId,
  [in]  LONG         lStrokeLCID,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="73884-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73884-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73884-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73884-108">O identificador do traço a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="73884-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="73884-109">*lStrokeLCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73884-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73884-110">O identificador de cultura a ser atribuído ao traço.</span><span class="sxs-lookup"><span data-stu-id="73884-110">The culture identifier to assign to the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="73884-111">*ulStrokePacketDataCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73884-111">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73884-112">O número de pacotes no traço.</span><span class="sxs-lookup"><span data-stu-id="73884-112">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="73884-113">*plStrokePacketData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73884-113">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73884-114">Uma matriz que contém os dados de pacote para o traço.</span><span class="sxs-lookup"><span data-stu-id="73884-114">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="73884-115">*ulStrokePacketDescriptionCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73884-115">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73884-116">O número de propriedades em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="73884-116">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="73884-117">*pStrokePacketDescriptionGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73884-117">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73884-118">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="73884-118">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="73884-119">*ppContextNodeStrokeAddedTo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="73884-119">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73884-120">Um ponteiro cujo valor é definido como o ponteiro do [**IContextNode**](icontextnode.md) que contém o traço recém-adicionado.</span><span class="sxs-lookup"><span data-stu-id="73884-120">A pointer whose value is set to the pointer of the [**IContextNode**](icontextnode.md) that contains the newly added stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73884-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73884-121">Return value</span></span>

<span data-ttu-id="73884-122">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="73884-122">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="73884-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="73884-123">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="73884-124">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="73884-124">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="73884-125">Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="73884-125">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="73884-126">O [**IInkAnalyzer**](iinkanalyzer.md) adiciona o traço a um [**IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="73884-126">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="73884-127">Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="73884-127">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="73884-128">O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura *lStrokeLCID* ao traço e adiciona o traço ao primeiro nó de contexto UnclassifiedInk no nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura.</span><span class="sxs-lookup"><span data-stu-id="73884-128">The [**IInkAnalyzer**](iinkanalyzer.md) assigns *lStrokeLCID* culture identifier to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="73884-129">Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk sob seu nó raiz e adicionará o traço ao novo nó de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="73884-129">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="73884-130">*plStrokePacketData* contém dados de pacote para todos os pontos no traço.</span><span class="sxs-lookup"><span data-stu-id="73884-130">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="73884-131">*pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto no traço.</span><span class="sxs-lookup"><span data-stu-id="73884-131">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="73884-132">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="73884-132">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="73884-133">Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora do traço adicionado.</span><span class="sxs-lookup"><span data-stu-id="73884-133">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="73884-134">Se o [**IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador de traço, o **IInkAnalyzer** retornará um **HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="73884-134">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="73884-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73884-135">Requirements</span></span>



| <span data-ttu-id="73884-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="73884-136">Requirement</span></span> | <span data-ttu-id="73884-137">Valor</span><span class="sxs-lookup"><span data-stu-id="73884-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73884-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73884-138">Minimum supported client</span></span><br/> | <span data-ttu-id="73884-139">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="73884-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="73884-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73884-140">Minimum supported server</span></span><br/> | <span data-ttu-id="73884-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="73884-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="73884-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73884-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="73884-143"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="73884-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="73884-144">DLL</span><span class="sxs-lookup"><span data-stu-id="73884-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73884-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73884-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="73884-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="73884-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73884-147">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="73884-147">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="73884-148">**Método IInkAnalyzer:: addstroke**</span><span class="sxs-lookup"><span data-stu-id="73884-148">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="73884-149">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="73884-149">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="73884-150">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="73884-150">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="73884-151">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="73884-151">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="73884-152">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="73884-152">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="73884-153">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="73884-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

