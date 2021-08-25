---
description: Restringe a área deste IAnalysisRegion à área criada por sua interseção com o retângulo especificado.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: Método IAnalysisRegion::IntersectRectangle (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 074e3cee4cd20a35c780ce0c644b24c7688956d85a631f3563dd678c70c82822
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935486"
---
# <a name="ianalysisregionintersectrectangle-method"></a>Método IAnalysisRegion::IntersectRectangle

Restringe a área deste [**IAnalysisRegion**](ianalysisregion.md) à área criada por sua interseção com o retângulo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pIntersectingRectangle* \[ Em\]
</dt> <dd>

Um ponteiro para o retângulo com o qual intersecção, em coordenadas de espaço em tinta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

As coordenadas do retângulo estão em unidades HIMETRIC.

Se as duas áreas não se cruzam, a nova área está vazia.

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

[**Método IAnalysisRegion::IntersectRegion**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**Método IAnalysisRegion::UnionRectangle**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**Método IAnalysisRegion::UnionRegion**](ianalysisregion-unionregion.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




