---
description: Retorna os identificadores de traço associados a este IAnalysisAlternate.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: Método IAnalysisAlternate::GetRogkeIds (IACom.h)
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
ms.openlocfilehash: 2682107a58f126011c4d80a02a119219ccea0976408937e19eb7b511eb82cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967495"
---
# <a name="ianalysisalternategetstrokeids-method"></a>Método IAnalysisAlternate::GetRogkeIds

Retorna os identificadores de traço associados a [**este IAnalysisAlternate.**](ianalysisalternate.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pulStrokeIdsCount* \[ in, out\]
</dt> <dd>

Um ponteiro para um **ULONG** definido como o número de identificadores de traço associados a [**este IAnalysisAlternate.**](ianalysisalternate.md)

</dd> <dt>

*pplStrkeIds* \[ out\]
</dt> <dd>

\[out, size \_ is( \* *pulStrkeIdsCount* \* sizeof(LONG))\]

Uma matriz **de LONG** de comprimento *pulRogkeIdsCount* que é definida para os identificadores de traço associados a [**este IAnalysisAlternate.**](ianalysisalternate.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar uma perda de memória, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória de \* *pplStrkeIds* quando você não precisar mais das informações.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

