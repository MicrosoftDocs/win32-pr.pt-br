---
description: As atualizações influenciam as informações para corresponder aos vértices depois que são reordenadas. Esse método deverá ser chamado se o buffer de vértice de destino tiver sido reordenado externamente.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: Método ID3DXSkinInfo::Remap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 941a71539184b7d49e35627c932da77b4494486c35506b1b4e5f69ad52c40829
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727776"
---
# <a name="id3dxskininforemap-method"></a>Método ID3DXSkinInfo::Remap

As atualizações influenciam as informações para corresponder aos vértices depois que são reordenadas. Esse método deverá ser chamado se o buffer de vértice de destino tiver sido reordenado externamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumVertices* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices a remapa.

</dd> <dt>

*pVertexRemap* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Matriz de DWORDS cujo comprimento é especificado por NumVertices.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Cada elemento em pVertexRemap especifica o índice de vértice anterior para essa posição. Por exemplo, se um vértice estava na posição 3, mas foi remapeado para a posição 5, o quinto elemento de pVertexRemap deve conter 3. A matriz de remapa de vértice retornada [**por ID3DXMesh::Optimize**](id3dxmesh--optimize.md) pode ser usada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
