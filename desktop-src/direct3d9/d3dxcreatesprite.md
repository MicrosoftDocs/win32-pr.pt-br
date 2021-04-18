---
description: Cria um objeto Sprite associado a um dispositivo específico. Os objetos Sprite são usados para desenhar imagens 2D na tela.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Função D3DXCreateSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798196"
---
# <a name="d3dxcreatesprite-function"></a>Função D3DXCreateSprite

Cria um objeto Sprite associado a um dispositivo específico. Os objetos Sprite são usados para desenhar imagens 2D na tela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado ao Sprite.

</dd> <dt>

*ppSprite* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***

Endereço de um ponteiro para uma interface [**ID3DXSprite**](id3dxsprite.md) . Essa interface permite que o usuário acesse as funções Sprite.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa interface pode ser usada para desenhar duas imagens dimensionais no espaço da tela do dispositivo associado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
