---
description: Restringe a área do IAnalysisRegion à parte de sua área que não faz a interseção do retângulo especificado.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'Método IAnalysisRegion:: ExcludeRectangle (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780432"
---
# <a name="ianalysisregionexcluderectangle-method"></a>Método IAnalysisRegion:: ExcludeRectangle

Restringe a área do [**IAnalysisRegion**](ianalysisregion.md) à parte de sua área que não faz a interseção do retângulo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pExcludingRectangle* \[ no\]
</dt> <dd>

O retângulo a ser excluído deste [**IAnalysisRegion**](ianalysisregion.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

As coordenadas de retângulo estão em unidades HIMETRIC.

Se as duas áreas não se interseccionarem, o [**IAnalysisRegion**](ianalysisregion.md) não será alterado.

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

[**Método IAnalysisRegion:: ExcludeRegion**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Método IAnalysisRegion:: IntersectRectangle**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Método IAnalysisRegion:: IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Método IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Método IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




