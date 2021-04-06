---
description: Recupera uma matriz de intervalos de caracteres que representa os intervalos de caracteres Unicode com suporte.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Método IInkAnalysisRecognizer:: GetUnicodeRanges (IACom. h)'
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
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827183"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>Método IInkAnalysisRecognizer:: GetUnicodeRanges

Recupera uma matriz de intervalos de caracteres que representa os intervalos de caracteres Unicode com suporte.

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

*pulNumberOfRanges* \[ entrada, saída\]
</dt> <dd>

O número de intervalos de caracteres apontados por *ppulLowUnicode*.

</dd> <dt>

*ppulLowUnicode* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de intervalos de caracteres que representa os intervalos de caracteres Unicode com suporte.

</dd> <dt>

*ppusUnicodeRangeLength* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de valores que indica o comprimento de cada ponto de matriz para por *ppulLowUnicode*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




