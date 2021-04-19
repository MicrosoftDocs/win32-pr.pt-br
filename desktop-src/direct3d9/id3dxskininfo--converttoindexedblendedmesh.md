---
description: Usa uma malha e retorna uma nova malha com pesos de mistura por vértice, índices e uma tabela de combinação de Bone. A tabela descreve quais paletas de Bone afetam quais subconjuntos da malha.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'Método ID3DXSkinInfo:: ConvertToIndexedBlendedMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768210"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>Método ID3DXSkinInfo:: ConvertToIndexedBlendedMesh

Usa uma malha e retorna uma nova malha com pesos de mistura por vértice, índices e uma tabela de combinação de Bone. A tabela descreve quais paletas de Bone afetam quais subconjuntos da malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

A malha de entrada. Consulte [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Opções* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Atualmente não utilizado.

</dd> <dt>

*paletteSize* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de matrizes Bone disponíveis para a aparência da paleta de matriz.

</dd> <dt>

*pAdjacencyIn* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Informações de adjacência da malha de entrada.

</dd> <dt>

*pAdjacencyOut* \[ no\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Informações de adjacência de malha de saída.

</dd> <dt>

*pFaceRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha mesclada. Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.

</dd> <dt>

*ppVertexRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos. Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice. Esse parâmetro é opcional; **NULL** pode ser usado.

</dd> <dt>

*pMaxVertexInfl* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para um DWORD que conterá o número máximo de influências Bone necessárias por vértice para esse método de aparência.

</dd> <dt>

*pNumBoneCombinations* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o número de Bones na tabela de combinação de Bone.

</dd> <dt>

*ppBoneCombinationTable* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ponteiro para a tabela de combinação de Bone. Os dados são organizados em uma estrutura [**D3DXBONECOMBINATION**](d3dxbonecombination.md) .

</dd> <dt>

*ppMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Ponteiro para a nova malha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Cada elemento nas matrizes de remapeamento especifica o índice anterior para essa posição. Por exemplo, se um vértice estava na posição 3, mas foi remapeado para a posição 5, o quinto elemento de pVertexRemap conterá 3.

Esse método não é executado em hardware que não dá suporte à mesclagem de vértice de função fixa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
