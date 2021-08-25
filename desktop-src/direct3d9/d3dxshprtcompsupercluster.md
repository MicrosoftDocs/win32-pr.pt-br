---
description: Função D3DXSHPRTCompSuperCluster – usada com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) precomputado.
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Função D3DXSHPRTCompSuperCluster (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55556046c7fa8e0a8e7666a9d2dd0a20d81b5f3cf59253f499cbd7d0fba41fbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749822"
---
# <a name="d3dxshprtcompsupercluster-function"></a>Função D3DXSHPRTCompSuperCluster

Usado com resultados compactados da versão de vértice do simulador de transferência radiante (PRT) de computação. Gera "superclusters", que são grupos de clusters que podem ser desenhados na mesma chamada de desenho. Um algoritmo de ávido que minimiza o superempate é usado para agrupar os clusters.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pClusterIDs* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para as IDs de cluster NumVerts (extraídas de um buffer compactado).

</dd> <dt>

*pScene* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma malha que representa a cena composta passada para o simulador. Consulte [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*MaxNumClusters* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de clusters alocados por super cluster.

</dd> <dt>

*NumClusters* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de clusters computados no simulador.

</dd> <dt>

*pSClusterIDs* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de comprimento *NumClusters*. Contém o índice do super cluster ao qual o cluster correspondente foi atribuído.

</dd> <dt>

*pNumSCs* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Número de superclusters alocados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
