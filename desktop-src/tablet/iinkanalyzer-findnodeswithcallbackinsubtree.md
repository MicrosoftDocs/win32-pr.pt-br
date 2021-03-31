---
description: Recupera todos os objetos IContextNode que correspondem aos critérios especificados e são descendentes do objeto IContextNode especificado.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Método IInkAnalyzer:: FindNodesWithCallBackInSubTree (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647231"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>Método IInkAnalyzer:: FindNodesWithCallBackInSubTree

Recupera todos os objetos [**IContextNode**](icontextnode.md) que correspondem aos critérios especificados e são descendentes do objeto **IContextNode** especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCriteria* \[ no\]
</dt> <dd>

Um objeto [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) que é usado para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em seus critérios especificados.

</dd> <dt>

*pContextNodeToSearchFrom* \[ no\]
</dt> <dd>

O objeto [**IContextNode**](icontextnode.md) cujos descendentes são pesquisados.

</dd> <dt>

*ppContextNodesFound* \[ fora\]
</dt> <dd>

Um ponteiro para o [**IContextNodes**](icontextnodes.md) que contém todos os nós que atendem aos critérios especificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto.

 

Se o [**IInkAnalyzer**](iinkanalyzer.md) não contiver o nó *pContextNodeToSearchFrom* , esse método retornará um código de erro.

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

[**Método IInkAnalyzer:: FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

