---
description: Ocorre quando o IInkAnalyzer está pronto para reconciliar seus resultados de análise em segundo plano com seu estado atual.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: 'Evento _IAnalysisEvents:: ReadyToReconcile (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b65606675d8ae5aed694df87f35667a71fad2576344231a4e329783be4b31426
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111266"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_Evento IAnalysisEvents:: ReadyToReconcile

Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) está pronto para reconciliar seus resultados de análise em segundo plano com seu estado atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Parâmetros

Este evento não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

O [**IInkAnalyzer**](iinkanalyzer.md) executa a reconciliação automática quando o sinalizador **\_ AutomaticReconciliation de AnalysisModes** do Ink Analyzer é definido (consulte o [**método IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)). Quando o sinalizador **AnalysisModes \_ AutomaticReconciliation** não é definido, seu aplicativo precisa reconciliar os resultados da análise em segundo plano manualmente.

Para executar a reconciliação manual, siga estas etapas.

1.  Limpe o sinalizador **AnalysisModes \_ AutomaticReconciliation** do Ink Analyzer.
2.  Manipule o evento **\_ IAnalysisEvents:: ReadyToReconcile** .
3.  Para reconciliar os resultados da análise, chame o método de [**método IInkAnalyzer:: reconcile**](iinkanalyzer-reconcile.md) do manipulador de eventos para o evento **\_ IAnalysisEvents:: ReadyToReconcile** . Para cancelar a operação atual de análise em segundo plano, chame o método do [**método IInkAnalyzer:: Abort**](iinkanalyzer-abort.md) do manipulador de eventos para o evento **\_ IAnalysisEvents:: ReadyToReconcile** .

O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento antes de gerar o evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) .

Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento durante a análise em segundo plano.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: Reconcilize**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




