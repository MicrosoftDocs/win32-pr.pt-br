---
description: Ocorre quando o estágio de análise intermediária atual é concluído.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: _IAnalysisEvents::IntermediateResults event (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9efead00094fdcd773c3ac90b0d626e2036030171bcf3be011323b6da70fb665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857192"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_Evento IAnalysisEvents::IntermediateResults

Ocorre quando o estágio de análise intermediária atual é concluído.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ Em\]
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) que está executando a análise.

</dd> <dt>

*pAnalysisStatus* \[ Em\]
</dt> <dd>

O [**objeto IAnalysisStatus**](ianalysisstatus.md) que representa o status dos resultados intermediários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de reconciliar os resultados intermediários para o estágio de análise atual.

Se seu aplicativo mantém sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md), esse evento indica que **o IInkAnalyzer** concluiu fazer alterações em seus dados internos para esse estágio de análise.

Bloqueie sua estrutura de dados quando [**o IInkAnalyzer**](iinkanalyzer.md) gera o [**\_ evento IAnalysisProxyEvents::InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Alterações na estrutura de dados durante essa fase de análise podem causar erros na análise e na sincronização de tinta. Você pode desbloquear sua estrutura de dados quando **o IInkAnalyzer** gera o evento **\_ IAnalysisEvents::IntermediateResults** ou [**\_ IAnalysisEvents::Results.**](-ianalysisevents-results.md)

Para obter mais informações sobre como sincronizar os dados do aplicativo [**com o IInkAnalyzer,**](iinkanalyzer.md)consulte Proxy de dados [com análise de tinta.](data-proxy-with-ink-analysis.md)

O [**IInkAnalyzer**](iinkanalyzer.md) gera resultados intermediários somente quando seus modos de análise têm o sinalizador **\_ IntermediateResults analysisModes** definido (consulte [**Método IInkAnalyzer::GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::Results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>
