---
description: Recupera os identificadores globalmente exclusivos (GUIDs) para as propriedades que esse IInkAnalysisRecognizer pode gerar para os resultados da análise.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'Método IInkAnalysisRecognizer:: GetSupportedProperties (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920953"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>Método IInkAnalysisRecognizer:: GetSupportedProperties

Recupera os identificadores globalmente exclusivos (GUIDs) para as propriedades que esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pode gerar para os resultados da análise.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulPropertiesCount* \[ entrada, saída\]
</dt> <dd>

O número de GUIDs em *ppProperties*.

</dd> <dt>

*ppProperties* \[ fora\]
</dt> <dd>

Um ponteiro para os GUIDs de propriedades que esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pode gerar para resultados de análise.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppProperties* quando você não precisar mais das informações.

 

Um reconhecedor pode dar suporte A métricas de linha, números de linha, níveis de confiança e assim por diante. Para obter uma lista completa das propriedades às quais um reconhecedor pode dar suporte, consulte [constantes](recognitionproperty-constants.md)recognizeproperty.

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

[Constantes rerecognitionproperty](recognitionproperty-constants.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

