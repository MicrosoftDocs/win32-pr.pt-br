---
description: Função D3DXCreateSkinInfo – cria um objeto de malha de capa vazio usando um Declarador.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: Função D3DXCreateSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfo
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da582d791b27d30c78583972e6f598af8af3eb9e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102734"
---
# <a name="d3dxcreateskininfo-function"></a>Função D3DXCreateSkinInfo

Cria um objeto de malha de capa vazio usando um Declarador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumVertices* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices para a malha de capa.

</dd> <dt>

*pDeclaration* \[ no\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o formato de vértice para a malha retornada.

</dd> <dt>

*NumBones* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de Bones para a malha de capa.

</dd> <dt>

*ppSkinInfo* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Endereço de um ponteiro para uma interface [**ID3DXSkinInfo**](id3dxskininfo.md) , que representa o objeto de malha de capa criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) para popular o objeto de malha de capa vazio retornado por esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
