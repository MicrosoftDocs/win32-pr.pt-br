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
ms.openlocfilehash: eee64e51d4717a9fe0983be849c78f99602cac9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771680"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>Métodos ID2D1Geometry:: CompareWithGeometry

Descreve a interseção entre essa geometria e a geometria especificada.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                            | Descrição                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F&, d2d1 \_ Geometry \_ relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento padrão.<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F \* , d2d1 \_ Geometry \_ relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento padrão.<br/>      |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F&, float, d2d1 \_ Geometry \_ relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento especificada.<br/>    |
| [**CompareWithGeometry (ID2D1Geometry \* , d2d1 \_ Matrix \_ 3x2 \_ F \* , float, d2d1 \_ Geometry \_ relation \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Descreve a interseção entre essa geometria e a geometria especificada. A comparação é executada usando a tolerância de nivelamento especificada.<br/> |



## <a name="remarks"></a>Comentários

Ao interpretar o valor de *relação* retornado, é importante lembrar que a relação de geometria de d2d1 de membro [**\_ \_ \_ está \_ contida**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) no tipo de enumeração de **\_ \_ relação de geometria de d2d1** significa que essa geometria está contida em *inputGeometry*, não que essa geometria contém *inputGeometry*.

Para obter mais informações sobre como interpretar outros valores de retorno possíveis, consulte [**d2d1 \_ Geometry \_ relation**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

