---
title: Função gluNheisCurve (Glu.h)
description: A função gluN shapesCurve define a forma de uma curva N LTDS (Racional B-Spline) não uniforme.
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- Função gluNagisCurve OpenGL
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
ms.openlocfilehash: 6d5973ce3cb4d1ac05ea353fd78359f6b3b1bc9a3a0ab3180807b0834cc4bb20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489036"
---
# <a name="glunurbscurve-function"></a>Função gluNagisCurve

A **função gluN shapesCurve** define a forma de uma curva [N LTDS](using-nurbs-curves-and-surfaces.md)(Não Uniforme Racional B-Spline).

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

O objeto N LTDA (criado com [**gluNewNheisRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*nknots* 
</dt> <dd>

O número de insomos *no meio de*. O *parâmetro nknots* é igual ao número de pontos de controle mais a ordem.

</dd> <dt>

*Nó* 
</dt> <dd>

Uma matriz de *valores nknots* nãondecreasing de aninhamento.

</dd> <dt>

*Passo* 
</dt> <dd>

O deslocamento (como um número de valores de ponto flutuante de precisão simples) entre pontos de controle de curva sucessivos.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Um ponteiro para uma matriz de pontos de controle. As coordenadas devem concordar com o *tipo*.

</dd> <dt>

*order* 
</dt> <dd>

A ordem da curva N LTDA. O *parâmetro order* é igual a degree + 1; portanto, uma curva cúbica tem uma ordem de 4.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo da curva. Se essa curva for definida dentro de um par [**gluBeginCurve**](glubegincurve.md)gluEndCurve, o tipo poderá ser qualquer um dos tipos de avaliador unidimensionais válidos / [](gluendcurve.md) (como GL \_ MAP1 \_ VERTEX 3 ou \_ GL \_ MAP1 COLOR \_ \_ 4). Entre um [**par gluBeginTrim**](glubegintrim.md)gluEndTrim, os únicos tipos válidos são / [](gluendtrim.md) GLU \_ MAP1 TRIM \_ \_ 2 e GLU \_ MAP1 TRIM \_ \_ 3.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Quando **gluNinasCurve** aparece entre um **par gluBeginCurve** / **gluEndCurve,** ele descreve uma curva a ser renderizada. Você associa coordenadas posicionais, de textura e de cor apresentando cada uma delas como um **gluN gluCurve** separado entre um **par gluBeginCurve** / **gluEndCurve.** Não faça mais de uma chamada para **gluNviesCurve para dados** de cor, posição e textura em um único par **gluBeginCurve** / **gluEndCurve.** Faça exatamente uma chamada para descrever *a* posição da curva (um tipo de GL \_ MAP1 \_ VERTEX 3 ou \_ GL \_ MAP1 \_ VERTEX \_ 4).

Quando **gluNinasCurve** aparece entre um par [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim,**](gluendtrim.md) ele descreve uma curva de corte em uma superfície NALTERS. Se *o* tipo for GLU MAP1 TRIM 2, ele descreverá uma curva no espaço de parâmetro \_ \_ \_ bidimensional (*u* e *v).* Se for GLU MAP1 TRIM 3, ele descreverá uma curva no espaço de parâmetro homogêneo \_ \_ \_ bidimensional (*u,* *v* e *w).* Para obter mais discussão sobre curvas de corte, consulte **gluBeginTrim**.

## <a name="examples"></a>Exemplos

As funções a seguir renderizarão uma curva NALTERS texturizada com normais:

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
| Cabeçalho<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

[**gluNewNagisRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





