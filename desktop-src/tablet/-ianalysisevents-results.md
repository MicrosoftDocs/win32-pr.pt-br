---
description: Ocorre quando o estágio de análise final é concluído.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: 'Evento _IAnalysisEvents:: Results (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763167"
---
# <a name="_ianalysiseventsresults-event"></a>\_Evento IAnalysisEvents:: Results

Ocorre quando o estágio de análise final é concluído.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ no\]
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) que produz os resultados da análise.

</dd> <dt>

*pAnalysisStatus* \[ no\]
</dt> <dd>

O objeto [**IAnalysisStatus**](ianalysisstatus.md) que representa o status da análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de ter reconciliado os resultados para o estágio de análise final.

Se seu aplicativo chamar o [**método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), esse evento sinalizará quando os resultados da análise estiverem prontos.

Se seu aplicativo mantém sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md), esse evento indica que o **IInkAnalyzer** terminou de fazer alterações em seus dados internos para este estágio de análise.

Bloqueie sua estrutura de dados quando o [**IInkAnalyzer**](iinkanalyzer.md) gerar o evento [**\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . As alterações na estrutura de dados durante esta fase de análise podem causar erros na análise de tinta e na sincronização. Desbloqueie sua estrutura de dados quando o **IInkAnalyzer** gerar o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou **\_ IAnalysisEvents:: Results** .

Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




