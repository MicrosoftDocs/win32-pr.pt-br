---
description: Obtenha uma lista de vértices que um determinado Bone influencia e uma lista da quantidade de influência que o Bone tem em cada vértice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'Método ID3DX10SkinInfo:: GetBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173196"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>Método ID3DX10SkinInfo:: GetBoneInfluences

Obtenha uma lista de vértices que um determinado Bone influencia e uma lista da quantidade de influência que o Bone tem em cada vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*BoneIndex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um índice que especifica um Bone existente. Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> <dt>

*Deslocamento* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um deslocamento da parte superior da lista de vértices influenciados do Bone. Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).

</dd> <dt>

*Contagem* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de índices e pesos a serem recuperados. Deve estar entre 0 e o valor retornado por ID3DX10SkinInfo:: GetBoneInfluenceCount.

</dd> <dt>

*pDestIndices* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Uma lista de índices no buffer de vértice, cada um representando um vértice influenciado pelo Bone. Esses valores correspondem aos valores em pDestWeights, de modo que pDestIndices \[ \] corresponde a pDestWeights \[ i \] .

</dd> <dt>

*pDestWeights* \[ entrada, saída\]
</dt> <dd>

Tipo: **float \***

Uma lista da quantidade de influência que o Bone tem em cada vértice. Esses valores correspondem aos valores em pDestIndices, de modo que pDestWeights \[ \] corresponde a pDestIndices \[ i \] . f

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

 

 
