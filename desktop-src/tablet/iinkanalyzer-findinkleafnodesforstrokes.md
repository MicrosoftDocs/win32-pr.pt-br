---
description: Recupera os nós folha de tinta que contêm os traços especificados.
ms.assetid: d9ebc57d-63f5-4175-8bb6-a688b98823d4
title: Método IInkAnalyzer::FindInkLeafNodesForRogkes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindInkLeafNodesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a7424f62008e15feb538df7a6a27745dda17bf6ace4612218608f8e509e75e59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967275"
---
# <a name="iinkanalyzerfindinkleafnodesforstrokes-method"></a>Método IInkAnalyzer::FindInkLeafNodesForStrkes

Recupera os nós folha de tinta que contêm os traços especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindInkLeafNodesForStrokes(
  [in]  ULONG         ulStrokeIdsCount,
  [in]  LONG          *plStrokeIds,
  [out] IContextNodes **ppContextNodesFound
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ Em\]
</dt> <dd>

O número de identificadores de traço passados.

</dd> <dt>

*plRogkeIds* \[ Em\]
</dt> <dd>

Uma matriz dos identificadores de traço.

</dd> <dt>

*ppContextNodesFound* \[ out\]
</dt> <dd>

A coleção de [**objetos IContextNode**](icontextnode.md) que contêm todos os nós folha de tinta que contêm os traços com identificadores na *matriz plStrkeIds.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em *ppContextNodesFound* quando você não precisar mais usar o objeto .

 

Nós folha não contêm nós filho. Nós de tinta contêm dados de traço. Exemplos de nós folha de tinta são objetos InkWord, InkDrawing eInkBullet [**IContextNode.**](icontextnode.md) Para obter mais informações, consulte [Tipos de nó de contexto](context-node-types.md).

Se nenhum dos nós contém os traços especificados, uma coleção [**IContextNodes**](icontextnodes.md) vazia será retornada. Da mesma forma, *se ulStrkeIdsCount* for zero, uma **coleção IContextNodes** vazia será retornada.

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

[**Método IInkAnalyzer::FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

