---
description: Computa Normals de unidade para cada vértice em uma malha. Fornecido para dar suporte a aplicativos herdados. Use D3DXComputeTangentFrameEx para obter resultados melhores.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Função D3DXComputeNormals (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f95e5e353c318429f5340d1a831f9ca3050ba3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930646"
---
# <a name="d3dxcomputenormals-function"></a>Função D3DXComputeNormals

Computa Normals de unidade para cada vértice em uma malha. Fornecido para dar suporte a aplicativos herdados. Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obter resultados melhores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando o objeto de malha normalizado.

</dd> <dt>

*pAdjacency* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha progressiva criada. Esse parâmetro é opcional e deve ser definido como **nulo** se não for usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A malha de entrada deve ter o sinalizador [ \_ normal D3DFVF](d3dfvf.md) especificado em seu formato de vértice flexível (FVF).

Um normal para um vértice é gerado pela média dos normais de todas as faces que compartilham esse vértice.

Se a adjacência for fornecida, os vértices replicados serão ignorados e "suavizados". Se a adjacência não for fornecida, os vértices replicados terão a média normal de somente as faces que as referenciam explicitamente.

Essa função simplesmente chama [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) com os seguintes parâmetros de entrada:


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
