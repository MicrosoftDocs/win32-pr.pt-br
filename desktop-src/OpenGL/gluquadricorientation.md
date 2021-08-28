---
title: Função gluQuadricOrientation (Glu.h)
description: A função gluQuadricOrientation especifica a orientação interna ou externa para os quadcs.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- Função gluQuadricOrientation OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa02c3b6d207cbcc2bf487f51c0e96dc2f2dd98748edc81efb58ac957fac4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937622"
---
# <a name="gluquadricorientation-function"></a>Função gluQuadricOrientation

A **função gluQuadricOrientation** especifica a orientação interna ou externa para os quadcs.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quadObject* 
</dt> <dd>

O objeto quadc (criado com [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Orientação* 
</dt> <dd>

A orientação desejada. Os valores a seguir são válidos.



| Valor                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**GLU \_ OUTSIDE**</dt> </dl> | Desenhar quadrics com normais apontando para fora. Esse é o valor padrão.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**GLU \_ INSIDE**</dt> </dl>    | Desenhar quadrics com normais apontando para dentro.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluQuadricOrientation** especifica que tipo de orientação é desejado para os quadcs renderizados com **quadObject**. A interpretação de para fora e para dentro depende do quadric que está sendo desenhado.

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

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





