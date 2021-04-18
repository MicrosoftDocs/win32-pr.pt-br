---
title: função gluEndSurface (Glu. h)
description: As funções gluBeginSurface e gluEndSurface delimitam uma definição de superfície de B-spline racional não uniforme (NURBS). | função gluEndSurface (Glu. h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- função gluEndSurface OpenGL
topic_type:
- apiref
api_name:
- gluEndSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54631d5c4ef752cffd989f8fa02f8cb512c67da3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506416"
---
# <a name="gluendsurface-function"></a>função gluEndSurface

As funções [**gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** delimitam uma definição de superfície de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluEndSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

As funções [**gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** marcam o início e o fim das definições de superfície NURBS, que são definidas com chamadas para **gluNurbsSurface**.

1.  Chame **gluBeginSurface** para marcar o início de uma definição de superfície NURBS.
2.  Faça uma ou mais chamadas para **gluNurbsSurface** para definir os atributos da superfície.

    Exatamente uma dessas chamadas para **gluNurbsSurface** deve ter um tipo de superfície de GL \_ map2 \_ Vertex \_ 3 ou GL \_ map2 \_ vértice \_ 4.

3.  Para marcar o final da definição da superfície NURBS, chame **gluEndSurface**.

As funções [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)e **GLUENDTRIM** dão suporte à remoção de superfícies NURBS.

Use avaliadores OpenGL para renderizar a superfície NURBS como um conjunto de polígonos. Preserve o estado do avaliador durante a renderização com [**glPushAttrib**](glpushattrib.md) ( \_ bit de avaliação GL \_ ) e [**glPopAttrib**](glpopattrib.md).

## <a name="examples"></a>Exemplos

As funções a seguir renderizam uma superfície NURBS texturizada com Normals; as coordenadas de textura e normais também são descritas como superfícies NURBS:

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

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
</dt> <dt>

[**gluNurbsSurface**](glunurbssurface.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





