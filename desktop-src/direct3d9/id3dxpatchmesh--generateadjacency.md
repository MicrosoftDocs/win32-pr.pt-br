---
description: Gere uma lista de bordas de malha e os patches que compartilham cada borda.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: Método ID3DXPatchMesh::GenerateAdjacency (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GenerateAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41e821d853a8a8f981f1174d654f17475c0363cdcc97bb537e308ccd72e38190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987196"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>Método ID3DXPatchMesh::GenerateAdjacency

Gere uma lista de bordas de malha e os patches que compartilham cada borda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fTolerance* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Especifica que os vértices que diferem na posição por menor que a tolerância devem ser tratados como coincidentes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Depois que um aplicativo gera informações de adjacency para uma malha, os dados de malha podem ser otimizados para um melhor desempenho de desenho. Esse método determina quais patches são adjacentes (dentro da tolerância fornecida). Essas informações são usadas internamente para otimizar o mosaico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
