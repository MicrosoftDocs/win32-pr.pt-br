---
title: Função gluNfaceSurface (Glu.h)
description: A função gluNfacesurface define a forma de uma superfície N GLUS (Racional B-Spline) não uniforme.
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- Função gluNfaceSurface OpenGL
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
ms.openlocfilehash: 50f56232ac891cbdfba18195741d875ecc5436112772ed4fa665903374e96602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554186"
---
# <a name="glunurbssurface-function"></a>Função gluNagisSurface

A **função gluNface define** a forma de uma superfície N [LTDS](using-nurbs-curves-and-surfaces.md)(Não Uniforme Racional B-Spline).

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

O objeto N LTDA (criado com [**gluNewNheisRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*sknot \_ count* 
</dt> <dd>

O número de reações na direção do *u* paramétrico.

</dd> <dt>

*sknot* 
</dt> <dd>

Uma matriz de valores de valores indesequente de contagem de *sknot \_* na direção do *u* paramétrico.

</dd> <dt>

*tknot \_ count* 
</dt> <dd>

O número de reações na direção v *paramétrica.*

</dd> <dt>

*tknot* 
</dt> <dd>

Uma matriz de *tknot count nãondecreasing \_* values in the parametric *v* direction.

</dd> <dt>

*s \_ stride* 
</dt> <dd>

O deslocamento (como um número de valores de ponto de precisão único) entre pontos de controle sucessivos na direção *u* paramétrica em *ctlarray*.

</dd> <dt>

*t \_ stride* 
</dt> <dd>

O deslocamento (em valores de ponto de precisão simples) entre pontos de controle sucessivos na direção *v* paramétrica em *ctlarray*.

</dd> <dt>

*ctlarray* 
</dt> <dd>

Uma matriz que contém pontos de controle para a superfície NALTERS. Os deslocamentos entre pontos de controle sucessivos nas direções *paramétricas u* e *v* são determinados *por \_ estridente* *e t \_ stride.*

</dd> <dt>

*sorder* 
</dt> <dd>

A ordem da superfície N LTDA na direção *do u paramétrico.* A ordem é um a mais do que o grau, portanto, uma superfície cúbica *em u* tem uma *ordem u* de 4.

</dd> <dt>

*torder* 
</dt> <dd>

A ordem da superfície N LTDA na direção *v* paramétrica. A ordem é um a mais do que o grau, portanto, uma superfície que é cúbica em *v* tem uma *ordem v* de 4.

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo da superfície. O *parâmetro* type pode ser qualquer um dos tipos de avaliador bidimensionais válidos (como GL \_ MAP2 \_ VERTEX \_ 3 ou GL \_ MAP2 COLOR \_ \_ 4).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluN ltda em uma** definição de superfície NFACES para descrever a forma de uma superfície NFACES (antes de qualquer corte). Para marcar o início de uma definição de superfície NFACES, use a [**função gluBeginSurface.**](glubeginsurface.md) Para marcar o final de uma definição de superfície NFACES, use a [**função gluEndSurface.**](gluendsurface.md) Chame **gluNfaceSurface somente em** uma definição de superfície NFACES.

Você associa coordenadas posicionais, de textura e de cores a uma superfície apresentando cada uma delas como um **gluNface separado** entre um par **gluBeginSurface** / **gluEndSurface.** Dentro de um único **par gluBeginSurface** gluEndSurface, você pode fazer apenas uma chamada a /  **gluNagisSurface** para dados de cor, posição e textura. Faça exatamente uma chamada para descrever *a* posição da superfície (um tipo de GL \_ MAP2 \_ VERTEX 3 ou \_ GL \_ MAP2 \_ VERTEX \_ 4).

Você pode cortar uma superfície NRANDOS usando as funções [**gluNrecidasCurve**](glunurbscurve.md) e [**gluPwlCurve**](glupwlcurve.md) entre chamadas [**para gluBeginTrim**](glubegintrim.md) e [**gluEndTrim**](gluendtrim.md).

Um **gluNilasSurface** com *sknot \_* count  nos pontos de controle (  tknot  count torder ) deve ter (*sknot \_ count* *\_*   - *sorder*) multipied by (*tknot \_ count*  - *torder*).

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNagisRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNagisCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





