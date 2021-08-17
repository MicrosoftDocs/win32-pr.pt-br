---
description: Tessellates um patch de superfície de ordem superior triangular em uma malha de triângulo.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Função D3DXTessellateTriPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1cae3ff9709cb74e15c176abc0e738e4f12d1417eec1d040b90269b7e3cbc6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122708"
---
# <a name="d3dxtessellatetripatch-function"></a>Função D3DXTessellateTriPatch

Tessellates um patch de superfície de ordem superior triangular em uma malha de triângulo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
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

Ponteiro para uma matriz de três valores de ponto flutuante que identificam o número de segmentos nos quais cada borda do patch de triângulo deve ser dividida quando mosaico. Consulte [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

</dd> <dt>

*pInDecl* \[ no\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Estrutura de declaração de vértice que define os dados de vértice. Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pTriPatchInfo* \[ no\]
</dt> <dd>

Tipo: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***

Descreve um patch de triângulo. Consulte [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).

</dd> <dt>

*pMesh* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para a malha criada. Consulte [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) para obter o número de vértices de saída e os índices necessários para a função de mosaico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
