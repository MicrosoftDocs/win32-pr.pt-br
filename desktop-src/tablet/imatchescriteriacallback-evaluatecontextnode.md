---
description: Quando substituído em uma classe derivada, avalia se um objeto IContextNode especificado atende aos critérios.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: Método IMatchesCriteriaCallBack::EvaluateContextNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d5855928e0827632240c8230bdcc57dff836c5287eec61f2911cc62367a8915f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719046"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>Método IMatchesCriteriaCallBack::EvaluateContextNode

Quando substituído em uma classe derivada, avalia se um objeto [**IContextNode**](icontextnode.md) especificado atende aos critérios.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContextNodeToEvaluate* \[ Em\]
</dt> <dd>

O [**objeto IContextNode**](icontextnode.md) a ser avaliada.

</dd> <dt>

*pbResult* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** se *pContextNodeToEvaluate corresponde* aos critérios; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Para usar [**o método IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md) ou o método [**IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md), crie uma classe que implemente [**IMatchesCriteriaCallBack.**](imatchescriteriacallback.md) Implemente **IMatchesCriteriaCallBack::EvaluateContextNode** para retornar **VARIANT \_ TRUE** se o objeto [**IContextNode**](icontextnode.md) corresponde aos seus critérios e **VARIANT \_ FALSE** caso contrário. Para alguns critérios, talvez seja necessário fornecer um meio de inicializar ou manter o estado do objeto **IMatchesCriteriaCallBack.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMatchesCriteriaCallBack**](imatchescriteriacallback.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Método IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




