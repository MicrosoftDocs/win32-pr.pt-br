---
description: Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interface ID3DXMatrixStack (D3DX10. h)
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
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298777"
---
# <a name="id3dxmatrixstack-interface"></a>Interface ID3DXMatrixStack

Os aplicativos usam os métodos da interface ID3DXMATRIXStack para manipular uma pilha de matriz.

## <a name="members"></a>Membros

A interface **ID3DXMatrixStack** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXMatrixStack** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXMatrixStack** tem esses métodos.



| Método                                                                      | Descrição                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetTop**](id3dxmatrixstack-gettop.md)                                   | Recupera a matriz atual na parte superior da pilha.<br/>                                                                           |
| [**Loadidentity**](id3dxmatrixstack-loadidentity.md)                       | Carrega a identidade na matriz atual.<br/>                                                                                           |
| [**Loadmatrix**](id3dxmatrixstack-loadmatrix.md)                           | Carrega a matriz determinada na matriz atual.<br/>                                                                                 |
| [**MultMatrix**](id3dxmatrixstack-multmatrix.md)                           | Determina o produto da matriz atual e a matriz especificada.<br/>                                                              |
| [**MultMatrixLocal**](id3dxmatrixstack-multmatrixlocal.md)                 | Determina o produto da matriz e da matriz atual.<br/>                                                              |
| [**Pop**](id3dxmatrixstack-pop.md)                                         | Remove a matriz atual da parte superior da pilha.<br/>                                                                           |
| [**Push**](id3dxmatrixstack-push.md)                                       | Adiciona uma matriz à pilha.<br/>                                                                                                     |
| [**RotateAxis**](id3dxmatrixstack-rotateaxis.md)                           | Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.<br/>                                                          |
| [**RotateAxisLocal**](id3dxmatrixstack-rotateaxislocal.md)                 | Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.<br/>                                             |
| [**RotateYawPitchRoll**](id3dxmatrixstack-rotateyawpitchroll.md)           | Gira (em relação ao espaço de coordenadas mundiais) em um eixo arbitrário.<br/>                                                          |
| [**RotateYawPitchRollLocal**](id3dxmatrixstack-rotateyawpitchrolllocal.md) | Gira (em relação ao espaço de coordenadas local do objeto) em um eixo arbitrário.<br/>                                             |
| [**Escalonáve**](id3dxmatrixstack-scale.md)                                     | Dimensione a matriz atual sobre a origem da coordenada mundial.<br/>                                                                     |
| [**ScaleLocal**](id3dxmatrixstack-scalelocal.md)                           | Dimensione a matriz atual sobre a origem do objeto.<br/>                                                                               |
| [**Traduzir**](id3dxmatrixstack-translate.md)                             | Determina o produto da matriz atual e a matriz de conversão computada determinada pelos fatores especificados (x, y e z).<br/> |
| [**TranslateLocal**](id3dxmatrixstack-translatelocal.md)                   | Determina o produto da matriz de conversão computada determinada pelos fatores especificados (x, y e z) e a matriz atual.<br/> |



 

## <a name="remarks"></a>Comentários

A interface ID3DX10MATRIXStack é obtida chamando a função [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .

O tipo LPD3DX10MATRIXSTACK é definido como um ponteiro para a interface **ID3DXMatrixStack** .


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
