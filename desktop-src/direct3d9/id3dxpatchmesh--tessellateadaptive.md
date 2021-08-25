---
description: Executa mosaico adaptável com base no critério de mosaico adaptável baseado em z.
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'Método ID3DXPatchMesh:: TessellateAdaptive (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6365cfcf50debfeeb28fd493b76ac60943ee14f27a2dadec168b3dd4d31ace1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856286"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a>Método ID3DXPatchMesh:: TessellateAdaptive

Executa mosaico adaptável com base no critério de mosaico adaptável baseado em z.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTrans* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Especifica um vetor 4D que é pontilhado com os vértices para obter a quantidade de mosaico adaptável por vértice. Cada borda é mosaico ao valor médio dos níveis de mosaico para os dois vértices que ele conecta.

</dd> <dt>

*dwMaxTessLevel* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Limite máximo para mosaico adaptável. Este é o número de vértices introduzidos entre os vértices existentes. Esse valor inteiro pode variar de 1 a 32, inclusive.

</dd> <dt>

*dwMinTessLevel* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Limite mínimo para mosaico adaptável. Este é o número de vértices introduzidos entre os vértices existentes. Esse valor inteiro pode variar de 1 a 32, inclusive.

</dd> <dt>

*pMesh* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Malha mosaico resultante. Consulte [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Essa função será executada com mais eficiência se a malha de patches tiver sido otimizada usando [**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
