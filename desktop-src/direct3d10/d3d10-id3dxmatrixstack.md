---
description: Interface ID3DXMatrixStack – os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matrizes.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interface ID3DXMatrixStack (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 14ad3a6212e5bebe2df988d2cecd305aa3141a674f83075935b3c411f6c9b329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914502"
---
# <a name="id3dxmatrixstack-interface"></a>Interface ID3DXMatrixStack

Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matrizes.

## <a name="members"></a>Membros

A interface **ID3DXMatrixStack** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXMatrixStack** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXMatrixStack** tem esses métodos.



| Método                                                                      | Descrição                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack-gettop.md)                                   | Recupera a matriz atual na parte superior da pilha.<br/>                                                                           |
| [**LoadIdentity**](id3dxmatrixstack-loadidentity.md)                       | Carrega a identidade na matriz atual.<br/>                                                                                           |
| [**LoadMatrix**](id3dxmatrixstack-loadmatrix.md)                           | Carrega a matriz determinada na matriz atual.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack-multmatrix.md)                           | Determina o produto da matriz atual e a matriz determinada.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack-multmatrixlocal.md)                 | Determina o produto da matriz determinada e a matriz atual.<br/>                                                              |
| [**Pop**](id3dxmatrixstack-pop.md)                                         | Remove a matriz atual da parte superior da pilha.<br/>                                                                           |
| [**Empurrar**](id3dxmatrixstack-push.md)                                       | Adiciona uma matriz à pilha.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack-rotateaxis.md)                           | Gira (em relação ao espaço de coordenadas do mundo) em torno de um eixo arbitrário.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack-rotateaxislocal.md)                 | Gira (em relação ao espaço de coordenadas local do objeto) em torno de um eixo arbitrário.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack-rotateyawpitchroll.md)           | Gira (em relação ao espaço de coordenadas do mundo) em torno de um eixo arbitrário.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack-rotateyawpitchrolllocal.md) | Gira (em relação ao espaço de coordenadas local do objeto) em torno de um eixo arbitrário.<br/>                                             |
| [**Escala**](id3dxmatrixstack-scale.md)                                     | Dimensione a matriz atual sobre a origem da coordenada do mundo.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack-scalelocal.md)                           | Dimensione a matriz atual sobre a origem do objeto.<br/>                                                                               |
| [**Traduzir**](id3dxmatrixstack-translate.md)                             | Determina o produto da matriz atual e a matriz de tradução computada determinada pelos fatores determinados (x, y e z).<br/> |
| [**TranslateLocal**](id3dxmatrixstack-translatelocal.md)                   | Determina o produto da matriz de tradução computada determinada pelos fatores determinados (x, y e z) e a matriz atual.<br/> |



 

## <a name="remarks"></a>Comentários

A interface ID3DX10MATRIXStack é obtida chamando a [**função D3DXCreateMatrixStack.**](d3d10-d3dxcreatematrixstack.md)

O tipo LPD3DX10MATRIXSTACK é definido como um ponteiro para a interface **ID3DXMatrixStack.**


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
