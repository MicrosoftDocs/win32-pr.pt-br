---
description: Expõe um método para avaliar se um objeto IContextNode atende ou falha em um critério especificado.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Interface IMatchesCriteriaCallBack (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc661f47c77d615df95f63e58beccbbf125b93078392a63f86ed50f52cc5636d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718965"
---
# <a name="imatchescriteriacallback-interface"></a>Interface IMatchesCriteriaCallBack

Expõe um método para avaliar se um objeto [**IContextNode**](icontextnode.md) atende ou falha em um critério especificado.

## <a name="members"></a>Membros

A interface **IMatchesCriteriaCallBack** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMatchesCriteriaCallBack** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMatchesCriteriaCallBack** tem esses métodos.



| Método                                                                      | Descrição                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) | Quando substituído em uma classe derivada, avalia se um objeto [**IContextNode**](icontextnode.md) especificado atende aos critérios.<br/> |



 

## <a name="remarks"></a>Comentários

Para usar o método [**IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou [**IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), crie uma classe que implemente **IMatchesCriteriaCallBack**. Implemente [**IMatchesCriteriaCallBack:: EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) para retornar **Variant \_ true** se o objeto [**IContextNode**](icontextnode.md) corresponder aos seus critérios e **Variant \_ false** caso contrário. Para alguns critérios, talvez seja necessário fornecer um meio de inicializar ou manter o estado do seu objeto **IMatchesCriteriaCallBack** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método IInkAnalyzer:: FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Método IInkAnalyzer:: FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

