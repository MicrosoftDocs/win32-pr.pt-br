---
description: Gera uma malha com faces e vértices reordenados para otimizar o desempenho do desenho. Esse método reordena a malha existente.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'Método ID3DXMesh:: OptimizeInplace (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0075e7a0b823f0d747859a4717a440e0c244fde76076e4b285c7d1b2a7e78d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120800"
---
# <a name="id3dxmeshoptimizeinplace-method"></a>Método ID3DXMesh:: OptimizeInplace

Gera uma malha com faces e vértices reordenados para otimizar o desempenho do desenho. Esse método reordena a malha existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinação de um ou mais sinalizadores [**D3DXMESHOPT**](./d3dxmeshopt.md) , especificando o tipo de otimização a ser executado.

</dd> <dt>

*pAdjacencyIn* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha de origem. Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF.

</dd> <dt>

*pAdjacencyOut* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de três DWORDs por face que especifica os três vizinhos para cada face na malha otimizada. Se a borda não tiver faces adjacentes, o valor será 0xFFFFFFFF. Se o valor fornecido para esse argumento for **nulo**, os dados de adjacência não serão retornados.

</dd> <dt>

*pFaceRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Uma matriz de DWORDs, uma por face, que identifica a face de malha original que corresponde a cada face na malha otimizada. Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento facial não serão retornados.

</dd> <dt>

*ppVertexRemap* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) , que contém um DWORD para cada vértice que especifica como os novos vértices são mapeados para os vértices antigos. Esse remapeamento será útil se você precisar alterar dados externos com base no novo mapeamento de vértice. Se o valor fornecido para esse argumento for **nulo**, os dados de remapeamento de vértice não serão retornados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Antes de executar **ID3DXMesh:: OptimizeInplace**, um aplicativo deve gerar um buffer de adjacência chamando [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md). O buffer de adjacência contém dados de adjacência, como uma lista de bordas e as faces que são adjacentes entre si.

> [!Note]  
> Esse método falhará se a malha estiver compartilhando seu buffer de vértice com outra malha, a menos que D3DXMESHOPT \_ IGNOREVERTS seja definido em sinalizadores.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md)
</dt> </dl>

 

 
