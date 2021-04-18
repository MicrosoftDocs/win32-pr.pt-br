---
description: Ocorre quando o IInkAnalyzer move um traço de um objeto IContextNode para outro.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: 'Evento _IAnalysisProxyEvents:: StrokeReparented (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105793260"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a>\_Evento IAnalysisProxyEvents:: StrokeReparented

Ocorre quando o [**IInkAnalyzer**](iinkanalyzer.md) move um traço de um objeto [**IContextNode**](icontextnode.md) para outro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ no\]
</dt> <dd>

O objeto [**IInkAnalyzer**](iinkanalyzer.md) que move o traço.

</dd> <dt>

*lStrokeIdToMove* \[ no\]
</dt> <dd>

O identificador do traço a ser movido.

</dd> <dt>

*pSourceContextNode* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) do qual o traço é movido.

</dd> <dt>

*pDestinationContextNode* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) para o qual o traço é movido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método **IInkAnalyzer** que move dados de traço de um [**IContextNode**](icontextnode.md) para outro.

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

 

 




