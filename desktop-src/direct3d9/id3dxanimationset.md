---
description: Essa interface encapsula a funcionalidade mínima necessária de uma animação definida por um controlador de animação.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interface ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173185"
---
# <a name="id3dxanimationset-interface"></a>Interface ID3DXAnimationSet

Essa interface encapsula a funcionalidade mínima necessária de uma animação definida por um controlador de animação. Os usuários avançados podem querer implementar essa interface para atender às suas necessidades especializadas; no entanto, para a maioria dos usuários, as interfaces [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) e [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) derivadas devem ser suficientes.

## <a name="members"></a>Membros

A interface **ID3DXAnimationSet** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationSet** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXAnimationSet** tem esses métodos.



| Método                                                                        | Descrição                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetAnimationIndexByName**](id3dxanimationset--getanimationindexbyname.md) | Obtém o índice de uma animação, dado seu nome.<br/>                        |
| [**GetAnimationNameByIndex**](id3dxanimationset--getanimationnamebyindex.md) | Obtém o nome de uma animação, dado seu índice.<br/>                        |
| [**Getcallback**](id3dxanimationset--getcallback.md)                         | Obtém informações sobre um retorno de chamada específico no conjunto de animações.<br/>       |
| [**GetName**](id3dxanimationset--getname.md)                                 | Obtém o nome do conjunto de animações.<br/>                                           |
| [**GetNumAnimations**](id3dxanimationset--getnumanimations.md)               | Obtém o número de animações no conjunto de animação.<br/>                    |
| [**Getperiod**](id3dxanimationset--getperiod.md)                             | Obtém o período do conjunto de animações.<br/>                                  |
| [**GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)         | Retorna a posição de hora no período de tempo local de um conjunto de animações.<br/>      |
| [**GetSRT**](id3dxanimationset--getsrt.md)                                   | Obtém os valores de escala, rotação e translação do conjunto de animações.<br/> |



 

## <a name="remarks"></a>Comentários

Um conjunto de animação consiste em animações para muitos nós para a mesma animação.

O tipo LPD3DXANIMATIONSET é definido como um ponteiro para essa interface.


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
