---
description: Adiciona um quadro filho a um quadro.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: Função D3DXFrameAppendChild (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173001"
---
# <a name="d3dxframeappendchild-function"></a>Função D3DXFrameAppendChild

Adiciona um quadro filho a um quadro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFrameParent* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Ponteiro para o nó pai.

</dd> <dt>

*pFrameChild* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Ponteiro para o nó filho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




