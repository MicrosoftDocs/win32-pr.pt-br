---
description: Ocorre antes de o IInkAnalyzer executar a análise dentro da região de um objeto IContextNode parcialmente populado.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P evento opulateContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ff6378f7ecf3ff597f4c02740e30544ff65651d0a7fcd6d6d490ebabf2161ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967925"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a>\_IAnalysisProxyEvents: evento opulateContextNode de:P

Ocorre antes de o [**IInkAnalyzer**](iinkanalyzer.md) executar a análise dentro da região de um objeto [**IContextNode**](icontextnode.md) parcialmente populado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ no\]
</dt> <dd>

O objeto [**IInkAnalyzer**](iinkanalyzer.md) prestes a executar a análise.

</dd> <dt>

*pContextNodeToPopulate* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) parcialmente preenchido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Quando o **IInkAnalyzer** gera esse evento, seu aplicativo deve preencher o *pContextNodeToPopulate*. Durante a fase de análise, o **IInkAnalyzer** gera esse evento para obter informações sobre áreas nas quais está analisando a tinta.

Se o documento contiver links para o *pContextNodeToPopulate*, seu aplicativo deverá criar e adicionar esses links. Esse processo requer que os nós de origem e de destino, incluindo seus ancestrais, sejam totalmente preenchidos antes que o manipulador de eventos para esse evento saia (consulte [**IContextLink:: GetSourceNode**](icontextlink-getsourcenode.md) e [**IContextLink:: GetDestinationNode**](icontextlink-getdestinationnode.md)).

Para obter mais informações sobre como sincronizar os dados do aplicativo com o [**IInkAnalyzer**](iinkanalyzer.md), consulte [proxy de dados com análise de tinta](data-proxy-with-ink-analysis.md).

Durante a análise em segundo plano, o [**IInkAnalyzer**](iinkanalyzer.md) gera esse evento depois de gerar o evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
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

 

 




