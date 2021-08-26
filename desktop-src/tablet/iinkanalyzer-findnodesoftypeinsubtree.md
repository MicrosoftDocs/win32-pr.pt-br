---
description: Recupera todos os objetos IContextNode do tipo especificado que são descendentes do objeto IContextNode especificado.
ms.assetid: 7e57d6ec-fe04-44c6-904f-7a212bbfcd19
title: 'Método IInkAnalyzer:: FindNodesOfTypeInSubTree (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesOfTypeInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 16e1516a8da5b4d09b80606bad5cf5f9444d82545394543c46b06a05425befa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939936"
---
# <a name="iinkanalyzerfindnodesoftypeinsubtree-method"></a>Método IInkAnalyzer:: FindNodesOfTypeInSubTree

Recupera todos os objetos [**IContextNode**](icontextnode.md) do tipo especificado que são descendentes do objeto **IContextNode** especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindNodesOfTypeInSubTree(
  [in]  const GUID          *pNodeType,
  [in]        IContextNode  *pContextNodeToSearchFrom,
  [out]       IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNodeType* \[ no\]
</dt> <dd>

O **GUID** que especifica o tipo de nó.

</dd> <dt>

*pContextNodeToSearchFrom* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) cujos descendentes são pesquisados.

</dd> <dt>

*ppContextNodesFound* \[ fora\]
</dt> <dd>

A coleção [**IContextNodes**](icontextnodes.md) que contém todos os nós do tipo *pNodeType* que são descendentes de *pContextNodeToSearchFrom*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.

 

Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver o nó *pContextNodeToSearchFrom* , esse método retornará um código de erro.

A propriedade *pNodeType* deve conter um GUID (identificador global exclusivo) das constantes de [tipos de nó de contexto](context-node-types.md) .

Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver tal [**IContextNode**](icontextnode.md), uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
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

[**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

