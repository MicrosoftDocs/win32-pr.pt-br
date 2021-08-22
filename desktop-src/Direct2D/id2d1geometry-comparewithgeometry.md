---
title: Métodos ID2D1Geometry CompareWithGeometry
description: Descreve a interseção entre essa geometria e a geometria especificada.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- Métodos CompareWithGeometry Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09978c38c3e4be7ad8a86ccfccb43387ed4ac48232e39e1ed19001d806362c88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304796"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>Métodos ID2D1Geometry::CompareWithGeometry

Descreve a interseção entre essa geometria e a geometria especificada.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                            | Descrição                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry(ID2D1Geometry, \* D2D1 \_ MATRIX \_ 3X2 \_ F&,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento padrão.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry, \* D2D1 \_ MATRIX \_ 3X2 \_ F , \* D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento padrão.<br/>      |
| [**CompareWithGeometry(ID2D1Geometry, \* D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,D2D1 \_ GEOMETRY RELATION \_ \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento especificada.<br/>    |
| [**CompareWithGeometry(ID2D1Geometry, \* D2D1 \_ MATRIX \_ 3X2 \_ \* F, FLOAT,D2D1 \_ GEOMETRY \_ RELATION \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento especificada.<br/> |



## <a name="remarks"></a>Comentários

Ao interpretar o  valor de relação retornado, é importante lembrar que o membro [**D2D1 \_ GEOMETRY \_ RELATION \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) ESTÁ CONTIDO do tipo de enumeração **D2D1 \_ GEOMETRY \_ RELATION** significa que essa geometria está contida dentro de *inputGeometry*, não que essa geometria contenha *inputGeometry*.

Para obter mais informações sobre como interpretar outros valores de retorno possíveis, [**consulte D2D1 \_ GEOMETRY \_ RELATION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

