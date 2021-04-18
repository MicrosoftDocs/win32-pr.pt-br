---
title: função gluNurbsCurve (Glu. h)
description: A função gluNurbsCurve define a forma de uma curva de B-spline racional não uniforme (NURBS).
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- função gluNurbsCurve OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758580"
---
# <a name="glunurbscurve-function"></a>função gluNurbsCurve

A função **gluNurbsCurve** define a forma de uma curva de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nknots* 
</dt> <dd>

O número de nós no *nó*. O parâmetro *nknots* é igual ao número de pontos de controle mais o pedido.

</dd> <dt>

*crescente* 
</dt> <dd>

Uma matriz de valores de nó *nknots* nondecreasing.

</dd> <dt>

*Stride* 
</dt> <dd>

O deslocamento (como um número de valores de ponto flutuante de precisão simples) entre pontos de controle de curva sucessivos.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Um ponteiro para uma matriz de pontos de controle. As coordenadas devem concordar com o *tipo*.

</dd> <dt>

*order* 
</dt> <dd>

A ordem da curva NURBS. O parâmetro *Order* é igual a grau + 1; Portanto, uma curva cúbica tem uma ordem de 4.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo da curva. Se essa curva for definida em um par [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , o tipo poderá ser qualquer um dos tipos de avaliadores unidimensionais válidos (como GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Color \_ 4). Entre um par [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , os únicos tipos válidos são Glu \_ MAP1 \_ Trim \_ 2 e Glu \_ MAP1 \_ Trim \_ 3.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Quando **gluNurbsCurve** aparece entre um  / par de **gluEndCurve** gluBeginCurve, ele descreve uma curva a ser renderizada. Você associa as coordenadas posicionais, de textura e de cores, apresentando cada uma delas como um **gluNurbsCurve** separado entre um par **gluBeginCurve** / **gluEndCurve** . Não faça mais de uma chamada para **gluNurbsCurve** para cor, posição e dados de textura em um único par **gluBeginCurve** / **gluEndCurve** . Faça exatamente uma chamada para descrever a posição da curva (um *tipo* de GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Vertex \_ 4).

Quando **gluNurbsCurve** aparece entre um [](glubegintrim.md) / par de [**gluEndTrim**](gluendtrim.md) gluBeginTrim, ele descreve uma curva de corte em uma superfície NURBS. Se *Type* for Glu \_ MAP1 \_ Trim \_ 2, ele descreve uma curva no espaço de parâmetro bidimensional (*u* e *v*). Se for GLU \_ MAP1 \_ Trim \_ 3, ele descreve uma curva no espaço de parâmetro bidimensional homogêneo (*u*, *v* e *w*). Para obter mais discussões sobre corte de curvas, consulte **gluBeginTrim**.

## <a name="examples"></a>Exemplos

As funções a seguir renderizam uma curva NURBS texturizada com Normals:

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
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

[**gluEndCurve**](gluendcurve.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





