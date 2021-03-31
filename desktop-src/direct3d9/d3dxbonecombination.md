---
description: Descreve um subconjunto da malha que tem a mesma combinação de atributo e Bone.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: Estrutura D3DXBONECOMBINATION (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012113"
---
# <a name="d3dxbonecombination-structure"></a>Estrutura D3DXBONECOMBINATION

Descreve um subconjunto da malha que tem a mesma combinação de atributo e Bone.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**Atribid**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identificador de tabela de atributo.

</dd> <dt>

**FaceStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando face.

</dd> <dt>

**FaceCount**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Contagem de face.

</dd> <dt>

**VertexStart**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Iniciando vértice.

</dd> <dt>

**Contagemdevértice**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Contagem de vértices.

</dd> <dt>

**Boneid**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

Ponteiro para uma matriz de valores que identifica cada um dos Bones que podem ser desenhados em uma única chamada de desenho. Observe que a matriz pode ser de comprimento variável para acomodar combinações Bone de comprimento variável de [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).

O tamanho da matriz varia de acordo com o tipo de malha gerada. Um tamanho de matriz de malha não indexada é igual ao número de pesos por vértice (pMaxVertexInfl em [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)). Um tamanho de matriz de malha indexada é igual ao número de entradas da paleta de matriz Bone (paletteSize em [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).

</dd> </dl>

## <a name="remarks"></a>Comentários

O subconjunto da malha descrito por **D3DXBONECOMBINATION** pode ser renderizado em uma única chamada de desenho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
