---
description: Obtém os objetos IContextNode associados a essa alternativa.
ms.assetid: 6dfae9cc-d9d2-44de-b6cf-80bbcd296390
title: 'Método IAnalysisAlternate:: GetAlternateNodes (IACom. h)'
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
ms.openlocfilehash: dd24581774c2115c9f7ccb6857d0cd4d9e1bfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759921"
---
# <a name="ianalysisalternategetalternatenodes-method"></a>Método IAnalysisAlternate:: GetAlternateNodes

Obtém os objetos [**IContextNode**](icontextnode.md) associados a essa alternativa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAlternateNodes(
  [out] IContextNodes **ppAlternateNodes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppAlternateNodes* \[ fora\]
</dt> <dd>

Um ponteiro para a coleção [**IContextNodes**](icontextnodes.md) que contém objetos [**IContextNode**](icontextnode.md) associados a essa alternativa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppAlternateNodes* quando você não precisar mais usar a coleção de nós de contexto.

 

Esse método retorna os nós de contexto folha que estão associados a essa alternativa. Exemplos de nós folha são nós de contexto InkWord, textword, Image, InkDrawing e InkBullet. Para obter mais informações, consulte [**IContextNode:: GetType**](icontextnode-gettype.md) e [tipos de nó de contexto](context-node-types.md).

Como elas correspondem a alternativas, esses objetos [**IContextNode**](icontextnode.md) não são descendentes do **IContextNode** raiz do objeto [**IInkAnalyzer**](iinkanalyzer.md) (Confira o [**método IInkAnalyzer:: GetRootNode**](iinkanalyzer-getrootnode.md)), a menos que eles sejam a alternativa principal, que é o primeiro elemento em uma coleção [**IAnalysisAlternates**](ianalysisalternates.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
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

[System. Windows. Ink. AnalysisCore. AnalysisAlternateBase. AlternateNodes](ianalysisalternate-getalternatenodes.md)
</dt> </dl>

 

