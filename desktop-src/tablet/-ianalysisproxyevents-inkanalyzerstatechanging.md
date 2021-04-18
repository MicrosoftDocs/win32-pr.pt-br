---
description: Ocorre antes de o IInkAnalyzer reconciliar os resultados da análise para que um aplicativo possa sincronizar dados com o IInkAnalyzer.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: 'Evento _IAnalysisProxyEvents:: InkAnalyzerStateChanging (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105789288"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_Evento IAnalysisProxyEvents:: InkAnalyzerStateChanging

Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) reconciliar os resultados da análise para que um aplicativo possa sincronizar dados com o **IInkAnalyzer**.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ no\]
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) que está prestes a reconciliar seus resultados de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Quando o **IInkAnalyzer** gera esse evento, seu aplicativo deve preencher os subnós do nó raiz do analisador de tinta (consulte o método [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) e [**IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)).

O [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de gerar o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) . Ele gera esse evento somente durante a execução da análise em segundo plano.

Bloqueie sua estrutura de dados quando o [**IInkAnalyzer**](iinkanalyzer.md) gerar o evento **\_ IAnalysisProxyEvents:: InkAnalyzerStateChanging** . As alterações na estrutura de dados durante esta fase de análise podem causar erros na análise de tinta e na sincronização. Desbloqueie sua estrutura de dados quando o **IInkAnalyzer** gerar o evento [**\_ IAnalysisEvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) ou [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

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

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




