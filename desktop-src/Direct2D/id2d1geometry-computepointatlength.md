---
title: Métodos ID2D1Geometry ComputePointAtLength
description: Calcula o ponto e o vetor tangente na distância especificada ao longo da geometria \ 160;.
ms.assetid: b76aa3db-2967-4baa-a449-f664b080fb74
keywords:
- Métodos ComputePointAtLength Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5b49be0b5a17dd828c9bd86ca41b4a3ff115f47a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812859"
---
# <a name="id2d1geometrycomputepointatlength-methods"></a>Métodos ID2D1Geometry:: ComputePointAtLength

Calcula o ponto e o vetor tangente na distância especificada ao longo da geometria.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                                                                        | Descrição                                                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ 3X2 \_ F&, d2d1 \_ Point \_ 2f \* , d2d1 \_ ponto \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))              | Calcula o vetor de ponto e tangente na distância especificada ao longo da geometria depois que ele é transformado pela matriz especificada e achatado usando a tolerância padrão.<br/>   |
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ 3x2 \_ F \* , d2d1 \_ Point \_ 2f \* , d2d1 \_ ponto \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))             | Calcula o vetor de ponto e tangente na distância especificada ao longo da geometria depois que ele é transformado pela matriz especificada e achatado usando a tolerância padrão.<br/>   |
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ 3X2 \_ F&, float, d2d1 \_ Point \_ 2f \* , d2d1 \_ ponto \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))  | Calcula o vetor de ponto e tangente na distância especificada ao longo da geometria depois que ele é transformado pela matriz especificada e achatado usando a tolerância especificada.<br/> |
| [**ComputePointAtLength (FLOAT, D2D1 \_ Matrix \_ 3x2 \_ F \* , float, d2d1 \_ Point \_ 2f \* , d2d1 \_ ponto \_ 2f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f)) | Calcula o vetor de ponto e tangente na distância especificada ao longo da geometria depois que ele é transformado pela matriz especificada e achatado usando a tolerância especificada.<br/> |



## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como usar **ComputePointAtLength** para calcular o ponto e o vetor tangente na distância especificada ao longo da geometria.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;
```




```C++
// Ask the geometry to give us the point that corresponds with the
// length at the current time.
hr = m_pPathGeometry->ComputePointAtLength(
    length, 
    NULL, 
    &point, 
    &tangent); 
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

 

