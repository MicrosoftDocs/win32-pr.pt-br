---
description: Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.
ms.assetid: 9d52290f-1c9e-43a7-b239-35cd54e36466
title: 'Método ID3DXBaseMesh:: GenerateAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5b1d304878a4977bb14d6ef98ad7256b6c3181f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370988"
---
# <a name="id3dxbasemeshgenerateadjacency-method"></a>Método ID3DXBaseMesh:: GenerateAdjacency

Gere uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT Epsilon,
  [in] DWORD *pAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Épsilon* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica que os vértices que diferem na posição por menos de Épsilon devem ser tratados como coincidentes.

</dd> <dt>

*pAdjacency* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de três DWORDs por face a ser preenchida com os índices de faces adjacentes. O número de bytes nessa matriz deve ser pelo menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados para melhorar o desempenho do desenho.

A ordem das entradas no buffer de adjacência é determinada pela ordem dos índices de vértice no buffer de índice. O triângulo adjacente 0 sempre corresponde à borda entre os índices dos cantos 0 e 1. O triângulo adjacente 1 sempre corresponde à borda entre os índices dos cantos 1 e 2, enquanto o triângulo adjacente 2 corresponde à borda entre os índices dos cantos 2 e 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
