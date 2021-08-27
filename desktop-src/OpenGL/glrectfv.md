---
title: Função glRectfv (Gl.h)
description: A função glRectfv desenha um retângulo.
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
keywords:
- Função glRectfv OpenGL
topic_type:
- apiref
api_name:
- glRectfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e51c98bd420680892bdcdc1a7c234892afd87fb281c7f26b62771084b6a2ebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036636"
---
# <a name="glrectfv-function"></a>Função glRectfv

A [**função glRectfv**](glrectdv.md) desenha um retângulo.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRectfv(
   const GLfloat *v1,
   const GLfloat *v2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*v1* 
</dt> <dd>

Um ponteiro para um vértice de um retângulo.

</dd> <dt>

*v2* 
</dt> <dd>

um ponteiro para o vértice oposto do retângulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glRectf** dá suporte à especificação eficiente de retângulos como dois pontos de canto. Cada comando de retângulo aceita quatro argumentos, organizados como dois pares consecutivos de coordenadas (*x*, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*). O retângulo resultante é definido no *plano z* = 0.

A **função glRectf**(*x1,* *y1,* *x2,* *y2*) é exatamente equivalente à seguinte sequência:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Observe que, se o segundo vértice estiver acima e à direita do primeiro vértice, o retângulo será construído com um winding no sentido anti-horário.

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

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





