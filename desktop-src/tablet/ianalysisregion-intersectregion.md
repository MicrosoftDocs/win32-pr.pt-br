---
description: Restringe a área de IAnalysisRegion para a área criada por sua interseção com o IAnalysisRegion especificado.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'Método IAnalysisRegion:: IntersectRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0db58dcc7fc1c1e7458cf804eb82af236de8f1997ddcc658391da19641d1cfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058076"
---
# <a name="ianalysisregionintersectregion-method"></a>Método IAnalysisRegion:: IntersectRegion

Restringe a área de [**IAnalysisRegion**](ianalysisregion.md) para a área criada por sua interseção com o **IAnalysisRegion** especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRegionToIntersect* \[ no\]
</dt> <dd>

O [**IAnalysisRegion**](ianalysisregion.md) com o qual fazer a interseção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se as duas áreas não se interseccionarem, a nova área estará vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Método IAnalysisRegion:: ExcludeRegion**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Método IAnalysisRegion:: IntersectRectangle**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Método IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Método IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




