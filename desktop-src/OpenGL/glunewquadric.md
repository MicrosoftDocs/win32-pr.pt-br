---
title: Função gluNewQuadric (Glu.h)
description: A função gluNewQuadric cria um objeto quadc.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- função gluNewQuadric OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66fed28c555d327bffa18d8f9100a6f5e9824b714bff1308e6b2dab20b5d3671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036266"
---
# <a name="glunewquadric-function"></a>Função gluNewQuadric

A **função gluNewQuadric** cria um objeto quadc.

## <a name="syntax"></a>Sintaxe


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="remarks"></a>Comentários

A **função gluNewQuadric** cria e retorna um ponteiro para um novo objeto quadc. Consulte este objeto ao chamar funções de renderização e controle de quadc. Um valor de retorno de zero significa que não há memória suficiente para alocar ao objeto.

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

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDeleteQuadric**](gludeletequadric.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





