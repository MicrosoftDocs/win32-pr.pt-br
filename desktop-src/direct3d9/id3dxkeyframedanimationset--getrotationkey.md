---
description: Obter informações de rotação para um quadro-chave específico no conjunto de animação.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: Método ID3DXKeyframedAnimationSet::GetRotationKey (D3dx9rotam.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5abb39061b1782b7794ec475a6217677c8723625e2752237c122a694435f2862
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951466"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a>Método ID3DXKeyframedAnimationSet::GetRotationKey

Obter informações de rotação para um quadro-chave específico no conjunto de animação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Animação* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de animação.

</dd> <dt>

*Chave* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Quadro-chave.

</dd> <dt>

*pRotationKeys* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**

Ponteiro para os dados de rotação. Consulte [**D3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
