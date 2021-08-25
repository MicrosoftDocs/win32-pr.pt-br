---
description: 'Método ID3DXBaseMesh:: GenerateAdjacency – gera uma lista de bordas de malha, bem como uma lista de faces que compartilham cada borda.'
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
ms.openlocfilehash: d51070b5b67b50859338943a60e44cbb224e572ab9e5704e56940328a65479f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848526"
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

## <a name="return-value"></a>Valor retornado

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

 

 
