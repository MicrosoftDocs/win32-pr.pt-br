---
title: Função glRotated (Gl.h)
description: A função glRotated multiplica a matriz atual por uma matriz de rotação.
ms.assetid: 9adfeb5b-8c2a-4acf-a251-6ba23cc4c3a6
keywords:
- Função glRotated OpenGL
topic_type:
- apiref
api_name:
- glRotated
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32216eab9a7c7613f082470360d3f938bbdeaf8ae38cd875d84cd0338dfa78c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491766"
---
# <a name="glrotated-function"></a>Função glRotated

A **função glRotated** multiplica a matriz atual por uma matriz de rotação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRotated(
   GLdouble angle,
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*angle* 
</dt> <dd>

O ângulo de rotação, em graus.

</dd> <dt>

*x* 
</dt> <dd>

A *coordenada x* de um vetor.

</dd> <dt>

*y* 
</dt> <dd>

A *coordenada y* de um vetor.

</dd> <dt>

*Z* 
</dt> <dd>

A *coordenada z* de um vetor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glRotated** calcula uma matriz que executa uma  rotação no sentido anti-horário de graus angulares sobre o vetor da origem até o ponto (*x*, *y*, *z*).

A matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)) é multiplicada por essa matriz de rotação, com o produto substituindo a matriz atual. Ou seja, se M for a matriz atual e R for a matriz de tradução, M será substituído por M R.

Se o modo de matriz for GL MODELVIEW ou GL PROJECTION, todos os objetos desenhados \_ \_ depois que **glRotated** for chamado serão girados. Use [**glPushMatrix e**](glpushmatrix.md) [**glPopMatrix**](glpopmatrix.md) para salvar e restaurar o sistema de coordenadas não rotatado.

As funções a seguir recuperam informações relacionadas **a glRotated:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ RENDER \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MATRIX \_ MODE

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ MODELVIEW \_ MATRIX

[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ PROJECTION \_ MATRIX

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ TEXTURE \_ MATRIX

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

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glScale**](glscale.md)
</dt> <dt>

[**glTranslate**](gltranslate.md)
</dt> </dl>

 

 





