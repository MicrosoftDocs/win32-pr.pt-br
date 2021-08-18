---
description: Remove uma dica de análise do IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: Método IInkAnalyzer::D eleteAnalysisHint (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6f514f20ed99f7fc56725f582b815639cb9d8b3179e9e428845d7e066b6e3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967285"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>Método IInkAnalyzer::D eleteAnalysisHint

Remove uma dica de análise do [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pHintToDelete* \[ Em\]
</dt> <dd>

A dica de análise do [**IInkAnalyzer.**](iinkanalyzer.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Remover uma dica de análise não marca a área da dica para reanálise. Para marcar a área dentro da dica para reanálise, use o Método [**IInkAnalyzer::SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para definir a região suja como a união da região suja atual e da área da dica de análise.

A dica é removida do analisador; no entanto, [**o próprio IContextNode**](icontextnode.md) não é excluído.

Esse método retorna um código de erro quando *pHintToDelete* é [**um IContextNode**](icontextnode.md) que não é do tipo AnalysisHint (consulte [**IContextNode::GetType**](icontextnode-gettype.md)).

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

[**Método IInkAnalyzer::CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Método IInkAnalyzer::GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Método IInkAnalyzer::GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




