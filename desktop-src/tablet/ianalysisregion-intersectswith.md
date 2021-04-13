---
description: Determina se a área do IAnalysisRegion intersecciona com o retângulo especificado.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Método IAnalysisRegion:: IntersectsWith (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501822"
---
# <a name="ianalysisregionintersectswith-method"></a>Método IAnalysisRegion:: IntersectsWith

Determina se a área do [**IAnalysisRegion**](ianalysisregion.md) intersecciona com o retângulo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRectangle* \[ no\]
</dt> <dd>

Um ponteiro para o retângulo com o qual comparar, em coordenadas de espaço de tinta.

</dd> <dt>

*pfIsIntersecting* \[ fora\]
</dt> <dd>

**Variante \_ TRUE** se a área do [**IAnalysisRegion**](ianalysisregion.md) Interseccionar com o retângulo especificado; caso contrário, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

A comparação está em coordenadas de espaço de tinta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




