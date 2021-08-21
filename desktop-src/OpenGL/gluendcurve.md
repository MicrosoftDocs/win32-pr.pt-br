---
title: função gluEndCurve (Glu. h)
description: As funções gluBeginCurve e gluEndCurve delimitam uma definição de curva de B-spline racional não uniforme (NURBS). | função gluEndCurve (Glu. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- função gluEndCurve OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b6d8e9871b03286eebc285d2c3ad8834c8c354b196213c985626fc80cd02fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489516"
---
# <a name="gluendcurve-function"></a>função gluEndCurve

As funções [**gluBeginCurve**](glubegincurve.md) e **gluEndCurve** delimitam uma definição de curva de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluEndCurve(
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

Use [**gluBeginCurve**](glubegincurve.md) para marcar o início de uma definição de curva NURBS. Depois de chamar **gluBeginCurve**, faça uma ou mais chamadas para [**gluNurbsCurve**](glunurbscurve.md) para definir os atributos da curva. Exatamente uma das chamadas para **gluNurbsCurve** deve ter um tipo de curva GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Vertex \_ 4. Para marcar o final da definição de curva NURBS, chame **gluEndCurve**.

Os avaliadores OpenGL são usados para renderizar a curva NURBS como uma série de segmentos de linha. O estado do avaliador é preservado durante a renderização com [**glPushAttrib**](glpushattrib.md) ( \_ bit de avaliação GL \_ ) e [**glPopAttrib**](glpopattrib.md). Para obter informações sobre exatamente que Estado Essas chamadas preservam, consulte **glPushAttrib**.

## <a name="examples"></a>Exemplos

As funções a seguir renderizam uma curva NURBS texturizada com Normals; as coordenadas de textura e normais também são especificadas como curvas NURBS:

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
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

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





