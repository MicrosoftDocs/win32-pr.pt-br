---
title: função gluGetNurbsProperty (Glu. h)
description: A função gluGetNurbsProperty Obtém uma propriedade B-spline racional não uniforme (NURBS).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- função gluGetNurbsProperty OpenGL
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
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085436"
---
# <a name="glugetnurbsproperty-function"></a>função gluGetNurbsProperty

A função **gluGetNurbsProperty** Obtém uma propriedade B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

A propriedade cujo valor deve ser recuperado. Os seguintes valores são válidos: tolerância de amostragem de GLU \_ \_ , \_ modo de exibição Glu \_ , glu \_ de remoção, matriz de \_ carga automática Glu \_ \_ , \_ tolerância paramétrica Glu \_ , \_ \_ método de amostragem glu, \_ etapa Glu U \_ e \_ etapa Glu V \_ .

</dd> <dt>

*value* 
</dt> <dd>

Um ponteiro para o local no qual o valor da propriedade nomeada é gravado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluGetNurbsProperty** para recuperar as propriedades armazenadas em um objeto NURBS. Essas propriedades afetam a maneira como as curvas NURBS e as superfícies são renderizadas. Para obter informações sobre as propriedades NURBS, consulte [**gluNurbsProperty**](glunurbsproperty.md).

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





