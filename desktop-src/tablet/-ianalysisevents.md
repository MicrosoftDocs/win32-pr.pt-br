---
description: Especifica os eventos associados às etapas de análise de um objeto IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interface _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2f49455e3e6fb68b2884cda380c304d7655b70d49ff338bcfb7c36904b449019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452161"
---
# <a name="_ianalysisevents-interface"></a>\_Interface IAnalysisEvents

Especifica os eventos associados às etapas de análise de um objeto [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Eventos](/windows)

### <a name="events"></a>Eventos

A interface **\_ IAnalysisEvents** tem esses eventos.



| Evento                                                               | Descrição                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atividade**](-ianalysisevents-activity.md)                       | Ocorre durante chamadas para o método de método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Ocorre quando o estágio de análise intermediária atual é concluído.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) está pronto para reconciliar seus resultados de análise em segundo plano com seu estado atual.<br/>                                                  |
| [**Resultados**](-ianalysisevents-results.md)                         | Ocorre quando o estágio de análise final é concluído.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Ocorre antes que o [**IInkAnalyzer**](iinkanalyzer.md) acesse os dados de traço.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

