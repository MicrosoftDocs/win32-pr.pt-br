---
description: Recupera o IInkAnalysisRecognizer no índice especificado.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: 'Método IInkAnalysisRecognizers:: GetInkAnalysisRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1008ae0b26d30233c3b00167391523d321cd381e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461152"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>Método IInkAnalysisRecognizers:: GetInkAnalysisRecognizer

Recupera o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no índice especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetInkAnalysisRecognizer(
  [in]  ULONG                  ulIndex,
  [out] IInkAnalysisRecognizer **ppInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulIndex* \[ no\]
</dt> <dd>

O índice de base zero do objeto [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) a ser obtido.

</dd> <dt>

*ppInkAnalysisRecognizer* \[ fora\]
</dt> <dd>

Um ponteiro para o [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no índice especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppInkAnalysisRecognizer* quando você não precisar mais usar o reconhecedor de análise de tinta.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

