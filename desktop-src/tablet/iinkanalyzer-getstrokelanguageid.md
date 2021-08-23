---
description: Retorna o identificador de localidade do traço especificado.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: Método IInkAnalyzer::GetEntrokeLanguageId (IACom.h)
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
ms.openlocfilehash: 8b61bfa61b4e4aa2c8415c9596cb97a3b0c1313cf3a080d065a7c82e4d69b84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713386"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a>Método IInkAnalyzer::GetEntrokeLanguageId

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

*lStrkeId* \[ Em\]
</dt> <dd>

O identificador de traço.

</dd> <dt>

*lRogkeLCID* \[ out\]
</dt> <dd>

O identificador de localidade para o traço especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

A localidade do traço é definida quando você adiciona o traço chamando o método [**IInkAnalyzer::AddStrke**](iinkanalyzer-addstroke.md), [**Método IInkAnalyzer::AddRogkeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**Método IInkAnalyzer::AddEntrokes**](iinkanalyzer-addstrokes.md)ou Método [**IInkAnalyzer::Add IssokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Para alterar a localidade do traço, use o Método [**IInkAnalyzer::SetOsekeLanguageId**](iinkanalyzer-setstrokelanguageid.md) ou o Método [**IInkAnalyzer::SetOsekesLanguageId**](iinkanalyzer-setstrokeslanguageid.md).

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

[**Método IInkAnalyzer::SetRogkeLanguageId**](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[**Método IInkAnalyzer::SetRogkesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




