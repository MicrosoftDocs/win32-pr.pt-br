---
title: Função glMultMatrixd (Gl.h)
description: A função glMultMatrixd multiplica a matriz atual por uma matriz arbitrária. | Função glMultMatrixd (Gl.h)
ms.assetid: 1f6cf4e4-e7bd-470c-b1f4-b9ccc1fb756e
keywords:
- Função glMultMatrixd OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd31b3f84bbc8c75a3622b7b87f7a7577a33927bd489a06b8691377badaf0b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358790"
---
# <a name="glmultmatrixd-function"></a>Função glMultMatrixd

As **funções glMultMatrixd** e [**glMultMatrixf**](glmultmatrixf.md) multiplicam a matriz atual por uma matriz arbitrária.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMultMatrixd(
   const GLdouble *m
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*m* 
</dt> <dd>

Um ponteiro para uma matriz 4x4 armazenada na ordem principal da coluna como 16 valores consecutivos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glMultMatrix** multiplica a matriz atual pela especificada em *m.* Ou seja, se M for a matriz atual e T for a matriz passada para **glMultMatrix,** M será substituído por M T.

A matriz atual é a matriz de projeção, matriz modelview ou matriz de textura, determinada pelo modo de matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)).

O *parâmetro m* aponta para uma matriz 4x4 de valores de ponto flutuante de precisão simples ou de precisão dupla armazenados em ordem de coluna principal. Ou seja, a matriz é armazenada conforme mostrado na imagem a seguir.

![! [Diagrama mostrando a matriz 4x4 para a que o parâmetro m aponta.]](images/multi01.png)

As funções a seguir recuperam informações relacionadas **a glMultMatrix:**

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





