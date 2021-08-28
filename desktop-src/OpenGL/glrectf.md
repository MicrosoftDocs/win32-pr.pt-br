---
title: Função glRectf (Gl.h)
description: A função glRectf desenha um retângulo.
ms.assetid: 3fb55382-6041-4d9a-83cb-09a5170cc95a
keywords:
- Função glRectf OpenGL
topic_type:
- apiref
api_name:
- glRectf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3323979ba2cd5c76c96ac8eb8f85d93e90f90c4b231cdf15b9a18ca363219ae6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492056"
---
# <a name="glrectf-function"></a>Função glRectf

A [**função glRectf**](glrectd.md) desenha um retângulo.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRectf(
   GLfloat x1,
   GLfloat y1,
   GLfloat x2,
   GLfloat y2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x1* 
</dt> <dd>

A *coordenada x* do vértice de um retângulo.

</dd> <dt>

*y1* 
</dt> <dd>

A *coordenada y* do vértice de um retângulo.

</dd> <dt>

*x2* 
</dt> <dd>

A *coordenada x* do vértice oposto do retângulo.

</dd> <dt>

*y2* 
</dt> <dd>

A *coordenada y* do vértice oposto do retângulo.

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

 

 





