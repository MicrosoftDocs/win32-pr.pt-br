---
title: função gluQuadricTexture (Glu. h)
description: A função gluQuadricTexture especifica se quadrics deve ser texturizado.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- função gluQuadricTexture OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbde88e0a878fd59e01ad0a450cf4cbe9831c4ad867c8029373586a8efe830eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937477"
---
# <a name="gluquadrictexture-function"></a>função gluQuadricTexture

A função **gluQuadricTexture** especifica se quadrics deve ser texturizado.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quádruplo* 
</dt> <dd>

O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*textureCoords* 
</dt> <dd>

Um sinalizador que indica se as coordenadas de textura devem ser geradas. Os valores a seguir são válidos.



| Valor                                                                                                                                          | Significado                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ verdadeiro**</dt> </dl>    | Gerar coordenadas de textura.<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**GL \_ falso**</dt> </dl> | Não gere coordenadas de textura. Esse é o valor padrão.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluQuadricTexture** especifica se as coordenadas de textura devem ser geradas para quadrics renderizado com o **quadobject**.

A maneira como as coordenadas de textura são geradas depende do Quadric específico renderizado.

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

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> </dl>

 

 





