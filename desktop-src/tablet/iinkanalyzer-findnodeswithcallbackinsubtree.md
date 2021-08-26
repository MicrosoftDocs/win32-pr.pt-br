---
description: Recupera todos os objetos IContextNode que corresponderem aos critérios especificados e são descendentes do objeto IContextNode especificado.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: Método IInkAnalyzer::FindNodesWithCallBackInSubTree (IACom.h)
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
ms.openlocfilehash: d6ab8e66e75af4e31a1efacd082f79f68d5f63c546c56d59bf4ca0fedc201929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939926"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a>Método IInkAnalyzer::FindNodesWithCallBackInSubTree

Recupera todos os objetos [**IContextNode**](icontextnode.md) que corresponderem aos critérios especificados e são descendentes do objeto **IContextNode** especificado.

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

*pCriteria* \[ Em\]
</dt> <dd>

Um [**objeto IMatchesCriteriaCallBack**](imatchescriteriacallback.md) usado para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em seus critérios especificados.

</dd> <dt>

*pContextNodeToSearchFrom* \[ Em\]
</dt> <dd>

O [**objeto IContextNode**](icontextnode.md) cujos descendentes são pesquisados.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

Um ponteiro para os [**IContextNodes que**](icontextnodes.md) contêm todos os nós que atendem aos critérios especificados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto .

 

Se [**o IInkAnalyzer**](iinkanalyzer.md) não contém o *nó pContextNodeToSearchFrom,* esse método retorna um código de erro.

Se [**O IInkAnalyzer**](iinkanalyzer.md) não contiver [**nenhum IContextNode,**](icontextnode.md)uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Método IInkAnalyzer::FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindInkLeafNodesForStrkes**](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindLeafNodes**](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNode**](iinkanalyzer-findnode.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesOfType**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesOfTypeForRogkes**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

