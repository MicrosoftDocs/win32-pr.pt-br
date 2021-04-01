---
title: função gluNurbsSurface (Glu. h)
description: A função gluNurbsSurface define a forma de uma superfície B-spline racional não uniforme (NURBS).
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- função gluNurbsSurface OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917963"
---
# <a name="glunurbssurface-function"></a>função gluNurbsSurface

A função **gluNurbsSurface** define a forma de uma superfície B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*contagem de sknot \_* 
</dt> <dd>

O número de nós na direção de *u* paramétrica.

</dd> <dt>

*sknot* 
</dt> <dd>

Uma matriz de *\_ contagem de sknot* nondecreasing valores de nó na direção de *u* paramétrica.

</dd> <dt>

*contagem de tknot \_* 
</dt> <dd>

O número de nós na direção de paramétrica *v* .

</dd> <dt>

*tknot* 
</dt> <dd>

Uma matriz de *\_ contagem de tknot* nondecreasing valores de nó na direção de paramétrica *v* .

</dd> <dt>

*\_distância s* 
</dt> <dd>

O deslocamento (como um número de valores de ponto de precisionfloating único) entre pontos de controle sucessivos na direção de paramétrica *u* em *ctlarray*.

</dd> <dt>

*t \_ Stride* 
</dt> <dd>

O deslocamento (em valores de ponto de precisionfloating único) entre pontos de controle sucessivos na direção de paramétrica *v* em *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Uma matriz que contém pontos de controle para a superfície NURBS. Os deslocamentos entre pontos de controle sucessivos nas direções paramétrica *u* e *v* são fornecidos por *s \_ Stride* e *t \_ Stride*.

</dd> <dt>

*sorder* 
</dt> <dd>

A ordem da superfície NURBS na direção de *u* paramétrica. A ordem é mais do que o grau, portanto, uma superfície que é cúbica em *u* tem uma ordem *u* de 4.

</dd> <dt>

*torder* 
</dt> <dd>

A ordem da superfície NURBS na direção *v* paramétrica. A ordem é mais do que o grau, portanto, uma superfície que é cúbica em *v* tem uma ordem *v* de 4.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo da superfície. O parâmetro de *tipo* pode ser qualquer um dos tipos de avaliadores bidimensionais válidos (como GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ Color \_ 4).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluNurbsSurface** em uma definição de superfície NURBS para descrever a forma de uma superfície NURBS (antes de qualquer corte). Para marcar o início de uma definição de superfície NURBS, use a função [**gluBeginSurface**](glubeginsurface.md) . Para marcar o final de uma definição de superfície NURBS, use a função [**gluEndSurface**](gluendsurface.md) . Chame **gluNurbsSurface** somente dentro de uma definição de superfície NURBS.

Você associa as coordenadas posicionais, de textura e de cores a uma superfície, apresentando cada uma como um **gluNurbsSurface** separado entre um par **gluBeginSurface** / **gluEndSurface** . Em um único par **gluBeginSurface** / **gluEndSurface** , você pode fazer apenas uma chamada para **gluNurbsSurface** para cor, posição e dados de textura. Faça exatamente uma chamada para descrever a posição da superfície (um *tipo* de GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ Vertex \_ 4).

Você pode cortar uma superfície NURBS usando as funções [**gluNurbsCurve**](glunurbscurve.md) e [**gluPwlCurve**](glupwlcurve.md) entre chamadas para [**gluBeginTrim**](glubegintrim.md) e [**gluEndTrim**](gluendtrim.md).

Um **gluNurbsSurface** com os nós de *\_ contagem sknot* nos nós de *\_ contagem* *u* e tknot na direção *v* com Orders *sorder* e *torder* deve ter os pontos de controle (sknot *\_ Count*  - *sorder*) multipied por (tknot *\_ Count*  - *torder*).

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





