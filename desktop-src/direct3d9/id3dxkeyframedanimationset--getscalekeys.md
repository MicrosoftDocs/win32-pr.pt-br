---
description: Preenche uma matriz com dados de chave de escala usados para animação de quadro-chave.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: Método ID3DXKeyframedAnimationSet::GetScaleKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1158195ae84f8215869571fc400950a6dfd475fc37050572ffb5e3e77f96d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493506"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a>Método ID3DXKeyframedAnimationSet::GetScaleKeys

Preenche uma matriz com dados de chave de escala usados para animação de quadro-chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Animação* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de animação.

</dd> <dt>

*pScaleKeys* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Ponteiro para uma matriz alocada pelo usuário de [**vetores D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que o método deve preencher com dados de escala de animação.

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
