---
description: Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'Método ID3DXMesh:: Optimize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930762"
---
# <a name="id3dxmeshoptimize-method"></a>Método ID3DXMesh:: Optimize

Gera uma nova malha com faces e vértices reordenados para otimizar o desempenho do desenho.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Especifica o tipo de otimização a ser executado. Esse parâmetro pode ser definido como uma combinação de um ou mais sinalizadores de [**D3DXMESHOPT**](./d3dxmeshopt.md) e [**D3DXMESH**](./d3dxmesh.md) (exceto D3DXMESH \_ 32 bits, D3DXMESH \_ IB \_ WriteOnly e D3DXMESH \_ WRITEONLY).

</dd> <dt>

*pAdjacencyIn* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha de origem. Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF. Consulte Observações.

</dd> <dt>

*pAdjacencyOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha otimizada. Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.

</dd> <dt>

*pFaceRemap* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha otimizada. Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.

</dd> <dt>

*ppVertexRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos. Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.

</dd> <dt>

*ppOptMesh* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha otimizada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método gera uma nova malha. Antes de executar Optimize, um aplicativo deve gerar um buffer de adjacência chamando [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). O buffer de adjacência contém dados de adjacência, como uma lista de bordas e as faces que são adjacentes entre si.

Esse método é muito semelhante ao método [**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) , exceto pelo fato de que ele pode executar a otimização ao gerar o novo clone da malha. A malha de saída herda todos os parâmetros de criação da malha de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh::OptimizeInplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
