---
description: Remove uma dica de análise do IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: 'IInkAnalyzer: método eleteAnalysisHint de:D (IACom. h)'
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
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090530"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>IInkAnalyzer: método eleteAnalysisHint de:D

Remove uma dica de análise do [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pHintToDelete* \[ no\]
</dt> <dd>

A dica de análise do [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Remover uma dica de análise não marca a área da dica para reanálise. Para marcar a área dentro da dica para reanálise, use o [**método IInkAnalyzer:: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) para definir a região suja como a União da região suja atual e da área da dica de análise.

A dica é removida do analisador; no entanto, o próprio [**IContextNode**](icontextnode.md) não é excluído.

Esse método retorna um código de erro quando *pHintToDelete* é um [**IContextNode**](icontextnode.md) que não é do tipo AnalysisHint (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)).

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

[**Método IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisHints**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




