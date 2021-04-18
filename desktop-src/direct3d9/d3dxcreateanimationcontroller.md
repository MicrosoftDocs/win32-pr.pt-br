---
description: Cria um objeto de controlador de animação.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Função D3DXCreateAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763006"
---
# <a name="d3dxcreateanimationcontroller-function"></a>Função D3DXCreateAnimationController

Cria um objeto de controlador de animação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaxNumAnimationOutputs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de saídas de animação às quais o controlador pode dar suporte.

</dd> <dt>

*MaxNumAnimationSets* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animação que podem ser misturados.

</dd> <dt>

*MaxNumTracks* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animação que podem ser misturados simultaneamente.

</dd> <dt>

*MaxNumEvents* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de eventos pendentes aos quais o controlador dará suporte.

</dd> <dt>

*ppAnimController* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Ponteiro para o objeto do controlador de animação criado. Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Um controlador de animação controla um mixer de animação. O controlador adiciona métodos para modificar parâmetros de mesclagem ao longo do tempo para habilitar transições suaves.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
