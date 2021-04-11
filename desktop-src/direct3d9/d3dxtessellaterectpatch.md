---
description: Tessellates um patch de superfície de ordem superior retangular em uma malha de triangulares.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Função D3DXTessellateRectPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172981"
---
# <a name="d3dxtessellaterectpatch-function"></a>Função D3DXTessellateRectPatch

Tessellates um patch de superfície de ordem superior retangular em uma malha de triangulares.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVB* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

O buffer de vértices que contém os dados do patch.

</dd> <dt>

*pNumSegs* \[ no\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de quatro valores de ponto flutuante que identificam o número de segmentos nos quais cada borda do patch de retângulo deve ser dividida quando mosaico. Consulte [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

</dd> <dt>

*pInDecl* \[ no\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Estrutura de declaração de vértice que define os dados de vértice. Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pRectPatchInfo* \[ no\]
</dt> <dd>

Tipo: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***

Descreve um patch retangular. Consulte [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).

</dd> <dt>

*pMesh* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para a malha criada. Consulte [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) para obter o número de vértices de saída e os índices necessários para a função de mosaico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
