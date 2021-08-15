---
title: função gluPickMatrix (Glu. h)
description: A função gluPickMatrix define uma região de separação.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- função gluPickMatrix OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 394e10c460b406e510b1423f299b4a8724492f5a5b180212ff121f4ad593041e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061574"
---
# <a name="glupickmatrix-function"></a>função gluPickMatrix

A função **gluPickMatrix** define uma região de separação.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

A coordenada x da janela de uma região de separação.

</dd> <dt>

*y* 
</dt> <dd>

A coordenada de janela y de uma região de separação.

</dd> <dt>

*altura* 
</dt> <dd>

A altura da região de separação em coordenadas da janela.

</dd> <dt>

*width* 
</dt> <dd>

A largura da região de separação em coordenadas da janela.

</dd> <dt>

*visor* 
</dt> <dd>

O visor atual (como de uma chamada [**glGetIntegerv**](glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluPickMatrix** cria uma matriz de projeção que você pode usar para restringir o desenho a uma pequena região do visor.

1.  Use **gluPickMatrix** para restringir o desenho a uma região pequena ao seu cursor.
2.  Insira o modo de seleção (com [**glRenderMode**](glrendermode.md)) e, em seguida, retorne a cena.

    Todos os primitivos que teriam sido desenhados perto do cursor são identificados e armazenados no buffer de seleção.

A matriz criada por **gluPickMatrix** é multiplicada pela matriz atual, assim como se [**glMultMatrix**](glmultmatrix.md) fosse chamado com a matriz gerada.

1.  Chame [**glLoadIdentity**](glloadidentity.md) para carregar uma matriz de identidade na pilha de matriz de perspectiva.
2.  Chame **gluPickMatrix**.
3.  Chame uma função (como [**gluPerspective**](gluperspective.md)) para multiplicar a matriz de perspectiva pela matriz de seleção.

Ao usar **gluPickMatrix** para escolher B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)), tenha cuidado para desativar a propriedade NURBS, a matriz de \_ carga automática Glu \_ \_ . Se a \_ \_ matriz de carga automática Glu não estiver desativada \_ , qualquer superfície NURBS renderizada será subdividida de forma diferente com a matriz de seleção de como ela foi subdividida sem a matriz de seleção.

## <a name="examples"></a>Exemplos

Ao renderizar uma cena da seguinte maneira:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



o código a seguir seleciona uma parte do visor:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glGetIntegerv**](glgetintegerv.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





