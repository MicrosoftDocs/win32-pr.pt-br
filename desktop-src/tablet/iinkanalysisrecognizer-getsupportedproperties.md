---
description: Recupera os GUIDs (identificadores globalmente exclusivos) para as propriedades que esse IInkAnalysisRecognizer pode gerar para resultados de análise.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: Método IInkAnalysisRecognizer::GetSupportedProperties (IACom.h)
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
ms.openlocfilehash: fce33317a234d82d6045dbefa93ed582d31d92f6ff54abe9ef87949559a5d269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057856"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>Método IInkAnalysisRecognizer::GetSupportedProperties

Recupera os GUIDs (identificadores globalmente exclusivos) para as propriedades que esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pode gerar para resultados de análise.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulPropertiesCount* \[ in, out\]
</dt> <dd>

O número de GUIDs em *ppProperties.*

</dd> <dt>

*ppProperties* \[ out\]
</dt> <dd>

Um ponteiro para os GUIDs de propriedades que esse [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) pode gerar para resultados de análise.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória de \* *ppProperties* quando você não precisar mais das informações.

 

Um reconhecedor pode dar suporte a métricas de linha, números de linha, níveis de confiança e assim por diante. Para ver uma lista completa das propriedades que um reconhecedor pode dar suporte, consulte [RecognitionProperty Constants](recognitionproperty-constants.md).

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
</dt> <dt>

[Constantes RecognitionProperty](recognitionproperty-constants.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

