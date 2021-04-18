---
description: Gere uma lista de bordas de malha e os patches que compartilham cada borda.
ms.assetid: 024528c0-2c0d-4448-9b38-05cf8d6ffc63
title: 'Método ID3DXPatchMesh:: GenerateAdjacency (D3DX9Mesh. h)'
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
ms.openlocfilehash: 68de2a77b9d27391c57ec299ceb87d29166ee248
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370924"
---
# <a name="id3dxpatchmeshgenerateadjacency-method"></a>Método ID3DXPatchMesh:: GenerateAdjacency

Gere uma lista de bordas de malha e os patches que compartilham cada borda.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GenerateAdjacency(
  [in] FLOAT fTolerance
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fTolerance* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Especifica que os vértices que diferem na posição por menos que a tolerância devem ser tratados como coincidentes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Depois que um aplicativo gera informações de adjacência para uma malha, os dados de malha podem ser otimizados para melhorar o desempenho do desenho. Esse método determina quais patches são adjacentes (dentro da tolerância fornecida). Essas informações são usadas internamente para otimizar o mosaico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh:: Optimize**](id3dxpatchmesh--optimize.md)
</dt> </dl>

 

 
