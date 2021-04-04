---
title: função glRectiv (GL. h)
description: A função glRectiv desenha um retângulo.
ms.assetid: 24db6fc0-9b53-4e72-9b12-18ea65409f12
keywords:
- função glRectiv OpenGL
topic_type:
- apiref
api_name:
- glRectiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 668e1f253a44833ee7b1e0210327e93536bb850f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824180"
---
# <a name="glrectiv-function"></a>função glRectiv

A função **glRectiv** desenha um retângulo.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRectiv(
   const GLint *v1,
   const GLint *v2
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

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glRecti** dá suporte à especificação eficiente de retângulos como dois pontos de canto. Cada comando de retângulo usa quatro argumentos, organizados como dois pares consecutivos de coordenadas (*x*, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*). O retângulo resultante é definido no plano *z* = 0.

A função **glRecti**(*X1,* *Y1,* *X2,* *Y2*) é exatamente equivalente à seguinte sequência:

**glBegin**( \_ polígono GL);

**glVertex2**( *X1,* *Y1* );

**glVertex2**( *X2,* *Y1* );

**glVertex2**( *X2,* *Y2* );

**glVertex2**( *X1,* *Y2* );

**glEnd**();

Observe que, se o segundo vértice estiver acima e à direita do primeiro vértice, o retângulo será construído com um retrocesso anti-horário.

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

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





