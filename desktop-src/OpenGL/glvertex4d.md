---
title: função glVertex4d (GL. h)
description: Especifica um vértice. | função glVertex4d (GL. h)
ms.assetid: d9203e4f-5ed2-41e7-b619-65cee3132ed9
keywords:
- função glVertex4d OpenGL
topic_type:
- apiref
api_name:
- glVertex4d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a28a64c35ff30cc668839899dca4f3dc2958ff9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105770270"
---
# <a name="glvertex4d-function"></a>função glVertex4d

Especifica um vértice.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glVertex4d(
   GLdouble x,
   GLdouble y,
   GLdouble z,
   GLdouble w
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

*z* 
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

Os comandos de função glVertex são usados em pares [**glBegin**](glbegin.md) / [**glEnd**](glend.md) para especificar vértices de ponto, linha e polígono. As coordenadas de cor atual, normal e de textura são associadas ao vértice quando glVertex é chamado. Quando apenas *x* e *y* são especificados, *z* usa como padrão 0,0 e *w* é o padrão de 1,0. Quando *x*, *y* e *z* são especificados, *w* assume o padrão de 1,0. Invocar glVertex fora de um par **glBegin** / **glEnd** resulta em um comportamento indefinido.

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

 

 





