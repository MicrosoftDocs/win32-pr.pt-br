---
description: Ocorre depois que o IInkAnalyzer cria um objeto IContextNode.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: _IAnalysisProxyEvents::ContextNodeCreated event (IACom.h)
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
ms.openlocfilehash: 5938ffda54542602248c5d04da0726d932b381aaff092f1c2038dd37ae4631e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675863"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeCreated

Ocorre depois que [**o IInkAnalyzer**](iinkanalyzer.md) cria um [**objeto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ Em\]
</dt> <dd>

O [**IInkAnalyzer que**](iinkanalyzer.md) cria o [**objeto IContextNode.**](icontextnode.md)

</dd> <dt>

*pContextNodeCreated* \[ Em\]
</dt> <dd>

O novo [**objeto IContextNode.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer.**](iinkanalyzer.md) Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método de analisador de tinta que cria [**um IContextNode.**](icontextnode.md)

Quando [**o IInkAnalyzer**](iinkanalyzer.md) cria um [**IContextNode**](icontextnode.md), o novo **IContextNode** não contém nenhum traço, não contém links para outros objetos **IContextNode** e pode não ter todas as suas propriedades definidas. Além disso, o **novo IContextNode** é adicionado ao final da coleção de subnónodos do nó pai (consulte [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)). Após esse evento, **o IInkAnalyzer** pode auerá-los.

-   O [**\_ evento IAnalysisProxyEvents::StrokeReparented**](-ianalysisproxyevents-strokereparented.md) quando ele move um traço de um nó de contexto para outro.
-   O [**\_ evento IAnalysisProxyEvents::ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) quando ele adiciona [**um IContextLink**](icontextlink.md) a [**um IContextNode.**](icontextnode.md)
-   O [**\_ evento IAnalysisProxyEvents::ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) quando ele altera a ordem de [**um IContextNode**](icontextnode.md) dentro da coleção de subnónodos de seu nó pai.
-   O [**IInkAnalyzer**](iinkanalyzer.md) gera o evento [**\_ IAnalysisProxyEvents::ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) depois de resolver o estado do [**IContextNode**](icontextnode.md) para essa fase de análise.

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

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




