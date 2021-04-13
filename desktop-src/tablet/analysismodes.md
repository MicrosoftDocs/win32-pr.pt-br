---
description: Especifica como o IInkAnalyzer executa a análise de tinta.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Enumeração AnalysisModes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370510"
---
# <a name="analysismodes-enumeration"></a><span data-ttu-id="0d9fc-103">Enumeração AnalysisModes</span><span class="sxs-lookup"><span data-stu-id="0d9fc-103">AnalysisModes enumeration</span></span>

<span data-ttu-id="0d9fc-104">Especifica como o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-104">Specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d9fc-105">Syntax</span></span>


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a><span data-ttu-id="0d9fc-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0d9fc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0d9fc-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes\_None**</span></span>
</dt> <dd>

<span data-ttu-id="0d9fc-108">Nenhum modo foi especificado.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-108">No modes are specified.</span></span>

</dd> <dt>

<span data-ttu-id="0d9fc-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes\_AutomaticReconciliation**</span></span>
</dt> <dd>

<span data-ttu-id="0d9fc-110">Se o [**IInkAnalyzer**](iinkanalyzer.md) inicia automaticamente a operação de reconciliação assim que os resultados intermediários ou finais estão prontos.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-110">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically starts the reconciliation operation as soon as the intermediate or final results are ready.</span></span>

<span data-ttu-id="0d9fc-111">Se esse modo estiver habilitado, o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) não será gerado.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-111">If this mode is enabled, the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event is not raised.</span></span> <span data-ttu-id="0d9fc-112">Se esse modo for desabilitado, o evento **\_ IAnalysisEvents:: ReadyToReconcile** será gerado.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-112">If this mode is disabled, the **\_IAnalysisEvents::ReadyToReconcile** event is raised.</span></span>

</dd> <dt>

<span data-ttu-id="0d9fc-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes\_StrokeCacheAutoCleanup**</span></span>
</dt> <dd>

<span data-ttu-id="0d9fc-114">Se o [**IInkAnalyzer**](iinkanalyzer.md) limpa automaticamente os traços desnecessários do cache de traço antes de executar a análise.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-114">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically clears unneeded strokes from the stroke cache before performing analysis.</span></span>

<span data-ttu-id="0d9fc-115">Se esse modo estiver habilitado, o [**IInkAnalyzer**](iinkanalyzer.md) limpará os dados de traço antes de executar a análise.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-115">If this mode is enabled, the [**IInkAnalyzer**](iinkanalyzer.md) clears the stroke data before performing analysis.</span></span> <span data-ttu-id="0d9fc-116">Seu código também deve manipular o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="0d9fc-116">Your code must also then handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span> <span data-ttu-id="0d9fc-117">Se o evento **\_ IAnalysisEvents:: UpdateStrokesCache** não for tratado, uma exceção será gerada.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-117">If the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span> <span data-ttu-id="0d9fc-118">Essa verificação é feita nas fases analisar (ou BackgroundAnalyze) e reconciliação.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-118">This check is done both at the Analyze (or BackgroundAnalyze) and Reconciliation phases.</span></span>

<span data-ttu-id="0d9fc-119">Se esse modo estiver desabilitado, o [**IInkAnalyzer**](iinkanalyzer.md) não limpará os dados do traço.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-119">If this mode is disabled, the [**IInkAnalyzer**](iinkanalyzer.md) does not clear the stroke data.</span></span> <span data-ttu-id="0d9fc-120">Para limpar os dados de traço, chame o [**método IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md).</span><span class="sxs-lookup"><span data-stu-id="0d9fc-120">To clear the stroke data, call [**IInkAnalyzer::ClearStrokeData Method**](iinkanalyzer-clearstrokedata.md).</span></span> <span data-ttu-id="0d9fc-121">Se esse modo estiver desabilitado, o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) será gerado para que o **IInkAnalyzer** possa recuperar os dados de traço mais recentes para os traços que tiveram o cache apagado.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-121">If this mode is disabled, the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event is raised so the **IInkAnalyzer** can retrieve the latest stroke data for any strokes that have had their cache cleared.</span></span> <span data-ttu-id="0d9fc-122">Se o cache de traço for limpo, mas o evento **\_ IAnalysisEvents:: UpdateStrokesCache** não for tratado, uma exceção será gerada.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-122">If the stroke cache is cleared, but the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span>

</dd> <dt>

<span data-ttu-id="0d9fc-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes\_PersonalizationEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="0d9fc-124">A personalização do reconhecimento de manuscrito está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-124">Personalization of handwriting recognition is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="0d9fc-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="0d9fc-126">Todos os modos estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-126">All modes are enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d9fc-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d9fc-127">Remarks</span></span>

<span data-ttu-id="0d9fc-128">Essa enumeração permite uma combinação de bit a bit de seus valores de membro.</span><span class="sxs-lookup"><span data-stu-id="0d9fc-128">This enumeration allows a bitwise combination of its member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d9fc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d9fc-129">Requirements</span></span>



| <span data-ttu-id="0d9fc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d9fc-130">Requirement</span></span> | <span data-ttu-id="0d9fc-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0d9fc-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9fc-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d9fc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9fc-133">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0d9fc-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0d9fc-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d9fc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9fc-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0d9fc-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0d9fc-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d9fc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d9fc-137"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0d9fc-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d9fc-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d9fc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d9fc-139">**Método IInkAnalyzer:: GetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-139">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="0d9fc-140">**Método IInkAnalyzer:: SetAnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-140">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="0d9fc-141">**\_IAnalysisEvents::IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-141">**\_IAnalysisEvents::IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[<span data-ttu-id="0d9fc-142">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-142">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="0d9fc-143">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="0d9fc-143">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="0d9fc-144">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="0d9fc-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




