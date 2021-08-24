---
description: Pega uma malha e retorna uma nova malha com pesos de combinação por vértice, índices e uma tabela de combinação de dois pontos. A tabela descreve quais paletas de malha afetam quais subconjuntos da malha.
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: Método ID3DXSkinInfo::ConvertToIndexedBlendedMesh (D3DX9Mesh.h)
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
ms.openlocfilehash: 9aa2b4bef607197c0f6fea084054d0e4fed1c721388677d45b465aff9c39ce49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790446"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>Método ID3DXSkinInfo::ConvertToIndexedBlendedMesh

Pega uma malha e retorna uma nova malha com pesos de combinação por vértice, índices e uma tabela de combinação de dois pontos. A tabela descreve quais paletas de malha afetam quais subconjuntos da malha.

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

*pMesh* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

A malha de entrada. Consulte [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Opções* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Atualmente não éusado.

</dd> <dt>

*paleetteSize* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de matrizes disponíveis para a paleta de matrizes.

</dd> <dt>

*pAdjacencyIn* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Informações de adjacency de malha de entrada.

</dd> <dt>

*pAdjacencyOut* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**

Informações de adjacency de malha de saída.

</dd> <dt>

*pFaceRemap* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Uma matriz de DWORDs, uma por face, que identifica o rosto da malha original que corresponde a cada rosto na malha mesclada. Se o valor fornecido para esse argumento for **NULL,** os dados de remapa facial não serão retornados.

</dd> <dt>

*ppVertexRemap* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer,**](id3dxbuffer.md) que contém uma DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos. Esse remapa será útil se você precisar alterar dados externos com base no novo mapeamento de vértice. Esse parâmetro é opcional; **NULL** pode ser usado.

</dd> <dt>

*pMaxVertexInfl* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma DWORD que conterá o número máximo de influências de gravidade necessárias por vértice para esse método de decodagem.

</dd> <dt>

*pNumBoneCombinations* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o número de esqueletos na tabela de combinação de animais.

</dd> <dt>

*ppBoneCombinationTable* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Ponteiro para a tabela de combinação de cores. Os dados são organizados em uma [**estrutura D3DXBONECOMBINATION.**](d3dxbonecombination.md)

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Ponteiro para a nova malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Cada elemento nas matrizes de remapa especifica o índice anterior para essa posição. Por exemplo, se um vértice estava na posição 3, mas foi remapeado para a posição 5, o quinto elemento de pVertexRemap conterá 3.

Esse método não é executado em hardware que não dá suporte à combinação de vértice de função fixa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
