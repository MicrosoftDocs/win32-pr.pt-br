---
title: Função gluQuadricNormals (Glu.h)
description: A função gluQuadricNormals especifica que tipo de normal deve ser usado para os quadcs.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- Função gluQuadricNormals OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d535a90f21b88b26c3afd245b2f6350a443fd8915a4cd806df79236484c36d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554176"
---
# <a name="gluquadricnormals-function"></a>Função gluQuadricNormals

A **função gluQuadricNormals** especifica que tipo de normal deve ser usado para os quadcs.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quadObject* 
</dt> <dd>

O objeto quadc (criado com [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Normais* 
</dt> <dd>

O tipo desejado de normais. Os valores a seguir são válidos.



| Valor                                                                                                                                                | Significado                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**GLU \_ NONE**</dt> </dl>       | Nenhuma normal é gerada.<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**GLU \_ FLAT**</dt> </dl>       | Um normal é gerado para cada faceta de um quadric.<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**GLU \_ SMOOTH**</dt> </dl> | Um normal é gerado para cada vértice de um quadric. Esse é o valor padrão.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluQuadricNormals** especifica que tipo de normal deve ser usado para os quadcs renderizados com **quadObject**.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





