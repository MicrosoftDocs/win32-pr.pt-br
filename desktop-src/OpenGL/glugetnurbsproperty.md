---
title: Função gluGetNheisProperty (Glu.h)
description: A função gluGetNheisProperty obtém uma propriedade NGETS (Rational B-Spline) não uniforme.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- Função gluGetNagisProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a68e91fbdaafc2a1857a95e059125bf62347777edfbcc764868ceea0a8fce578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519586"
---
# <a name="glugetnurbsproperty-function"></a>Função gluGetNagisProperty

A **função gluGetNheisProperty** obtém uma propriedade [NGETS](using-nurbs-curves-and-surfaces.md)(Rational B-Spline) não uniforme.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto N LTDA (criado com [**gluNewNheisRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

A propriedade cujo valor deve ser recuperado. Os seguintes valores são válidos: GLU \_ SAMPLING \_ TOLERANCE, \_ GLU DISPLAY \_ MODE, GLU \_ SAMPLINGING, GLU \_ AUTO LOAD \_ \_ MATRIX, GLU \_ PARAMETRIC \_ TOLERANCE, GLU SAMPLING METHOD, GLU U \_ STEP \_ \_ \_ \_ \_ e GLU V STEP.

</dd> <dt>

*value* 
</dt> <dd>

Um ponteiro para o local no qual o valor da propriedade nomeada é gravado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluGetNagisProperty** para recuperar propriedades armazenadas em um objeto NGETS. Essas propriedades afetam a maneira como as curvas e superfícies N LTDAS são renderizadas. Para obter informações sobre as propriedades NALTERS, consulte [**gluN gluPerty**](glunurbsproperty.md).

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

[**gluNewNagisRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNagisProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





