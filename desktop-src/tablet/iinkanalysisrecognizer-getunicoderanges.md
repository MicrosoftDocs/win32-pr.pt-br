---
description: Recupera uma matriz de intervalos de caracteres que representam os intervalos de caracteres Unicode com suporte.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: Método IInkAnalysisRecognizer::GetUnicodeRanges (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cf8c0fe75d2eff0cdd8f2f9d3eb5366f6bab4dd4588c854455804ce4196971bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008396"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>Método IInkAnalysisRecognizer::GetUnicodeRanges

Recupera uma matriz de intervalos de caracteres que representam os intervalos de caracteres Unicode com suporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulNumberOfRanges* \[ in, out\]
</dt> <dd>

O número de intervalos de caracteres apontados por *ppulLowUnicode.*

</dd> <dt>

*ppulLowUnicode* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de intervalos de caracteres que representam os intervalos de caracteres Unicode com suporte.

</dd> <dt>

*ppusUnicodeRangeLength* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de valores que indica o comprimento de cada ponto de matriz para *por ppulLowUnicode.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




