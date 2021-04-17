---
description: Computa os vetores tangentes das coordenadas de textura dadas no estágio de textura. Fornecido para dar suporte a aplicativos herdados. Use D3DXComputeTangentFrameEx para obter resultados melhores.
ms.assetid: 39748459-3f9b-4b48-ae13-7143eb29c292
title: Função D3DXComputeTangent (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangent
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cdb6a9dae3bdbad0f239fa61ba066d7b1bffb14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812289"
---
# <a name="d3dxcomputetangent-function"></a>Função D3DXComputeTangent

Computa os vetores tangentes das coordenadas de textura dadas no estágio de textura. Fornecido para dar suporte a aplicativos herdados. Use [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) para obter resultados melhores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeTangent(
  _In_       LPD3DXMESH Mesh,
  _In_       DWORD      TexStageIndex,
  _In_       DWORD      TangentIndex,
  _In_       DWORD      BinormIndex,
  _In_       DWORD      Wrap,
  _In_ const DWORD      *pAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Malha* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) que representa a malha de entrada.

</dd> <dt>

*TexStageIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice que representa o estágio de textura.

</dd> <dt>

*TangentIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice que fornece o índice de uso para os dados da tangente. A declaração de vértice implica o uso; Esse índice modifica o uso com o índice de uso. Para obter mais informações sobre uma declaração de vértice, consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*BinormIndex* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice que fornece o índice de uso para os dados binormal. A declaração de vértice implica o uso; Esse índice modifica o uso com o índice de uso. Para obter mais informações sobre uma declaração de vértice, consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).

</dd> <dt>

*Encapsular* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Defina esse valor como 0 para sem quebra automática ou para 1 para quebra automática nas direções você e V.

</dd> <dt>

*pAdjacency* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face a ser preenchida com índices de face adjacentes. O número de bytes nessa matriz deve ser pelo menos (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Se a declaração de vértice de malha especificar campos tangentes ou binormal, o **D3DXComputeTangent** atualizará todos os dados tangentes ou binormals fornecidos pelo usuário. Como alternativa, defina TangentIndex como [D3DX como \_ padrão](other-d3dx-constants.md) para não atualizar os dados tangentes fornecidos pelo usuário ou defina BinormIndex como D3DX como \_ padrão para não atualizar os dados binormal fornecidos pelo usuário. TexStageIndex não pode ser definido como D3DX \_ padrão.

**D3DXComputeTangent** depende da declaração de vértice de malha que contém o campo binormal (BinormIndex), o campo tangente (TangentIndex) ou ambos. Se ambos estiverem ausentes, essa função falhará.

Essa função simplesmente chama [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) com os seguintes parâmetros de entrada:


```
D3DXComputeTangentFrameEx( Mesh,
                           D3DDECLUSAGE_TEXCOORD,
                           TexStageIndex,
                           ( BinormIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_BINORMAL,
                               // provides backward function compatibility
                           BinormIndex,
                           ( TangentIndex == D3DX_DEFAULT ) ?
                               D3DX_DEFAULT : D3DDECLUSAGE_TANGENT,
                           TangentIndex,
                           D3DX_DEFAULT, // do not store normals
                           0,
                           ( Wrap ? D3DXTANGENT_WRAP_UV : 0 )
                               | D3DXTANGENT_GENERATE_IN_PLACE
                               | D3DXTANGENT_ORTHOGONALIZE_FROM_U,
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

 

 
