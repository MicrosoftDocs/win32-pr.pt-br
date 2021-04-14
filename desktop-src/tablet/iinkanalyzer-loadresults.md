---
description: Carrega os resultados da análise salva no IInkAnalyzer.
ms.assetid: 7634dbe2-1857-497c-81b5-76b92fed862d
title: 'Método IInkAnalyzer:: loadresults (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.LoadResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 76c7fed63b38f1b4fc058fbe7676a727c2d47f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461148"
---
# <a name="iinkanalyzerloadresults-method"></a><span data-ttu-id="5e498-103">Método IInkAnalyzer:: loadresults</span><span class="sxs-lookup"><span data-stu-id="5e498-103">IInkAnalyzer::LoadResults method</span></span>

<span data-ttu-id="5e498-104">Carrega os resultados da análise salva no [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="5e498-104">Loads saved analysis results into the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5e498-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e498-105">Syntax</span></span>


```C++
HRESULT LoadResults(
  [in]          ULONG        ulDataSize,
  [in]          BYTE         *pbSerializedResults,
  [in]          ULONG        ulStrokeIdsCount,
  [in]          LONG         *plOriginalStrokeIds,
  [in]          LONG         *plNewStrokeIds,
  [out, retval] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="5e498-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e498-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e498-107">*ulDataSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e498-107">*ulDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e498-108">O número de bytes em *pbSerializedResults*.</span><span class="sxs-lookup"><span data-stu-id="5e498-108">The number of bytes in *pbSerializedResults*.</span></span>

</dd> <dt>

<span data-ttu-id="5e498-109">*pbSerializedResults* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e498-109">*pbSerializedResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e498-110">Os resultados da análise serializada.</span><span class="sxs-lookup"><span data-stu-id="5e498-110">The serialized analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="5e498-111">*ulStrokeIdsCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e498-111">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e498-112">O número de identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="5e498-112">The number of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="5e498-113">*plOriginalStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e498-113">*plOriginalStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e498-114">A matriz de identificadores de traço originais.</span><span class="sxs-lookup"><span data-stu-id="5e498-114">The array of original stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="5e498-115">*plNewStrokeIds* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e498-115">*plNewStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e498-116">A matriz de novos identificadores de traço.</span><span class="sxs-lookup"><span data-stu-id="5e498-116">The array of new stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="5e498-117">*pfSuccessful* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5e498-117">*pfSuccessful* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5e498-118">**Variante \_ TRUE** se o carregamento tiver sido bem-sucedido; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="5e498-118">**VARIANT\_TRUE** if loading was successful; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e498-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e498-119">Return value</span></span>

<span data-ttu-id="5e498-120">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5e498-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e498-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e498-121">Remarks</span></span>

<span data-ttu-id="5e498-122">Quando o [**IInkAnalyzer**](iinkanalyzer.md) adiciona um [**IContextNode**](icontextnode.md) dos resultados salvos, ele atribui um novo GUID (identificador global exclusivo) para o **IContextNode** (consulte [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md) e propriedades de nó de [contexto](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="5e498-122">When the [**IInkAnalyzer**](iinkanalyzer.md) adds a [**IContextNode**](icontextnode.md) from the saved results, it assigns a new globally unique identifier (GUID) to the **IContextNode** (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md) and [Context Node Properties](context-node-properties.md)).</span></span>

<span data-ttu-id="5e498-123">Esse método adiciona os resultados da análise salva à árvore [**IContextNode**](icontextnode.md) existente.</span><span class="sxs-lookup"><span data-stu-id="5e498-123">This method adds the saved analysis results to the existing [**IContextNode**](icontextnode.md) tree.</span></span> <span data-ttu-id="5e498-124">Para garantir que os resultados combinados sejam ordenados corretamente, adicione a área que contém os nós de contexto carregados à região suja do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) e reanalise a tinta.</span><span class="sxs-lookup"><span data-stu-id="5e498-124">To ensure that the combined results are ordered correctly, add the area containing the loaded context nodes to the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) and reanalyze the ink.</span></span>

<span data-ttu-id="5e498-125">O método [**IInkAnalyzer:: SaveResults**](iinkanalyzer-saveresults.md), o método [**IInkAnalyzer:: SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)e os métodos do [**método IInkAnalyzer:: SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md) não salvam os dados do pacote junto com os resultados da análise.</span><span class="sxs-lookup"><span data-stu-id="5e498-125">The [**IInkAnalyzer::SaveResults Method**](iinkanalyzer-saveresults.md), [**IInkAnalyzer::SaveResultsForNodes Method**](iinkanalyzer-saveresultsfornodes.md), and [**IInkAnalyzer::SaveResultsForStrokes Method**](iinkanalyzer-saveresultsforstrokes.md) methods do not save the packet data along with the analysis results.</span></span>

<span data-ttu-id="5e498-126">Cada identificador em *plOriginalStrokeIds* é o identificador de traço para o traço nos resultados da análise salva.</span><span class="sxs-lookup"><span data-stu-id="5e498-126">Each identifier in *plOriginalStrokeIds* is the stroke identifier for the stroke in the saved analysis results.</span></span> <span data-ttu-id="5e498-127">Cada identificador em *plNewStrokeIds* é o novo identificador com o qual substituir o identificador original nos resultados da análise carregada.</span><span class="sxs-lookup"><span data-stu-id="5e498-127">Each identifier in *plNewStrokeIds* is the new identifier with which to replace the original identifier in the loaded analysis results.</span></span>

<span data-ttu-id="5e498-128">Se uma dica de análise salva entrar em conflito com uma dica de análise existente, o [**IInkAnalyzer**](iinkanalyzer.md) não carregará a dica salva, mas carregará o restante dos resultados salvos.</span><span class="sxs-lookup"><span data-stu-id="5e498-128">If a saved analysis hint conflicts with an existing analysis hint, the [**IInkAnalyzer**](iinkanalyzer.md) does not load the saved hint but does load the rest of the saved results.</span></span> <span data-ttu-id="5e498-129">No entanto, se o **IInkAnalyzer** carrega resultados para um traço que está dentro da área de uma dica de análise salva que o **IInkAnalyzer** não carrega, o **IInkAnalyzer** adiciona a caixa delimitadora do traço à região suja do objeto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="5e498-129">However, if the **IInkAnalyzer** loads results for a stroke that is within the area of a saved analysis hint that the **IInkAnalyzer** does not load, the **IInkAnalyzer** adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="5e498-130">Além disso, se o **IInkAnalyzer** carregar resultados para um traço que esteja dentro de uma área de dica de análise existente, o **IInkAnalyzer** também adicionará a caixa delimitadora do traço à região suja do objeto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="5e498-130">Also, if the **IInkAnalyzer** loads results for a stroke that is within an existing analysis hint's area, the **IInkAnalyzer** also adds the bounding box of the stroke to the **IInkAnalyzer** object's dirty region.</span></span> <span data-ttu-id="5e498-131">Para obter mais informações sobre dicas de análise, consulte [Propriedades de dica de análise](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="5e498-131">For more information about analysis hints, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="5e498-132">Esse método pode gerar os eventos [**\_ IAnalysisProxyEvents:: ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)e [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) à medida que ele carrega os resultados salvos.</span><span class="sxs-lookup"><span data-stu-id="5e498-132">This method may raise the [**\_IAnalysisProxyEvents::ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**\_IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), and [**\_IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) events as it loads the saved results.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e498-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e498-133">Requirements</span></span>



| <span data-ttu-id="5e498-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e498-134">Requirement</span></span> | <span data-ttu-id="5e498-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5e498-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e498-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e498-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5e498-137">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5e498-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5e498-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e498-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5e498-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5e498-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5e498-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e498-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e498-141"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5e498-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5e498-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5e498-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e498-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e498-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5e498-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e498-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e498-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5e498-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5e498-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="5e498-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="5e498-147">**Método IInkAnalyzer:: GetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="5e498-147">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="5e498-148">**Método IInkAnalyzer:: SetDirtyRegion**</span><span class="sxs-lookup"><span data-stu-id="5e498-148">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="5e498-149">**Método IInkAnalyzer:: SaveResults**</span><span class="sxs-lookup"><span data-stu-id="5e498-149">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="5e498-150">**Método IInkAnalyzer:: SaveResultsForNodes**</span><span class="sxs-lookup"><span data-stu-id="5e498-150">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="5e498-151">**Método IInkAnalyzer:: SaveResultsForStrokes**</span><span class="sxs-lookup"><span data-stu-id="5e498-151">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="5e498-152">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="5e498-152">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




