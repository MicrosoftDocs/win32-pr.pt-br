---
description: Expande a área desta IAnalysisRegion para a área criada por sua união com o IAnalysisRegion especificado.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'Método IAnalysisRegion:: UnionRegion (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 760296552dc13ac394d4554903d84f596faba14318db9af3145c79f156c736fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720003"
---
# <a name="ianalysisregionunionregion-method"></a>Método IAnalysisRegion:: UnionRegion

Expande a área desta [**IAnalysisRegion**](ianalysisregion.md) para a área criada por sua união com o **IAnalysisRegion** especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRegionToUnion* \[ no\]
</dt> <dd>

O [**IAnalysisRegion**](ianalysisregion.md) com o qual combinar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

Se qualquer área for infinita, a nova área também será infinita.

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

[**Método IAnalysisRegion:: IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Método IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




