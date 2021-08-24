---
description: Obter uma lista de vértices que um determinado nome influencia e uma lista da quantidade de influência que o sr. tem em cada vértice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: Método ID3DX10SkinInfo::GetBoneInfluences (D3DX10.h)
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
ms.openlocfilehash: 38d6901abd871a2b65f4d6816ad4d4b7a0d2effb5ccbd3f4ccee20bc0b8d5ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752906"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a>Método ID3DX10SkinInfo::GetBoneInfluences

Obter uma lista de vértices que um determinado nome influencia e uma lista da quantidade de influência que o sr. tem em cada vértice.

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

*DexIndex* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um índice que especifica um fragmento existente. Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo::GetNumBones.**](id3dx10skininfo-getnumbones.md)

</dd> <dt>

*Deslocamento* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um deslocamento da parte superior da lista de vértices influenciados. Isso deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo::GetBoneInfluenceCount.**](id3dx10skininfo-getboneinfluencecount.md)

</dd> <dt>

*Contagem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de índices e pesos a recuperar. Deve estar entre 0 e o valor retornado por ID3DX10SkinInfo::GetBoneInfluenceCount.

</dd> <dt>

*pDestIndices* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Uma lista de índices no buffer de vértice, cada um representando um vértice influenciado pelo apêndice. Esses valores correspondem aos valores em pDestWeights, de forma que pDestIndices \[ i \] corresponda a pDestWeights \[ i \] .

</dd> <dt>

*pDestWeights* \[ in, out\]
</dt> <dd>

Tipo: **\* float**

Uma lista da quantidade de influência que o sr. tem em cada vértice. Esses valores correspondem aos valores em pDestIndices, de forma que pDestWeights i corresponda \[ \] a pDestIndices \[ i \] .f

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG ou E \_ OUTOFMEMORY.

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

 

 
