---
description: Ocorre depois que o IInkAnalyzer cria um objeto IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Evento _IAnalysisProxyEvents:: ContextNodeCreated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930233"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Evento IAnalysisProxyEvents:: ContextNodeCreated

Ocorre depois que o [**IInkAnalyzer**](iinkanalyzer.md) cria um objeto [**IContextNode**](icontextnode.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ no\]
</dt> <dd>

O [**IInkAnalyzer**](iinkanalyzer.md) criando o objeto [**IContextNode**](icontextnode.md) .

</dd> <dt>

*pContextNodeCreated* \[ no\]
</dt> <dd>

O novo objeto [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer**](iinkanalyzer.md). Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método do analisador de tinta que cria um [**IContextNode**](icontextnode.md).

Quando o [**IInkAnalyzer**](iinkanalyzer.md) cria um [**IContextNode**](icontextnode.md), o novo **IContextNode** não contém traços, não contém links para outros objetos do **IContextNode** e pode não ter todas as suas propriedades definidas. Além disso, o novo **IContextNode** é adicionado ao final da coleção de subnós do seu nó pai (consulte [**IContextNode:: GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md)). Após esse evento, o **IInkAnalyzer** pode gerar os eventos a seguir.

-   O evento [**\_ IAnalysisProxyEvents:: StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando move um traço de um nó de contexto para outro.
-   O evento [**\_ IAnalysisProxyEvents:: ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) quando ele adiciona um [**IContextLink**](icontextlink.md) a um [**IContextNode**](icontextnode.md).
-   O evento [**\_ IAnalysisProxyEvents:: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) quando ele altera a ordem de um [**IContextNode**](icontextnode.md) dentro de sua coleção de subnós do nó pai.
-   O [**IInkAnalyzer**](iinkanalyzer.md) gera o evento [**\_ IAnalysisProxyEvents:: ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) depois de resolver o estado do [**IContextNode**](icontextnode.md) para esta fase de análise.

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

 

 




