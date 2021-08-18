---
title: função glRectd (GL. h)
description: A função glRectd desenha um retângulo.
ms.assetid: d5574c22-7ae1-4040-9b95-769693fa41e3
keywords:
- função glRectd OpenGL
topic_type:
- apiref
api_name:
- glRectd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 961b5b9ddf478475806d391d6499eed01fd43e14781f57dcd82e9ff6a1a55a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492166"
---
# <a name="glrectd-function"></a>função glRectd

A função **glRectd** desenha um retângulo.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRectd(
   GLdouble x1,
   GLdouble y1,
   GLdouble x2,
   GLdouble y2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*X1* 
</dt> <dd>

A coordenada *x* do vértice de um retângulo.

</dd> <dt>

*y1* 
</dt> <dd>

A coordenada *y* do vértice de um retângulo.

</dd> <dt>

*X2* 
</dt> <dd>

A coordenada *x* do vértice oposto do retângulo.

</dd> <dt>

*Y2* 
</dt> <dd>

A coordenada *y* do vértice oposto do retângulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glRectd** dá suporte à especificação eficiente de retângulos como dois pontos de canto. Cada comando de retângulo usa quatro argumentos, organizados como dois pares consecutivos de coordenadas (*x*, *y*) ou como dois ponteiros para matrizes, cada um contendo um par (*x*, *y*). O retângulo resultante é definido no plano *z* = 0.

A função **glRectd**(*X1,* *Y1,* *X2,* *Y2*) é exatamente equivalente à seguinte sequência:

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

 

 





