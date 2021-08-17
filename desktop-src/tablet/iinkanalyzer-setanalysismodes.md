---
description: Modifica os sinalizadores que controlam como o IInkAnalyzer executa a análise de tinta.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: 'Método IInkAnalyzer:: SetAnalysisModes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7edd167cd40b80a01fd2f23243c931fe6a15795da08d7735b6e2433c462ee01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091487"
---
# <a name="iinkanalyzersetanalysismodes-method"></a>Método IInkAnalyzer:: SetAnalysisModes

Modifica os sinalizadores que controlam como o [**IInkAnalyzer**](iinkanalyzer.md) executa a análise de tinta.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*analysismode* \[ no\]
</dt> <dd>

Uma combinação de bits de bit que contenha valores de enumeração [**AnalysisModes**](analysismodes.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




