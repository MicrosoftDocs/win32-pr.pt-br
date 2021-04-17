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
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763438"
---
# <a name="_ianalysisevents-interface"></a>\_Interface IAnalysisEvents

Especifica os eventos associados às etapas de análise de um objeto [**IInkAnalyzer**](iinkanalyzer.md) .

-   [Eventos](/windows)

### <a name="events"></a>Eventos

A interface **\_ IAnalysisEvents** tem esses eventos.



| Evento                                                               | Descrição                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Actividade**](-ianalysisevents-activity.md)                       | Ocorre durante chamadas para o método de método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Ocorre quando o estágio de análise intermediária atual é concluído.<br/>                                                                                                                    |
| [**ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)       | Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) está pronto para reconciliar seus resultados de análise em segundo plano com seu estado atual.<br/>                                                  |
| [**Resultados**](-ianalysisevents-results.md)                         | Ocorre quando o estágio de análise final é concluído.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Ocorre antes que o [**IInkAnalyzer**](iinkanalyzer.md) acesse os dados de traço.<br/>                                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/> |
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

 

