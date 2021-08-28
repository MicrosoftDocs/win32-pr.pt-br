---
description: Recupera o IInkAnalysisRecognizer no índice especificado.
ms.assetid: e4db56c6-7c15-4336-bc0a-f50222c3520e
title: Método IInkAnalysisRecognizers::GetInkAnalysisRecognizer (IACom.h)
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
ms.openlocfilehash: 6755b82beaea1bec9a38b9c15ea57a97c1d19fc4eecb5a2b55c80e2070562d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967335"
---
# <a name="iinkanalysisrecognizersgetinkanalysisrecognizer-method"></a>Método IInkAnalysisRecognizers::GetInkAnalysisRecognizer

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

*ulIndex* \[ Em\]
</dt> <dd>

O índice baseado em zero do [**objeto IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) a ser obter.

</dd> <dt>

*ppInkAnalysisRecognizer* \[ out\]
</dt> <dd>

Um ponteiro para [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no índice especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, chame [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em \* *ppInkAnalysisRecognizer* quando você não precisar mais usar o reconhecedor de análise de tinta.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**InkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

