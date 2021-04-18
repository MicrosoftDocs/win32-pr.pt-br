---
description: Converta o subconjunto de malha especificado em uma série de faixas.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: Função D3DXConvertMeshSubsetToStrips (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771516"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a>Função D3DXConvertMeshSubsetToStrips

Converta o subconjunto de malha especificado em uma série de faixas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Malha* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando a malha a ser convertida em uma faixa.

</dd> <dt>

*Atribid* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

ID de atributo do subconjunto de malha a ser convertido em faixas.

</dd> <dt>

*IBOptions* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando opções para criar o buffer de índice. Não pode ser D3DXMESH \_ 32 bits. O buffer de índice será criado com índices de 32 bits ou de 16 bits, dependendo do formato do buffer de índice da malha especificada pelo parâmetro *mesh* .

</dd> <dt>

*ppIndexBuffer* \[ fora\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Ponteiro para uma interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , representando o buffer de índice que contém a faixa.

</dd> <dt>

*pNumIndices* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de índices no buffer retornado no parâmetro *ppIndexBuffer* .

</dd> <dt>

*ppStripLengths* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Buffer que contém uma matriz de um DWORD por faixa, que especifica o número de triângulos na faixa.

</dd> <dt>

*pNumStrips* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Número de faixas individuais no buffer de índice e na matriz de comprimento de faixa correspondente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Antes de executar essa função, chame [**Optimize**](id3dxmesh--optimize.md) ou [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), com o \_ sinalizador D3DXMESHOPT ATTRSORT definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
