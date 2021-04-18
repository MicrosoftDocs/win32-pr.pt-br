---
description: 'Aplica os resultados de uma operação de análise de tinta em segundo plano à árvore de nós de contexto para as partes da árvore que não foram modificadas pelo aplicativo desde a chamada para o método IInkAnalyzer:: BackgroundAnalyze.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'Método IInkAnalyzer:: Reconcilize (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752181"
---
# <a name="iinkanalyzerreconcile-method"></a>Método IInkAnalyzer:: Reconcilize

Aplica os resultados de uma operação de análise de tinta em segundo plano à árvore de nós de contexto para as partes da árvore que não foram modificadas pelo aplicativo desde a chamada para o [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Por padrão, o [**IInkAnalyzer**](iinkanalyzer.md) executa uma fase de reconciliação automática imediatamente antes de gerar os eventos [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) e [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

Para desabilitar a reconciliação automática, desmarque o sinalizador **AnalysisModes \_ AutomaticReconciliation** dos modos de análise do Ink Analyzer (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) e [**AnalysisModes**](analysismodes.md)). O método do [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) retorna um erro quando a reconciliação automática está desabilitada e seu aplicativo não manipula o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . Seu aplicativo deve chamar o método de **método IInkAnalyzer:: reconcile** antes que o [**IInkAnalyzer**](iinkanalyzer.md) possa continuar processando os resultados ou continuar a análise para o estágio de análise correspondente.

Seu aplicativo pode fazer alterações, como adicionar ou remover traços e alterar dados de traço, na árvore de nós de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) durante a análise em segundo plano. Essas alterações podem invalidar partes dos resultados da análise em segundo plano. Esse método aplica resultados de análise somente à árvore de nós de contexto do analisador para as partes da árvore em que seu aplicativo não foi alterado. Esse método também adiciona regiões que contêm resultados de análise invalidados à região suja do objeto **IInkAnalyzer** (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Para obter mais informações sobre como usar o para analisar a tinta, consulte [visão geral da análise de tinta](ink-analysis-overview.md). [**AnalysisModes**](analysismodes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




