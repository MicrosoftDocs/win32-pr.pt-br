---
description: Recupera os identificadores para as localidades às quais esse IInkAnalysisRecognizer dá suporte.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'Método IInkAnalysisRecognizer:: GetLanguages (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827184"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>Método IInkAnalysisRecognizer:: GetLanguages

Recupera os identificadores para as localidades às quais esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dá suporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulLanguagesCount* \[ entrada, saída\]
</dt> <dd>

O número de identificadores em *ppulLanguages*.

</dd> <dt>

*ppulLanguages* \[ fora\]
</dt> <dd>

Um ponteiro para os identificadores para as localidades às quais esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dá suporte.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppulLanguages* quando você não precisar mais das informações.

 

Esse método retorna uma matriz vazia para reconhecedores de objeto e de gesto.

Para obter mais informações sobre identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).

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
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

