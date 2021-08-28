---
description: Registre os dados de quadro-chave de dimensionamento, rotação e conversão (SRT) para uma animação.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'Método ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07ec4db0bb02eb0a177375fc37af67264f1368b2ab952c0b170580112e4dbf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987366"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>Método ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys

Registre os dados de quadro-chave de dimensionamento, rotação e conversão (SRT) para uma animação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome da animação.

</dd> <dt>

*NumScaleKeys* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de chaves de escala.

</dd> <dt>

*NumRotationKeys* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de chaves de rotação.

</dd> <dt>

*NumTranslationKeys* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de chaves de tradução.

</dd> <dt>

*pScaleKeys* \[ no\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Endereço de um ponteiro para uma matriz alocada pelo usuário de vetores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que o método preenche com dados de escala.

</dd> <dt>

*pRotationKeys* \[ no\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) \***

Endereço de um ponteiro para uma matriz alocada pelo usuário de quaternions [**D3DXKEY do \_ Quaternion**](d3dxkey-quaternion.md) que o método preenche com dados de rotação.

</dd> <dt>

*pTranslationKeys* \[ no\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Endereço de um ponteiro para uma matriz alocada pelo usuário de vetores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que o método preenche com dados de tradução.

</dd> <dt>

*pAnimationIndex* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Retorna o índice de animação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
