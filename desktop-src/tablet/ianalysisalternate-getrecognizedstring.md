---
description: Obtém o valor de cadeia de caracteres reconhecido do objeto IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'Método IAnalysisAlternate:: reconhecívelstring (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501828"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>Método IAnalysisAlternate:: reconhecívelstring

Obtém o valor de cadeia de caracteres reconhecido do objeto [**IAnalysisAlternate**](ianalysisalternate.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrRecognizedString* \[ fora\]
</dt> <dd>

Um ponteiro para o **BSTR** que é definido como o valor de cadeia de caracteres reconhecido.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**Método IInkAnalyzer:: reconhecívelstring**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




