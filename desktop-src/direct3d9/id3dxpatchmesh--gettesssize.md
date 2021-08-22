---
description: Obtém o tamanho da malha mosaico, dado um nível de mosaico.
ms.assetid: 86d1d1a0-1934-40e9-bff9-6c435d1e5183
title: 'Método ID3DXPatchMesh:: GetTessSize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetTessSize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4668f50236684f104aedf0ad9ecad413a583facbc45d5f3fa0331abb5938bf5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493046"
---
# <a name="id3dxpatchmeshgettesssize-method"></a>Método ID3DXPatchMesh:: GetTessSize

Obtém o tamanho da malha mosaico, dado um nível de mosaico.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTessSize(
  [in]  FLOAT fTessLevel,
  [in]  DWORD Adaptive,
  [out] DWORD *NumTriangles,
  [out] DWORD *NumVertices
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fTessLevel* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Nível de mosaico.

</dd> <dt>

*Adaptável* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Mosaico adaptável. Para mosaico adaptável, defina esse valor como **true** e defina fTessLevel como o valor de mosaico máximo. Isso resultará no tamanho máximo de malha necessário para mosaico adaptável.

</dd> <dt>

*NumTriangles* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o número de triângulos gerados pela malha mosaico.

</dd> <dt>

*NumVertices* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para o número de vértices gerados pela malha mosaico.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Esse método pressupõe mosaico uniforme.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> </dl>

 

 
