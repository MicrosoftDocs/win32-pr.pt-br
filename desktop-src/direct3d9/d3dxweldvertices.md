---
description: As soldas agrupam vértices replicados que têm atributos iguais. Esse método usa valores de Épsilon especificados para comparações de igualdade.
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: Função D3DXWeldVertices (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664017"
---
# <a name="d3dxweldvertices-function"></a>Função D3DXWeldVertices

As soldas agrupam vértices replicados que têm atributos iguais. Esse método usa valores de Épsilon especificados para comparações de igualdade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para um objeto [**ID3DXMesh**](id3dxmesh.md) , a malha da qual os vértices de soldagem.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores de [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).

</dd> <dt>

*pEpsilons* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

Ponteiro para uma estrutura [**D3DXWeldEpsilons**](d3dxweldepsilons.md) , especificando os valores de Épsilon a serem usados para esse método. Use **NULL** para inicializar todos os membros da estrutura com um valor padrão de 1,0 e-6F.

</dd> <dt>

*pAdjacencyIn* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha de origem. Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF. Se esse parâmetro for definido como **NULL**, [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) será chamado para criar informações de adjacência lógica.

</dd> <dt>

*pAdjacencyOut* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha otimizada. Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.

</dd> <dt>

*pFaceRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha soldada.

</dd> <dt>

*ppVertexRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos. Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função usa informações de adjacência fornecidas para determinar os pontos que são replicados. Os vértices são mesclados com base em uma comparação de Épsilon. Os vértices com a mesma posição já devem ter sido calculados e representados por dados de representante de ponto.

Essa função combina vértices com soldagem lógica que têm componentes semelhantes, como normalidades ou coordenadas de textura dentro de pEpsilons.

O código de exemplo a seguir chama essa função com soldagem habilitada. Os vértices são comparados usando valores de Épsilon para a posição normal do vetor e do vértice. Um ponteiro é retornado para uma matriz de remapeamento facial (*pFaceRemap*).


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
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

 

 
