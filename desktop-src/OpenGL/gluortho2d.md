---
title: função gluOrtho2D (Glu. h)
description: A função gluOrtho2D define uma matriz de projeção ortográfica 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- função gluOrtho2D OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369204"
---
# <a name="gluortho2d-function"></a>função gluOrtho2D

A função **gluOrtho2D** define uma matriz de projeção ortográfica 2D.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*esquerda* 
</dt> <dd>

A coordenada para o plano de recorte vertical esquerdo.

</dd> <dt>

*direita* 
</dt> <dd>

A coordenada para o plano de recorte vertical direito.

</dd> <dt>

*início* 
</dt> <dd>

A coordenada para o plano de recorte horizontal superior.

</dd> <dt>

*parte inferior* 
</dt> <dd>

A coordenada para o plano de recorte horizontal inferior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluOrtho2D** configura uma região de exibição ortográfica bidimensional. Isso é equivalente a chamar [**glOrtho**](glortho.md) com near = 1 e far = 1.

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

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





