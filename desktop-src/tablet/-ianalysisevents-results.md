---
description: Ocorre quando o estágio de análise final é concluído.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: _IAnalysisEvents::Results event (IACom.h)
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
ms.openlocfilehash: 22d9ac16976b1cd61d5d2e403424fc9ed08b8da0cbfcced213decc512a1f1e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047388"
---
# <a name="_ianalysiseventsresults-event"></a>\_Evento IAnalysisEvents::Results

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

*pInkAnalyzer* \[ Em\]
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) que produz os resultados da análise.

</dd> <dt>

*pAnalysisStatus* \[ Em\]
</dt> <dd>

O [**objeto IAnalysisStatus**](ianalysisstatus.md) que representa o status da análise.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de reconciliar os resultados para o estágio de análise final.

Se seu aplicativo chamar [**o método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md), esse evento sinaliza quando os resultados da análise estão prontos.

Se seu aplicativo mantém sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md), esse evento indica que **o IInkAnalyzer** concluiu fazer alterações em seus dados internos para esse estágio de análise.

Bloqueie sua estrutura de dados quando [**o IInkAnalyzer**](iinkanalyzer.md) gera o [**\_ evento IAnalysisProxyEvents::InkAnalyzerStateChanging.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Alterações na estrutura de dados durante essa fase de análise podem causar erros na análise e na sincronização de tinta. Desbloqueie sua estrutura de dados quando **o IInkAnalyzer** agarr [**\_ o evento IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) ou **\_ IAnalysisEvents::Results.**

Para obter mais informações sobre como sincronizar os dados do aplicativo [**com o IInkAnalyzer,**](iinkanalyzer.md)consulte Proxy de dados [com análise de tinta.](data-proxy-with-ink-analysis.md)

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

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




