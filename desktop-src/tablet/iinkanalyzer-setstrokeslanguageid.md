---
description: Altera o identificador de localidade para os traços especificados.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'Método IInkAnalyzer:: SetStrokesLanguageId (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2a063180d89fd9f29ebcacd5b9cbd9e98e4299d82aac2328b08624e3c1557249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590336"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a>Método IInkAnalyzer:: SetStrokesLanguageId

Altera o identificador de localidade para os traços especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulStrokeIdCount* \[ no\]
</dt> <dd>

O número de identificadores de traço em *plStrokes*.

</dd> <dt>

*plStrokes* \[ no\]
</dt> <dd>

A matriz de identificadores para os traços aos quais atribuir o identificador de localidade.

</dd> <dt>

*lStrokesLCID* \[ no\]
</dt> <dd>

O identificador de localidade a ser atribuído aos traços.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

A localidade de um traço é definida quando você adiciona o traço chamando [**IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md), o método [**IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), o método [**IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)ou o [**método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Para obter a localidade atualmente atribuída a um traço, chame o [**método IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).

Os traços especificados são movidos para um nó de tinta não classificado (consulte [**IContextNode:: GetType**](icontextnode-gettype.md)) que contém traços do mesmo idioma. Se não existir tal [**IContextNode**](icontextnode.md) , esse método criará um novo nó de tinta não classificada e moverá os traços para ele. Um nó de tinta não classificado é um **IContextNode** que tem um tipo de UnclassifiedInk.

Se esse método mover traços de um [**IContextNode**](icontextnode.md) que não seja um nó de tinta não classificado, esse método também adicionará as caixas delimitadoras de traços à região suja do Ink Analyzer (consulte o [**método IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Esse método não moverá um traço se o parâmetro *lStrokeLCID* corresponder ao identificador de idioma atual do traço.

Se um traço especificado não estiver associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método ignorará o identificador.

Se nenhum dos traços especificados identificar um traço associado ao [**IInkAnalyzer**](iinkanalyzer.md), esse método retornará sem Atualizar o **IInkAnalyzer**.

Esse método retorna um código de erro quando strokeIds é **nulo**.

Para obter mais informações sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).

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

[**Método IInkAnalyzer:: addstroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Método IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Método IInkAnalyzer:: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**Método IInkAnalyzer:: SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

