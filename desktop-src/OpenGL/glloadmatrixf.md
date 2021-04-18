---
title: função glLoadMatrixf (GL. h)
description: A função glLoadMatrixf substitui a matriz atual por uma matriz arbitrária. | função glLoadMatrixf (GL. h)
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- função glLoadMatrixf OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0c54f4f7f7255b2dde724cf018d57fab6cf3e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105753154"
---
# <a name="glloadmatrixf-function"></a>função glLoadMatrixf

As funções [**glLoadMatrixd**](glloadmatrixd.md) e **glLoadMatrixf** substituem a matriz atual por uma matriz arbitrária.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
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

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glLoadMatrix** substitui a matriz atual por aquela especificada em *m*. A matriz atual é a matriz de projeção, a matriz modelview ou a matriz de textura, determinada pelo modo de matriz atual (consulte [**glMatrixMode**](glmatrixmode.md)).

O parâmetro *m* aponta para uma matriz 4x4 de valores de ponto flutuante de precisão simples ou de precisão dupla armazenados em ordem de coluna principal. Ou seja, a matriz é armazenada conforme mostrado na imagem a seguir.

![Diagrama que mostra a matriz 4x4 à qual o parâmetro m aponta.](images/load02.png)

As funções a seguir recuperam informações relacionadas ao **glLoadMatrix**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_

**glGet** com o argumento GL \_ MODELVIEW \_ Matrix

 \_ matriz de projeção GLGET com Argument GL \_

**glGet** com matriz de \_ textura Argument GL \_

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

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





