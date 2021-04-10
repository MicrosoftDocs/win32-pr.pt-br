---
description: Modifica a área que foi alterada desde a última operação de análise.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Método IInkAnalyzer:: SetDirtyRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090516"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>Método IInkAnalyzer:: SetDirtyRegion

Modifica a área que foi alterada desde a última operação de análise.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDirtyRegion* \[ no\]
</dt> <dd>

Um [**IAnalysisRegion**](ianalysisregion.md) que descreve a área que foi alterada desde a última operação de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Esse método identifica as áreas que precisam ser analisadas ou analisadas novamente. Todos os métodos [**IInkAnalyzer**](iinkanalyzer.md) que adicionam, atualizam ou removem dados de traço atualizam a região suja. Para marcar manualmente uma área para reanálise:

1.  Obtenha a região suja usando o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md).
2.  Use o método [**IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md) ou [**IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md) para adicionar a área à região da etapa 1.
3.  Use o **método IInkAnalyzer:: SetDirtyRegion** para atualizar a região suja.

O [**IInkAnalyzer**](iinkanalyzer.md) analisa a tinta em sua região suja durante uma chamada para o método [**IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md). No entanto, o **IInkAnalyzer** pode expandir a operação de análise para incluir regiões vizinhas.

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

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




