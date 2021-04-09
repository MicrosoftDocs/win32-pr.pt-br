---
description: Recupera as alternativas de análise para os traços com os identificadores de traço especificados.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Método IInkAnalyzer:: GetAlternatesForStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090525"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a>Método IInkAnalyzer:: GetAlternatesForStrokes

Recupera as alternativas de análise para os traços com os identificadores de traço especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdsCount* \[ no\]
</dt> <dd>

O número de identificadores de traço em *plStrokes*.

</dd> <dt>

*plStrokes* \[ no\]
</dt> <dd>

A matriz de identificadores de traço.

</dd> <dt>

*ulMaximumAlternates* \[ no\]
</dt> <dd>

O número máximo de alternativas de análise retornado.

</dd> <dt>

*ppAlternates* \[ fora\]
</dt> <dd>

O objeto [**IAnalysisAlternates**](ianalysisalternates.md) que contém as alternativas de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppAlternates* quando você não precisar mais usar o objeto.

 

O [**IAnalysisAlternate**](ianalysisalternate.md) superior é retornado como a primeira alternativa da coleção.

Os traços especificados não precisam representar áreas adjacentes do documento.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**Método IInkAnalyzer:: getalternations**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Método IInkAnalyzer:: ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Método IInkAnalyzer:: ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

