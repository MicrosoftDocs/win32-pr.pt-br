---
title: Função glPushMatrix (Gl.h)
description: As funções glPushMatrix e glPopMatrix e push e pop da pilha de matriz atual. | Função glPushMatrix (Gl.h)
ms.assetid: 97d8e644-50bb-4130-b6b7-d87df4468e73
keywords:
- Função glPushMatrix OpenGL
topic_type:
- apiref
api_name:
- glPushMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0d6af41bb02c82a28b667a2b5ad62d942c036c7f744a68fa9bb79188e26ae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795131"
---
# <a name="glpushmatrix-function"></a>Função glPushMatrix

As **funções glPushMatrix** e [**glPopMatrix**](glpopmatrix.md) e push e pop da pilha de matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPushMatrix(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

É um erro fazer push de uma pilha de matriz completa ou para abrir uma pilha de matriz que contém apenas uma única matriz. Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ STACK \_ OVERFLOW**</dt> </dl>    | A função foi chamada enquanto a pilha de matriz atual estava cheia.<br/>                                                           |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Há uma pilha de matrizes para cada um dos modos de matriz. No modo GL \_ MODELVIEW, a profundidade da pilha é pelo menos 32. Nos outros dois modos, GL \_ PROJECTION e GL \_ TEXTURE, a profundidade é pelo menos 2. A matriz atual em qualquer modo é a matriz na parte superior da pilha para esse modo.

A **função glPushMatrix** esmaeia a pilha de matriz atual em um, duplicando a matriz atual. Ou seja, após uma **chamada glPushMatrix,** a matriz na parte superior da pilha é idêntica à que está abaixo dela. A **função glPopMatrix** abre a pilha de matriz atual, substituindo a matriz atual pela que está abaixo dela na pilha. Inicialmente, cada uma das pilhas contém uma matriz, uma matriz de identidade.

As funções a seguir recuperam informações relacionadas **a glPushMatrix** e **glPopMatrix**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MATRIX \_ MODE

**glGet** com o argumento GL \_ MODELVIEW \_ MATRIX

**glGet com** o argumento GL \_ PROJECTION \_ MATRIX

**glGet** com o argumento GL \_ TEXTURE \_ MATRIX

**glGet com** o argumento GL \_ MODELVIEW \_ STACK \_ DEPTH

**glGet com** o argumento GL \_ PROJECTION STACK \_ \_ DEPTH

**glGet com** o argumento GL \_ TEXTURE STACK \_ \_ DEPTH

**glGet com** o argumento GL \_ MAX \_ MODELVIEW STACK \_ \_ DEPTH

**glGet com** o argumento GL \_ MAX PROJECTION STACK \_ \_ \_ DEPTH

**glGet com** o argumento GL \_ MAX TEXTURE STACK \_ \_ \_ DEPTH

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





