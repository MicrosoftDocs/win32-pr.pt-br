---
description: Limpa uma malha, preparando-a para simplificação.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Função D3DXCleanMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: adc5d60b66dc9eaa06314e18ead26412b8572e9dbc649070c37891a62fb9ecbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495906"
---
# <a name="d3dxcleanmesh-function"></a>Função D3DXCleanMesh

Limpa uma malha, preparando-a para simplificação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CleanType* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**

Operações de vértice a executar na preparação para limpeza de malha. Consulte [**D3DXCLEANTYPE**](./d3dxcleantype.md).

</dd> <dt>

*pMeshIn* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para uma [**interface ID3DXMesh,**](id3dxmesh.md) representando a malha a ser limpa.

</dd> <dt>

*pAdjacencyIn* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha a ser limpo.

</dd> <dt>

*ppMeshOut* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Endereço de um ponteiro para uma interface [**ID3DXMesh,**](id3dxmesh.md) representando a malha limpa retornada. A mesma malha é retornada que foi passada se nenhuma limpeza foi necessária.

</dd> <dt>

*pAdjacencyOut* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha de saída.

</dd> <dt>

*ppErrorsAndWarnings* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retorna um buffer que contém uma cadeia de caracteres de erros e avisos, que explica os problemas encontrados na malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função limpa uma malha usando o método de limpeza e as opções especificadas no parâmetro CleanType. Consulte a [**enumeração D3DXCLEANTYPE**](./d3dxcleantype.md) para ver uma descrição das opções disponíveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
