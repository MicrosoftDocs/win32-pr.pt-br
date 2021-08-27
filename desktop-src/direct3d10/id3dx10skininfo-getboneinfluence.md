---
description: Obter a quantidade de influência de um determinado vértice sobre um determinado vértice.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: Método ID3DX10SkinInfo::GetBoneInfluence (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b53f642b6e62bb37c6979602b1ae66e09ffc2eb42a6d47c70c6b895a01ba273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096546"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>Método ID3DX10SkinInfo::GetBoneInfluence

Obter a quantidade de influência de um determinado vértice sobre um determinado vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DexIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um índice que especifica um fragmento existente. Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo::GetNumBones.**](id3dx10skininfo-getnumbones.md)

</dd> <dt>

*InfluenceIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um índice na lista de vértices que ele influencia.

</dd> <dt>

*pWeight* \[ Em\]
</dt> <dd>

Tipo: **\* float**

A quantidade de influência, entre 0 e 1, que o sr. tem sobre o vértice.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser E \_ INVALIDARG.

## <a name="remarks"></a>Comentários

Use ID3DX10SkinInfo::GetBoneInfluenceCount para descobrir quantos vértices o urso influencia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
