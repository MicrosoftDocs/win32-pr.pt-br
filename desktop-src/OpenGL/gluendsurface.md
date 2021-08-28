---
title: Função gluEndSurface (Glu.h)
description: As funções gluBeginSurface e gluEndSurface delimitam uma definição de superfície NRITOS (Racional B-Spline) não uniforme. | Função gluEndSurface (Glu.h)
ms.assetid: beaa0340-c67d-4376-bedd-7f73c5c6d742
keywords:
- Função gluEndSurface OpenGL
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
ms.openlocfilehash: 32c8fb5165be78032429dce7957cd0975753515d55969b04415c61be2a7dc5ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675366"
---
# <a name="gluendsurface-function"></a>Função gluEndSurface

As [**funções gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** delimitam uma definição de superfície [NALTERS](using-nurbs-curves-and-surfaces.md)(Rational B-Spline ) não uniforme.

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

O objeto N LTDA (criado com [**gluNewNheisRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

As [**funções gluBeginSurface**](glubeginsurface.md) e **gluEndSurface** marcam o início e o fim das definições de superfície NFACES, que são definidas com chamadas **para gluNfaceSurface.**

1.  Chame **gluBeginSurface** para marcar o início de uma definição de superfície NFACES.
2.  Faça uma ou mais chamadas para **gluNfaceSurface** para definir os atributos da superfície.

    Exatamente uma dessas chamadas para **gluNfaceSurface** deve ter um tipo de superfície GL \_ MAP2 \_ VERTEX 3 ou \_ GL \_ MAP2 \_ VERTEX \_ 4.

3.  Para marcar o final da definição da superfície NFACES, chame **gluEndSurface**.

As [**funções gluBeginTrim**](glubegintrim.md), [**gluPwlCurve,**](glupwlcurve.md) [**gluNagisCurve**](glunurbscurve.md)e **gluEndTrim** suportam o corte de superfícies NRECS.

Use avaliadores OpenGL para renderizar a superfície N LTDA como um conjunto de polígonos. Preservar o estado do avaliador durante a renderização [**com glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) e [**glPopAttrib.**](glpopattrib.md)

## <a name="examples"></a>Exemplos

As funções a seguir renderizarão uma superfície N LTDA texturizada com normais; as coordenadas de textura e as normais também são descritas como superfícies NALTERS:

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
| Cabeçalho<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNagisRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNagisCurve**](glunurbscurve.md)
</dt> <dt>

[**gluNagisSurface**](glunurbssurface.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





