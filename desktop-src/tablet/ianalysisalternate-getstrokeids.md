---
description: Retorna os identificadores de traço associados a este IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'Método IAnalysisAlternate:: GetStrokeIds (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827195"
---
# <a name="ianalysisalternategetstrokeids-method"></a>Método IAnalysisAlternate:: GetStrokeIds

Retorna os identificadores de traço associados a este [**IAnalysisAlternate**](ianalysisalternate.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulStrokeIdsCount* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para um **ULONG** que é definido como o número de identificadores de traço associados a este [**IAnalysisAlternate**](ianalysisalternate.md).

</dd> <dt>

*pplStrokeIds* \[ fora\]
</dt> <dd>

\[out, tamanho \_ é ( \* *PULSTROKEIDSCOUNT* \* sizeof (Long))\]

Uma matriz de *pulStrokeIdsCount* de comprimento **longa** que é definida para os identificadores de traço associados a esse [**IAnalysisAlternate**](ianalysisalternate.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *pplStrokeIds* quando você não precisar mais das informações.

 

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

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

