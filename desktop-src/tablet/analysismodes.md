---
description: Especifica como o IInkAnalyzer executa a análise de tinta.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Enumeração AnalysisModes (IACom.h)
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
ms.openlocfilehash: e7e363353e6b9569d99adedd690c4ca40010fd62d3681ee5053447243961f2e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675584"
---
# <a name="analysismodes-enumeration"></a>Enumeração AnalysisModes

Especifica como o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise de tinta.

## <a name="syntax"></a>Syntax


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ None**
</dt> <dd>

Nenhum modo é especificado.

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**\_AutomaticReconciliation do AnalysisModes**
</dt> <dd>

Se o [**IInkAnalyzer inicia**](iinkanalyzer.md) automaticamente a operação de reconciliação assim que os resultados intermediários ou finais estão prontos.

Se esse modo estiver habilitado, o [**\_ evento IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) não será gerado. Se esse modo estiver desabilitado, **\_ o evento IAnalysisEvents::ReadyToReconcile** será gerado.

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**StrokeCacheAutoCleanup do AnalysisModes \_**
</dt> <dd>

Se o [**IInkAnalyzer**](iinkanalyzer.md) limpa automaticamente os traços não precisos do cache de traço antes de executar a análise.

Se esse modo estiver habilitado, o [**IInkAnalyzer**](iinkanalyzer.md) limpará os dados de traço antes de executar a análise. Seu código também deve manipular o [**\_ evento IAnalysisEvents::UpdateStrkesCache.**](-ianalysisevents-updatestrokescache.md) Se o **\_ evento IAnalysisEvents::UpdateStrkesCache** não for tratado, uma exceção será aventada. Essa verificação é feita nas fases Analisar (ou BackgroundAnalyze) e Reconciliação.

Se esse modo estiver desabilitado, [**o IInkAnalyzer**](iinkanalyzer.md) não limpará os dados de traço. Para limpar os dados de traço, chame [**o método IInkAnalyzer::ClearStrkeData**](iinkanalyzer-clearstrokedata.md). Se esse modo estiver desabilitado, o evento [**\_ IAnalysisEvents::UpdateStrkesCache**](-ianalysisevents-updatestrokescache.md) será gerado para que **o IInkAnalyzer** possa recuperar os dados de traço mais recentes para todos os traços que tiveram seu cache limpo. Se o cache de traço estiver limpo, mas o evento **\_ IAnalysisEvents::UpdateOsekesCache** não for tratado, uma exceção será apurada.

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**
</dt> <dd>

A personalização do reconhecimento de manuscrito está habilitada.

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**Padrão \_ analysisModes**
</dt> <dd>

Todos os modos estão habilitados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração permite uma combinação bit a bit de seus valores de membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IInkAnalyzer::GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Método IInkAnalyzer::SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateRogkesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




