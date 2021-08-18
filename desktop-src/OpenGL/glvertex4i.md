---
title: Função glVertex4i (Gl.h)
description: Especifica um vértice. | Função glVertex4i (Gl.h)
ms.assetid: eb73c5eb-c03d-489f-b323-bb2245d9b34c
keywords:
- Função glVertex4i OpenGL
topic_type:
- apiref
api_name:
- glVertex4i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2974bfb823d71003d418a6e08a3c04b80a8bfb707e630cc1a45fc719b7abde99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035576"
---
# <a name="glvertex4i-function"></a>Função glVertex4i

Especifica um vértice.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glVertex4i(
   GLint x,
   GLint y,
   GLint z,
   GLint w
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

Especifica a coordenada x de um vértice.

</dd> <dt>

*y* 
</dt> <dd>

Especifica a coordenada y de um vértice.

</dd> <dt>

*Z* 
</dt> <dd>

Especifica a coordenada z de um vértice.

</dd> <dt>

*w* 
</dt> <dd>

Especifica a coordenada w de um vértice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md)glEnd para especificar vértices de / [](glend.md) ponto, linha e polígono. As coordenadas de cor, normal e textura atuais são associadas ao vértice quando glVertex é chamado. Quando apenas *x* e *y* são especificados, *o padrão z* é 0.0 e *w* assume como padrão 1.0. Quando *x*, *y* e *z* são especificados, *w* assume como padrão 1.0. Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glRect**](glrect-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> </dl>

 

 





