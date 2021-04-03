---
description: Preenche uma matriz com dados de chave de rotação usados para animação de quadro chave.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'Método ID3DXKeyframedAnimationSet:: GetRotationKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664092"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a>Método ID3DXKeyframedAnimationSet:: GetRotationKeys

Preenche uma matriz com dados de chave de rotação usados para animação de quadro chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Animação* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de animação.

</dd> <dt>

*pRotationKeys* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**

Ponteiro para uma matriz alocada pelo usuário de quaternions [**D3DXKEY do \_ Quaternion**](d3dxkey-quaternion.md) que o método deve preencher com dados de rotação de animação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
