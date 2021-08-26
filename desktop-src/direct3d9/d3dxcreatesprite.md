---
description: Cria um objeto sprite associado a um dispositivo específico. Os objetos sprite são usados para desenhar imagens 2D para a tela.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Função D3DXCreateSprite (D3dx9core.h)
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
ms.openlocfilehash: 8fe6d4897a581302f27544217c3caf5b6c723ce2ff4aed611b40a21cd7b0d35f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027736"
---
# <a name="d3dxcreatesprite-function"></a>Função D3DXCreateSprite

Cria um objeto sprite associado a um dispositivo específico. Os objetos sprite são usados para desenhar imagens 2D para a tela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) o dispositivo a ser associado ao sprite.

</dd> <dt>

*ppSprite* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***

Endereço de um ponteiro para uma [**interface ID3DXSprite.**](id3dxsprite.md) Essa interface permite que o usuário acesse funções de sprite.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa interface pode ser usada para desenhar imagens bidimensionais no espaço de tela do dispositivo associado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
