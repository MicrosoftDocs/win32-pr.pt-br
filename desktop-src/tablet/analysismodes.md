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

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ nenhum**
</dt> <dd>

Nenhum modo foi especificado.

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**
</dt> <dd>

Se o [**IInkAnalyzer**](iinkanalyzer.md) inicia automaticamente a operação de reconciliação assim que os resultados intermediários ou finais estão prontos.

Se esse modo estiver habilitado, o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) não será gerado. Se esse modo for desabilitado, o evento **\_ IAnalysisEvents:: ReadyToReconcile** será gerado.

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**
</dt> <dd>

Se o [**IInkAnalyzer**](iinkanalyzer.md) limpa automaticamente os traços desnecessários do cache de traço antes de executar a análise.

Se esse modo estiver habilitado, o [**IInkAnalyzer**](iinkanalyzer.md) limpará os dados de traço antes de executar a análise. Seu código também deve manipular o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) . Se o evento **\_ IAnalysisEvents:: UpdateStrokesCache** não for tratado, uma exceção será gerada. Essa verificação é feita nas fases analisar (ou BackgroundAnalyze) e reconciliação.

Se esse modo estiver desabilitado, o [**IInkAnalyzer**](iinkanalyzer.md) não limpará os dados do traço. Para limpar os dados de traço, chame o [**método IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md). Se esse modo estiver desabilitado, o evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) será gerado para que o **IInkAnalyzer** possa recuperar os dados de traço mais recentes para os traços que tiveram o cache apagado. Se o cache de traço for limpo, mas o evento **\_ IAnalysisEvents:: UpdateStrokesCache** não for tratado, uma exceção será gerada.

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**
</dt> <dd>

A personalização do reconhecimento de manuscrito está habilitada.

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes \_ padrão**
</dt> <dd>

Todos os modos estão habilitados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa enumeração permite uma combinação de bit a bit de seus valores de membro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




