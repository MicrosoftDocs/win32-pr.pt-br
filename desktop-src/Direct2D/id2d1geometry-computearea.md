---
title: Métodos ID2D1Geometry ComputeArea
description: Computa a área da geometria.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Métodos ComputeArea Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f6b79e8434a2174bcb05659f6656a46cc2d43cbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754278"
---
# <a name="id2d1geometrycomputearea-methods"></a>Métodos ID2D1Geometry:: ComputeArea

Computa a área da geometria.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                      | Descrição                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputeArea ( \_ matriz d2d1 \_ 3X2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | Computa a área da geometria após ela ter sido transformada pela matriz especificada e mesclada usando a tolerância padrão.<br/>    |
| [**ComputeArea ( \_ matriz d2d1 \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | Computa a área da geometria após ela ter sido transformada pela matriz especificada e mesclada usando a tolerância padrão.<br/> |
| [**ComputeArea ( \_ matriz d2d1 \_ 3X2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | Computa a área da geometria após ela ter sido transformada pela matriz especificada e mesclada usando a tolerância especificada.<br/>  |
| [**ComputeArea ( \_ matriz d2d1 \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | Computa a área da geometria após ela ter sido transformada pela matriz especificada e mesclada usando a tolerância especificada.<br/>  |



## <a name="examples"></a>Exemplos

O exemplo de código a seguir usa **ComputeArea** para calcular a área de um círculo especificado (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

