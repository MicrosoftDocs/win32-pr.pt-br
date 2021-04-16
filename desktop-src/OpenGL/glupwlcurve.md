---
title: função gluPwlCurve (Glu. h)
description: A função gluPwlCurve descreve uma curva de corte de B-spline (NURBS) não uniforme de piecewise linear.
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- função gluPwlCurve OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751089"
---
# <a name="glupwlcurve-function"></a>função gluPwlCurve

A função **gluPwlCurve** descreve uma curva de corte de B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) não uniforme de piecewise linear.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*contagem* 
</dt> <dd>

O número de pontos na curva.

</dd> <dt>

*array* 
</dt> <dd>

Uma matriz que contém os pontos de curva.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento (um número de valores de ponto flutuante de precisão simples) entre pontos na curva.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de curva. Deve ser GLU \_ MAP1 \_ Trim \_ 2 ou Glu \_ MAP1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluPwlCurve** descreve uma curva de corte linear piecewise para uma superfície NURBS. Uma curva linear piecewise consiste em uma lista de coordenadas de pontos no espaço de parâmetro para a superfície NURBS ser cortada. Esses pontos são conectados com segmentos de linha para formar uma curva. Se a curva for uma aproximação para uma curva real, os pontos deverão ser próximos o suficiente para que o caminho resultante apareça curvo na resolução usada no aplicativo.

Se *Type* for Glu \_ MAP1 \_ Trim \_ 2, ele descreve uma curva no espaço de parâmetro bidimensional (*u* e *v*). Se for GLU \_ MAP1 \_ Trim \_ 3, ele descreverá uma curva no espaço de parâmetro bidimensional homogêneo (*u*, *v* e *w*). Para obter mais informações sobre as curvas de corte, consulte [**gluBeginTrim**](glubegintrim.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





