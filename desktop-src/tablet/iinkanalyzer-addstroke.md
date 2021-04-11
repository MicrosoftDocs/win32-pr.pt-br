---
description: Adiciona dados de traço para um único traço para o IInkAnalyzer e atribui o identificador de cultura do thread de entrada ativo ao traço.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: 'Método IInkAnalyzer:: addstroke (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc946e7975772eb7be6fff54d01bb1a6dae8ebe7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164545"
---
# <a name="iinkanalyzeraddstroke-method"></a><span data-ttu-id="1909f-103">Método IInkAnalyzer:: addstroke</span><span class="sxs-lookup"><span data-stu-id="1909f-103">IInkAnalyzer::AddStroke method</span></span>

<span data-ttu-id="1909f-104">Adiciona dados de traço para um único traço para o [**IInkAnalyzer**](iinkanalyzer.md) e atribui o identificador de cultura do thread de entrada ativo ao traço.</span><span class="sxs-lookup"><span data-stu-id="1909f-104">Adds stroke data for a single stroke to the [**IInkAnalyzer**](iinkanalyzer.md) and assigns the active input thread's culture identifier to the stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="1909f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1909f-105">Syntax</span></span>


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a><span data-ttu-id="1909f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1909f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1909f-107">*lStrokeId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1909f-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1909f-108">O identificador do traço a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="1909f-108">The identifier for the stroke to add.</span></span>

</dd> <dt>

<span data-ttu-id="1909f-109">*ulStrokePacketDataCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1909f-109">*ulStrokePacketDataCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1909f-110">O número de pacotes no traço.</span><span class="sxs-lookup"><span data-stu-id="1909f-110">The number of packets in the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="1909f-111">*plStrokePacketData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1909f-111">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1909f-112">Uma matriz que contém os dados de pacote para o traço.</span><span class="sxs-lookup"><span data-stu-id="1909f-112">An array containing the packet data for the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="1909f-113">*ulStrokePacketDescriptionCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1909f-113">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1909f-114">O número de propriedades do pacote em cada pacote.</span><span class="sxs-lookup"><span data-stu-id="1909f-114">The number of packet properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="1909f-115">*pStrokePacketDescriptionGuids* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1909f-115">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1909f-116">Uma matriz que contém os identificadores de Propriedade do pacote.</span><span class="sxs-lookup"><span data-stu-id="1909f-116">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="1909f-117">*ppContextNodeStrokeAddedTo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1909f-117">*ppContextNodeStrokeAddedTo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1909f-118">Um ponteiro para o [**IContextNode**](icontextnode.md) para o qual o [**IInkAnalyzer**](iinkanalyzer.md) adicionou o traço.</span><span class="sxs-lookup"><span data-stu-id="1909f-118">A pointer to the [**IContextNode**](icontextnode.md) to which the [**IInkAnalyzer**](iinkanalyzer.md) added the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1909f-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1909f-119">Return value</span></span>

<span data-ttu-id="1909f-120">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1909f-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1909f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="1909f-121">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1909f-122">Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodeStrokeAddedTo* quando você não precisar mais usar o objeto.</span><span class="sxs-lookup"><span data-stu-id="1909f-122">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeStrokeAddedTo* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="1909f-123">Quando *ppContextNodeStrokeAddedTo* é **nulo**, ele indica que o chamador não está interessado no valor de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="1909f-123">When *ppContextNodeStrokeAddedTo* is **NULL**, it indicates that the caller is not interested in the return value from the method.</span></span>

<span data-ttu-id="1909f-124">O [**IInkAnalyzer**](iinkanalyzer.md) adiciona o traço a um [**IContextNode**](icontextnode.md) do tipo UnclassifiedInk (consulte [tipos de nó de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="1909f-124">The [**IInkAnalyzer**](iinkanalyzer.md) adds the stroke to an [**IContextNode**](icontextnode.md) of type UnclassifiedInk (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="1909f-125">Esse nó está na coleção de subnós do nó raiz (consulte os métodos [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) ).</span><span class="sxs-lookup"><span data-stu-id="1909f-125">This node is in the root node's subnode collection (see [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) methods).</span></span>

<span data-ttu-id="1909f-126">O [**IInkAnalyzer**](iinkanalyzer.md) atribui o identificador de cultura do thread de entrada ativo ao traço e adiciona o traço ao primeiro nó de contexto UnclassifiedInk no nó raiz do analisador de tinta que contém traços com o mesmo identificador de cultura.</span><span class="sxs-lookup"><span data-stu-id="1909f-126">The [**IInkAnalyzer**](iinkanalyzer.md) assigns the culture identifier of the active input thread to the stroke and adds the stroke to the first UnclassifiedInk context node under the ink analyzer's root node that contains strokes with the same culture identifier.</span></span> <span data-ttu-id="1909f-127">Se o analisador de tinta não tiver um nó com o mesmo identificador de cultura, ele criará um novo nó de contexto UnclassifiedInk sob seu nó raiz e adicionará o traço ao novo nó de contexto UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="1909f-127">If the ink analyzer does not have a node with the same culture identifier, it creates a new UnclassifiedInk context node under its root node and adds the stroke to the new UnclassifiedInk context node.</span></span>

<span data-ttu-id="1909f-128">*plStrokePacketData* contém dados de pacote para todos os pontos no traço.</span><span class="sxs-lookup"><span data-stu-id="1909f-128">*plStrokePacketData* contains packet data for all of the points in the stroke.</span></span> <span data-ttu-id="1909f-129">*pStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto no traço.</span><span class="sxs-lookup"><span data-stu-id="1909f-129">*pStrokePacketDescriptionGuids* contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in the stroke.</span></span> <span data-ttu-id="1909f-130">Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1909f-130">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="1909f-131">Esse método expande a região suja para a União do valor atual da região e a caixa delimitadora do traço adicionado.</span><span class="sxs-lookup"><span data-stu-id="1909f-131">This method expands the dirty region to the union of the region's current value and the bounding box of the added stroke.</span></span>

<span data-ttu-id="1909f-132">Se o [**IInkAnalyzer**](iinkanalyzer.md) já contiver um traço com o mesmo identificador de traço, o **IInkAnalyzer** retornará um **HRESULT** de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="1909f-132">If the [**IInkAnalyzer**](iinkanalyzer.md) already contains a stroke with the same stroke identifier, the **IInkAnalyzer** returns an **HRESULT** of **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1909f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1909f-133">Requirements</span></span>



| <span data-ttu-id="1909f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1909f-134">Requirement</span></span> | <span data-ttu-id="1909f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1909f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1909f-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1909f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1909f-137">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1909f-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1909f-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1909f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1909f-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1909f-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1909f-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1909f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1909f-141"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1909f-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1909f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1909f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1909f-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1909f-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1909f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1909f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1909f-145">**InkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1909f-145">**InkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="1909f-146">**Método IInkAnalyzer:: AddStrokeForLanguage**</span><span class="sxs-lookup"><span data-stu-id="1909f-146">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="1909f-147">**Método IInkAnalyzer:: AddStrokes**</span><span class="sxs-lookup"><span data-stu-id="1909f-147">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="1909f-148">**Método IInkAnalyzer:: AddStrokesForLanguage**</span><span class="sxs-lookup"><span data-stu-id="1909f-148">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="1909f-149">**Método IInkAnalyzer:: RemoveStroke**</span><span class="sxs-lookup"><span data-stu-id="1909f-149">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="1909f-150">**Método IInkAnalyzer:: RemoveStrokes**</span><span class="sxs-lookup"><span data-stu-id="1909f-150">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="1909f-151">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="1909f-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

