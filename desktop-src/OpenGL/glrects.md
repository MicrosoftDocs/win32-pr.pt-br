---
title: Função glRects (Gl.h)
description: A função glRects desenha um retângulo.
ms.assetid: cf56352a-3396-4061-aa5e-dada986cf4ca
keywords:
- Função glRects OpenGL
topic_type:
- apiref
api_name:
- glRects
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e7207f46ec8bb25f22b3b620f00994bf88e929dac318abf14bd09af78cd3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937916"
---
# <a name="glrects-function"></a>Função glRects

A **função glRects** desenha um retângulo.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRects(
   GLshort x1,
   GLshort y1,
   GLshort x2,
   GLshort y2
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

A **função glRects** dá suporte à especificação eficiente de retângulos como dois pontos de canto. Cada comando de retângulo aceita quatro argumentos, organizados como dois pares consecutivos de coordenadas (x, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*). O retângulo resultante é definido no *plano z* = 0.

A **função glRects**(*x1,* *y1,* *x2,* *y2*) é exatamente equivalente à seguinte sequência:

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

 

 





