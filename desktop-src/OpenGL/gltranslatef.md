---
title: Função glTranslatef (Gl.h)
description: A função glTranslatef multiplica a matriz atual por uma matriz de tradução.
ms.assetid: 2354ad52-e80f-49fc-82e7-ac6c146aa59d
keywords:
- Função glTranslatef OpenGL
topic_type:
- apiref
api_name:
- glTranslatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12975095aa78d143aaaf096e8b0141f37d45a56286e7d607a9253e59e27ba5bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489836"
---
# <a name="gltranslatef-function"></a>Função glTranslatef

A [**função glTranslatef**](gltranslate.md) multiplica a matriz atual por uma matriz de tradução.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTranslatef(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

A *coordenada x* de um vetor de tradução.

</dd> <dt>

*y* 
</dt> <dd>

A *coordenada y* de um vetor de tradução.

</dd> <dt>

*Z* 
</dt> <dd>

A *coordenada z* de um vetor de tradução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função glTranslatef** produz a tradução especificada por (*x*, *y*, *z*). O vetor de tradução é usado para calcular uma matriz de tradução 4x4:

![Diagrama mostrando a matriz de tradução 4x4 especificada por x, y, z.](images/trans01.png)

A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de tradução, com o produto substituindo a matriz atual. Ou seja, se M for a matriz atual e T for a matriz de tradução, M será substituído por M T.

Se o modo de matriz for GL MODELVIEW ou GL PROJECTION, todos os objetos desenhados depois que \_ \_ **glTranslatef** for chamado serão convertidos. Use [**glPushMatrix e**](glpushmatrix.md) **glPopMatrix** para salvar e restaurar o sistema de coordenadas nãotranslado.

As funções a seguir recuperam informações relacionadas [**a glTranslated**](gltranslate.md) e **glTranslatef**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MATRIX \_ MODE

**glGet** com o argumento GL \_ MODELVIEW \_ MATRIX

**glGet com** o argumento GL \_ PROJECTION \_ MATRIX

**glGet** com o argumento GL \_ TEXTURE \_ MATRIX

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> </dl>

 

 





