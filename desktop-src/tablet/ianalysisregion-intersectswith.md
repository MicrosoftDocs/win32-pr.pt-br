---
description: Determina se a área da IAnalysisRegion intersecções com o retângulo especificado.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: Método IAnalysisRegion::IntersectsWith (IACom.h)
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
ms.openlocfilehash: 04613e061929bba04c14be37914b22a51de0377f125b21fa29db9c56fc8dfeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720013"
---
# <a name="ianalysisregionintersectswith-method"></a>Método IAnalysisRegion::IntersectsWith

Determina se a área da [**IAnalysisRegion**](ianalysisregion.md) intersecções com o retângulo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRectangle* \[ Em\]
</dt> <dd>

Um ponteiro para o retângulo com o qual comparar, em coordenadas de espaço em tinta.

</dd> <dt>

*pfIsIntersecting* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** se a área da [**IAnalysisRegion**](ianalysisregion.md) intersecções com o retângulo especificado; caso contrário, **VARIANT \_ FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

A comparação está em coordenadas de espaço em tinta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




