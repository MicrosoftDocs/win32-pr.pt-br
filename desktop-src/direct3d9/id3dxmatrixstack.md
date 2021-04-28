---
description: Interface ID3DXMATRIXStack – os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interface ID3DXMATRIXStack (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62681c468fa7e78e6fd08c458798d98b467b992e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093314"
---
# <a name="id3dxmatrixstack-interface"></a>Interface ID3DXMATRIXStack

Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.

## <a name="members"></a>Membros

A interface **ID3DXMATRIXStack** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXMATRIXStack** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXMATRIXStack** tem esses métodos.



| Método                                                                       | Descrição                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack--gettop.md)                                   | Recupera a matriz atual na parte superior da pilha.<br/>                                                                           |
| [**Loadidentity**](id3dxmatrixstack--loadidentity.md)                       | Carrega a identidade na matriz atual.<br/>                                                                                           |
| [**Loadmatrix**](id3dxmatrixstack--loadmatrix.md)                           | Carrega a matriz determinada na matriz atual.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack--multmatrix.md)                           | Determina o produto da matriz atual e a matriz especificada.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)                 | Determina o produto da matriz e da matriz atual.<br/>                                                              |
| [**Pop**](id3dxmatrixstack--pop.md)                                         | Remove a matriz atual da parte superior da pilha.<br/>                                                                           |
| [**Push**](id3dxmatrixstack--push.md)                                       | Adiciona uma matriz à pilha.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack--rotateaxis.md)                           | Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)                 | Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)           | Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md) | Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.<br/>                                             |
| [**Escala**](id3dxmatrixstack--scale.md)                                     | Dimensione a matriz atual sobre a origem da coordenada mundial.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack--scalelocal.md)                           | Dimensione a matriz atual sobre a origem do objeto.<br/>                                                                               |
| [**Traduzir**](id3dxmatrixstack--translate.md)                             | Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).<br/> |
| [**TranslateLocal**](id3dxmatrixstack--translatelocal.md)                   | Determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.<br/> |



 

## <a name="remarks"></a>Comentários

A interface **ID3DXMATRIXStack** é obtida chamando a função [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) .

O tipo LPD3DXMATRIXSTACK é definido como um ponteiro para a interface **ID3DXMATRIXStack** .


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
