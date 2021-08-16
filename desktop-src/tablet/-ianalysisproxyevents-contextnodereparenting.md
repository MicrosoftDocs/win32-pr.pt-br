---
description: Ocorre antes que o IInkAnalyzer mova um objeto IContextNode alterando seu nó pai.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: _IAnalysisProxyEvents::Evento ContextNodeReparenting (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eafb37fd4083f0ecf7c68eaf45fc3339a730e818864f4be15eca4b94d4bd5b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857105"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_Evento IAnalysisProxyEvents::ContextNodeReparenting

Ocorre antes que [**o IInkAnalyzer**](iinkanalyzer.md) mova um [**objeto IContextNode**](icontextnode.md) alterando seu nó pai.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pInkAnalyzer* \[ Em\]
</dt> <dd>

O [**objeto IInkAnalyzer**](iinkanalyzer.md) movendo o [**objeto IContextNode.**](icontextnode.md)

</dd> <dt>

*pNewParentContextNode* \[ Em\]
</dt> <dd>

O novo objeto [**IContextNode**](icontextnode.md) pai.

</dd> <dt>

*pContextNodeToBeReparented* \[ Em\]
</dt> <dd>

O [**objeto IContextNode**](icontextnode.md) a ser movido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Use esse evento quando seu aplicativo mantiver sua própria estrutura de dados, que é sincronizada com a do [**IInkAnalyzer.**](iinkanalyzer.md) Esse evento ocorre durante a fase de reconciliação da análise de tinta ou em resposta a um método que move um [**IContextNode**](icontextnode.md) de uma coleção de subnodes para outra (consulte [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) e [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).

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

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[**Método IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




