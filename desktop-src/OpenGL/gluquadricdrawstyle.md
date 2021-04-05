---
title: função gluQuadricDrawStyle (Glu. h)
description: A função gluQuadricDrawStyle especifica o estilo de desenho desejado para quadrics.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- função gluQuadricDrawStyle OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918830"
---
# <a name="gluquadricdrawstyle-function"></a>função gluQuadricDrawStyle

A função **gluQuadricDrawStyle** especifica o estilo de desenho desejado para quadrics.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quádruplo* 
</dt> <dd>

O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*desenharstyle* 
</dt> <dd>

O estilo de desenho desejado. Os valores a seguir são válidos.



| Valor                                                                                                                                                            | Significado                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**preenchimento de GLU \_**</dt> </dl>                   | Quadrics são renderizados com primitivas de polígono. Os polígonos são desenhados em um sentido anti-horário com relação aos seus normais (conforme definido com [**gluQuadricOrientation**](gluquadricorientation.md)).<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**GLU \_ linha**</dt> </dl>                   | Quadrics são renderizados como um conjunto de linhas.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**silhueta de GLU \_**</dt> </dl> | Quadrics são renderizados como um conjunto de linhas, exceto que as bordas que separam rostos de coplanar não serão desenhadas.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**ponto de GLU \_**</dt> </dl>                | Quadrics são renderizados como um conjunto de pontos.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluQuadricDrawStyle** especifica o estilo de desenho para quadrics renderizado com o **quadobject**.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





