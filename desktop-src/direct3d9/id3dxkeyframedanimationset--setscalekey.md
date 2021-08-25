---
description: Defina informações de escala para um quadro-chave específico no conjunto de animações.
ms.assetid: b606e5d3-11c9-4997-ad3c-d3ae21c32e10
title: 'Método ID3DXKeyframedAnimationSet:: SetScaleKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d5d33ab0c8e6bd01335d5843121917f89e3cf60bd81a5d54a85d298ec990e4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748205"
---
# <a name="id3dxkeyframedanimationsetsetscalekey-method"></a>Método ID3DXKeyframedAnimationSet:: SetScaleKey

Defina informações de escala para um quadro-chave específico no conjunto de animações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Animação* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de animação.

</dd> <dt>

*Chave* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Quadro-chave.

</dd> <dt>

*pScaleKeys* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Ponteiro para os dados de escala. Consulte [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
