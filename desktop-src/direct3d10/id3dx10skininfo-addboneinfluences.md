---
description: Habilite um Bone existente para influenciar um grupo de vértices e definir quanto influência o Bone tem em cada vértice.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'Método ID3DX10SkinInfo:: AddBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173018"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a>Método ID3DX10SkinInfo:: AddBoneInfluences

Habilite um Bone existente para influenciar um grupo de vértices e definir quanto influência o Bone tem em cada vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*BoneIndex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um índice que especifica um Bone existente. Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*InfluenceCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices a serem adicionados à influência do Bone.

</dd> <dt>

*pIndices* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de índices de vértice. Cada membro dessa matriz tem um membro correspondente em pWeights, de modo que pIndices \[ \] corresponde a pWeights \[ i \] . O valor correspondente em pWeights \[ eu defino o quanto \] a BoneIndex de influência terá no vértice indexado por pIndices \[ i \] . O tamanho da matriz pIndices deve ser igual ou maior que InfluenceCount.

</dd> <dt>

*pWeights* \[ no\]
</dt> <dd>

Tipo: **float \***

Ponteiro para uma matriz de pesos de Bone. Cada membro dessa matriz tem um membro correspondente em pIndices, de modo que pWeights \[ \] corresponde a pIndices \[ i \] . Cada valor em pWeights está entre 0 e 1 e define a quantidade de influência que o Bone tem sobre cada vértice. O tamanho de pWeights deve ser igual ou maior que InfluenceCount.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG ou \_ OUTOFMEMORY.

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

 

 
