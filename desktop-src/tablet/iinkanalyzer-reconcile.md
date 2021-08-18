---
description: Aplica os resultados de uma operação de análise de tinta em segundo plano à árvore de nó de contexto para as partes da árvore que não foram modificadas pelo aplicativo desde a chamada para o Método IInkAnalyzer::BackgroundAnalyze.
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: Método IInkAnalyzer::Reconcile (IACom.h)
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
ms.openlocfilehash: 3b16497a7f7822bf1557e3e686a81497a4e3723e71f115a1a7d6aa59d8381db2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092026"
---
# <a name="iinkanalyzerreconcile-method"></a>Método IInkAnalyzer::Reconcile

Aplica os resultados de uma operação de análise de tinta em segundo plano à árvore de nó de contexto para as partes da árvore que não foram modificadas pelo aplicativo desde a chamada para o Método [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Por padrão, [**o IInkAnalyzer**](iinkanalyzer.md) executa uma fase de reconciliação automática imediatamente antes de auerar os eventos [**\_ IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) e [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Para desabilitar a reconciliação automática, limpe o sinalizador **\_ AutomaticReconciliation do AnalysisModes** dos modos de análise do analisador de tinta (consulte [**Método IInkAnalyzer::SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) e [**AnalysisModes).**](analysismodes.md) O [**método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) retorna um erro quando a reconciliação automática é desabilitada e seu aplicativo não trata o evento [**\_ IAnalysisEvents::ReadyToReconcile.**](-ianalysisevents-readytoreconcile.md) Seu aplicativo deve chamar o método **IInkAnalyzer::Reconcile** antes que [**o IInkAnalyzer**](iinkanalyzer.md) possa continuar a processar os resultados ou continuar a análise para o estágio de análise correspondente.

Seu aplicativo pode fazer alterações, como adicionar ou remover traços e alterar dados de traço, na árvore de nós de contexto do objeto [**IInkAnalyzer**](iinkanalyzer.md) durante a análise em segundo plano. Essas alterações podem invalidar partes dos resultados da análise em segundo plano. Esse método aplica os resultados da análise somente à árvore de nós de contexto do analisador para as partes da árvore que seu aplicativo não alterou. Esse método também adiciona regiões que contêm resultados de análise invalidados à região suja do objeto **IInkAnalyzer** (consulte [**Método IInkAnalyzer::GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Para obter mais informações sobre como usar o para analisar tinta, consulte Visão [geral da análise de tinta.](ink-analysis-overview.md) [**AnalysisModes**](analysismodes.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




