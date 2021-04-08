---
description: 'Define identificadores globais exclusivos (GUIDs) para propriedades de um nó de dica de análise (consulte IContextNode:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Propriedades da dica de análise (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920619"
---
# <a name="analysis-hint-properties"></a><span data-ttu-id="0356c-103">Propriedades da dica de análise</span><span class="sxs-lookup"><span data-stu-id="0356c-103">Analysis Hint Properties</span></span>

<span data-ttu-id="0356c-104">Define identificadores globais exclusivos (GUIDs) para propriedades de um nó de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="0356c-104">Defines globally unique identifiers (GUIDs) for properties of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="0356c-105">A tabela a seguir descreve as informações referenciadas por cada constante.</span><span class="sxs-lookup"><span data-stu-id="0356c-105">The following table describes information referenced by each constant.</span></span>



| <span data-ttu-id="0356c-106">Constante</span><span class="sxs-lookup"><span data-stu-id="0356c-106">Constant</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="0356c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0356c-107">Description</span></span>                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <span data-ttu-id="0356c-108"><dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-108"><dt>**GUID\_AHP\_ALLOWPARTIALDICTIONARYTERMS**</dt></span></span> </dl>       | <span data-ttu-id="0356c-109">Se termos de dicionário parciais são permitidos em uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-109">Whether partial dictionary terms are allowed on an analysis hint.</span></span><br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <span data-ttu-id="0356c-110"><dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-110"><dt>**GUID\_AHP\_ANALYSISHINTNAME**</dt></span></span> </dl>                                        | <span data-ttu-id="0356c-111">O nome de uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-111">The name of an analysis hint.</span></span><br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <span data-ttu-id="0356c-112"><dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-112"><dt>**GUID\_AHP\_COERCETOFACTOID**</dt></span></span> </dl>                                           | <span data-ttu-id="0356c-113">Se o analisador de tinta limita sua análise de tinta na área da dica para estar de acordo com o factor.</span><span class="sxs-lookup"><span data-stu-id="0356c-113">Whether the ink analyzer limits its analysis of ink within the hint's area to conform to the factoid.</span></span><br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <span data-ttu-id="0356c-114"><dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-114"><dt>**GUID\_AHP\_ENABLEDUNICODECHARACTERRANGES**</dt></span></span> </dl> | <span data-ttu-id="0356c-115">A dica contém uma matriz de caracteres que representa o conjunto restrito de conjunto de caracteres Unicode com suporte permitido por este InkRecognizer.</span><span class="sxs-lookup"><span data-stu-id="0356c-115">The hint contains an array of characters that represent the restricted set of supported unicode character set supported by this InkRecognizer.</span></span><br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <span data-ttu-id="0356c-116"><dt>**\_factor de AHP GUID \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-116"><dt>**GUID\_AHP\_FACTOID**</dt></span></span> </dl>                                                                   | <span data-ttu-id="0356c-117">O factor em uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-117">The factoid on an analysis hint.</span></span><br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <span data-ttu-id="0356c-118"><dt>**\_Guia de AHP GUID \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-118"><dt>**GUID\_AHP\_GUIDE**</dt></span></span> </dl>                                                                         | <span data-ttu-id="0356c-119">A estrutura [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) que representa o guia para uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-119">The [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) structure that represents the guide for an analysis hint.</span></span><br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <span data-ttu-id="0356c-120"><dt>**GUID \_ AHP \_ PREFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-120"><dt>**GUID\_AHP\_PREFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="0356c-121">O texto do prefixo em uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-121">The prefix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <span data-ttu-id="0356c-122"><dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-122"><dt>**GUID\_AHP\_SUFFIXTEXT**</dt></span></span> </dl>                                                          | <span data-ttu-id="0356c-123">O texto do sufixo em uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-123">The suffix text on an analysis hint.</span></span><br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <span data-ttu-id="0356c-124"><dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-124"><dt>**GUID\_AHP\_TOPINKBREAKSONLY**</dt></span></span> </dl>                                        | <span data-ttu-id="0356c-125">Se as várias segmentações nos resultados do reconhecimento de tinta estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="0356c-125">Whether the multiple segmentations in the ink recognition results are disabled.</span></span><br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <span data-ttu-id="0356c-126"><dt>**\_AHP de \_ palavras de GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-126"><dt>**GUID\_AHP\_WORDLIST**</dt></span></span> </dl>                                                                | <span data-ttu-id="0356c-127">A matriz de cadeias de caracteres que representa a lista de palavras para uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-127">The array of strings that represents the word list for an analysis hint.</span></span><br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <span data-ttu-id="0356c-128"><dt>**GUID \_ AHP \_ WordMode**</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-128"><dt>**GUID\_AHP\_WORDMODE**</dt></span></span> </dl>                                                                | <span data-ttu-id="0356c-129">Se o analisador de tinta prioriza resultados de palavras únicas em resultados de várias palavras para uma dica de análise.</span><span class="sxs-lookup"><span data-stu-id="0356c-129">Whether the ink analyzer prioritizes single-word results over multiple-word results for an analysis hint.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="0356c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="0356c-130">Remarks</span></span>

<span data-ttu-id="0356c-131">Essas GUIDs são usadas para identificar propriedades que o [**IInkAnalyzer**](iinkanalyzer.md) pode definir em um nó de contexto de dica de análise (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="0356c-131">These GUIDs are used to identify properties that the [**IInkAnalyzer**](iinkanalyzer.md) can set on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

<span data-ttu-id="0356c-132">Para obter ou definir propriedades de um [**IContextNode**](icontextnode.md) em geral, consulte [Propriedades do nó de contexto](context-node-properties.md).</span><span class="sxs-lookup"><span data-stu-id="0356c-132">To get or set properties of an [**IContextNode**](icontextnode.md) in general, see [Context Node Properties](context-node-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0356c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0356c-133">Requirements</span></span>



| <span data-ttu-id="0356c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0356c-134">Requirement</span></span> | <span data-ttu-id="0356c-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0356c-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0356c-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0356c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0356c-137">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0356c-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0356c-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0356c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0356c-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0356c-139">None supported</span></span><br/>                                                           |
| <span data-ttu-id="0356c-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0356c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0356c-141"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="0356c-141"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0356c-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="0356c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0356c-143">Propriedades do nó de contexto</span><span class="sxs-lookup"><span data-stu-id="0356c-143">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="0356c-144">Tipos de nó de contexto</span><span class="sxs-lookup"><span data-stu-id="0356c-144">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="0356c-145">**Método IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="0356c-145">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="0356c-146">**Método IInkAnalyzer:: GetAnalysisHintsByName**</span><span class="sxs-lookup"><span data-stu-id="0356c-146">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="0356c-147">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0356c-147">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="0356c-148">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0356c-148">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="0356c-149">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="0356c-149">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="0356c-150">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="0356c-150">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="0356c-151">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="0356c-151">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="0356c-152">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="0356c-152">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="0356c-153">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="0356c-153">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




