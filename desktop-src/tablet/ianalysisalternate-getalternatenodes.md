---
description: Obtém os objetos IContextNode associados a essa alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: Método IAnalysisAlternate::GetAlternateNodes (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetAlternateNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fbaff3cea515c9636127ce2267b9f05e0c0a0006b96046a7f2474661b3b76f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935516"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>Método IAnalysisAlternate::GetAlternateNodes

Obtém [**os objetos IContextNode**](icontextnode.md) associados a essa alternativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAlternateNodes* \[ out\]
</dt> <dd>

Um ponteiro para a [**coleção IContextNodes**](icontextnodes.md) que contém [**objetos IContextNode**](icontextnode.md) associados a essa alternativa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppAlternateNodes* quando você não precisar mais usar a coleção de nós de contexto.

 

Esse método retorna os nós de contexto folha associados a essa alternativa. Exemplos de nós folha são nós de contexto InkWord, TextWord, Image, InkDrawing e InkBullet. Para obter mais informações, consulte [**IContextNode::GetType e**](icontextnode-gettype.md) [Tipos de nó de contexto](context-node-types.md).

Como eles correspondem a alternativas, esses objetos [**IContextNode**](icontextnode.md) não são descendentes do **IContextNode** raiz do objeto [**IInkAnalyzer**](iinkanalyzer.md) (consulte [**Método IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md)), a menos que sejam o principal alternativo, que é o primeiro elemento em uma [**coleção IAnalysisAlternates.**](ianalysisalternates.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> <dt>

[Sistema. Windows. Ink.AnalysisCore.AnalysisAlternateBase.AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

