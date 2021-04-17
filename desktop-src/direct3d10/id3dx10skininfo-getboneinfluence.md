---
description: Obter a quantidade de influência que um determinado Bone tem sobre um determinado vértice.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'Método ID3DX10SkinInfo:: GetBoneInfluence (D3DX10. h)'
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
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798500"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a>Método ID3DX10SkinInfo:: GetBoneInfluence

Obter a quantidade de influência que um determinado Bone tem sobre um determinado vértice.

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

*BoneIndex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um índice que especifica um Bone existente. Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceIndex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um índice na lista de vértices do Bone que ele influencia.

</dd> <dt>

*pWeight* \[ no\]
</dt> <dd>

Tipo: **float \***

A quantidade de influência, entre 0 e 1, que o Bone tem sobre o vértice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser E \_ INVALIDARG.

## <a name="remarks"></a>Comentários

Use ID3DX10SkinInfo:: GetBoneInfluenceCount para descobrir quantos vértices o Bone influencia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
