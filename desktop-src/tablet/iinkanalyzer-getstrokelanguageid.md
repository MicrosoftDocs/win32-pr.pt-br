---
description: Retorna o identificador de localidade do traço especificado.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Método IInkAnalyzer:: GetStrokeLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647225"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>Método IInkAnalyzer:: GetStrokeLanguageId

Retorna o identificador de localidade do traço especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrokeId* \[ no\]
</dt> <dd>

O identificador de traço.

</dd> <dt>

*lStrokeLCID* \[ fora\]
</dt> <dd>

O identificador de localidade para o traço especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

A localidade do traço é definida quando você adiciona o traço chamando [**IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md), o método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), o método [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)ou o [**método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Para alterar a localidade do traço, use o método [**IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md) ou o método [**IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).

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

[**Método IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




