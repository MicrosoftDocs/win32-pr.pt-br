---
title: função glPopMatrix (GL. h)
description: As funções glPushMatrix e glPopMatrix enviam por push e pop a pilha de matriz atual. | função glPopMatrix (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- função glPopMatrix OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c0f10456c1038da46d9070689713a8237f876bec7ce7da40acf3d81d89ad15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128016"
---
# <a name="glpopmatrix-function"></a>função glPopMatrix

As funções [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** enviam por push e pop a pilha de matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

É um erro enviar por push uma pilha de matriz completa ou exibir uma pilha de matriz que contém apenas uma única matriz. Em ambos os casos, o sinalizador de erro é definido e nenhuma outra alteração é feita no estado OpenGL.

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_estouro negativo de pilha GL \_**</dt> </dl>   | A função foi chamada enquanto a pilha de matriz atual continha apenas uma única matriz.<br/>                                     |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Há uma pilha de matrizes para cada um dos modos de matriz. No \_ modo MODELVIEW GL, a profundidade da pilha é de pelo menos 32. Nos outros dois modos, \_ a projeção GL e \_ a textura GL, a profundidade é pelo menos 2. A matriz atual em qualquer modo é a matriz na parte superior da pilha para esse modo.

A função [**glPushMatrix**](glpushmatrix.md) envia por push a pilha da matriz atual por uma, duplicando a matriz atual. Ou seja, após uma chamada **glPushMatrix** , a matriz na parte superior da pilha é idêntica à seguinte. A função **glPopMatrix** exibe a pilha da matriz atual, substituindo a matriz atual pela que está abaixo dela na pilha. Inicialmente, cada uma das pilhas contém uma matriz, uma matriz de identidade.

As funções a seguir recuperam informações relacionadas a [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_

**glGet** com o argumento GL \_ MODELVIEW \_ Matrix

 \_ matriz de projeção GLGET com Argument GL \_

**glGet** com matriz de \_ textura Argument GL \_

profundidade de pilha **glGet** com Argument GL \_ MODELVIEW \_ \_

 profundidade da pilha de \_ projeção GLGET com Argument GL \_ \_

 profundidade da pilha de textura glGet com Argument GL \_ \_ \_

**glGet** com o argumento GL \_ Max \_ MODELVIEW de \_ profundidade de pilha \_

 \_ profundidade máxima da pilha de \_ projeção glGet \_ com Argument GL \_

 \_ profundidade máxima da pilha de \_ textura \_ glGet com Argument GL \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
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

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glRotate**](glrotate.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





