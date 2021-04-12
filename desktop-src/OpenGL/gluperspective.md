---
title: função gluPerspective (Glu. h)
description: A função gluPerspective configura uma matriz de projeção em perspectiva.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- função gluPerspective OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369813"
---
# <a name="gluperspective-function"></a>função gluPerspective

A função **gluPerspective** configura uma matriz de projeção em perspectiva.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fovy* 
</dt> <dd>

O campo de ângulo de exibição, em graus, na direção y.

</dd> <dt>

*aspect* 
</dt> <dd>

A taxa de proporção que determina o campo de exibição na direção x. A taxa de proporção é a proporção entre *x* (largura) e *y* (altura).

</dd> <dt>

*zNear* 
</dt> <dd>

A distância do visualizador para o plano de recorte próximo (sempre positivo).

</dd> <dt>

*zFar* 
</dt> <dd>

A distância do visualizador até o plano de recorte distante (sempre positivo).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluPerspective** especifica um frustum de exibição no sistema de coordenadas mundiais. Em geral, a taxa de proporção em **gluPerspective** deve corresponder à taxa de proporção do visor associado. Por exemplo, *Aspect* = 2,0 significa que o ângulo de exibição do visualizador é duas vezes mais largo em *x* , como em *y*. Se o visor for duas vezes maior que o comprimento, ele exibirá a imagem sem distorção.

A matriz gerada por **gluPerspective** é multiplicada pela matriz atual, assim como se [**glMultMatrix**](glmultmatrix.md) fosse chamado com a matriz gerada. Para carregar a matriz de perspectiva na pilha da matriz atual, preceda a chamada para **gluPerspective** com uma chamada para [**glLoadIdentity**](glloadidentity.md).

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**gluOrtho2D**](gluortho2d.md)
</dt> </dl>

 

 





