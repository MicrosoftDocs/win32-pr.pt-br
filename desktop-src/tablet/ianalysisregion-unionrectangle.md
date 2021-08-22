---
description: Expande a área deste IAnalysisRegion para a área criada por sua união com o retângulo especificado.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: Método IAnalysisRegion::UnionRectangle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da3eefb3a527646ba416d62783421d6dfe9be5706c0527df7eb321d3945b6f92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596746"
---
# <a name="ianalysisregionunionrectangle-method"></a>Método IAnalysisRegion::UnionRectangle

Expande a área deste [**IAnalysisRegion**](ianalysisregion.md) para a área criada por sua união com o retângulo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRectangle* \[ Em\]
</dt> <dd>

Um ponteiro para o retângulo com o qual combinar, em coordenadas de espaço em tinta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

As coordenadas do retângulo estão em unidades HIMETRIC.

Se uma das áreas for infinita, a nova área também será infinita.

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

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**Método IAnalysisRegion::ExcludeRegion**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**Método IAnalysisRegion::IntersectRectangle**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**Método IAnalysisRegion::IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Método IAnalysisRegion::UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




