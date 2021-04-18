---
description: Recupera todos os objetos IContextNode do tipo especificado que contêm os traços especificados.
ms.assetid: c674a03b-841c-4a9c-8268-302bc4038934
title: 'Método IInkAnalyzer:: FindNodesOfTypeForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dd98c72007a69521506e2be21ad10edeb46df27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815475"
---
# <a name="iinkanalyzerfindnodesoftypeforstrokes-method"></a>Método IInkAnalyzer:: FindNodesOfTypeForStrokes

Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado que contêm os traços especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindNodesOfTypeForStrokes(
  [in]  const GUID          *pNodeType,
  [in]        ULONG         ulStrokeIdsCount,
  [in]        LONG          *plStrokeIds,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNodeType* \[ no\]
</dt> <dd>

O GUID (identificador global exclusivo) que especifica o tipo de nó.

</dd> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de identificadores de traço passados.

</dd> <dt>

*plStrokeIds* \[ no\]
</dt> <dd>

Uma matriz dos identificadores de traço.

</dd> <dt>

*ppContextNodesFound* \[ fora\]
</dt> <dd>

A coleção de objetos [**IContextNode**](icontextnode.md) que contém todos os nós do tipo *pNodeType* que contêm os traços com identificadores na matriz *plStrokeIds* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppContextNodesFound* quando você não precisar mais usar o objeto.

 

A propriedade *pNodeType* deve conter um GUID das constantes de [tipos de nó de contexto](context-node-types.md) .

Se o tipo de nó especificado não for um nó folha, mas um dos descendentes do nó fizer referência a um traço na coleção de traços, esse nó será adicionado à coleção retornada.

Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver tal [**IContextNode**](icontextnode.md), uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindLeafNodes**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

